# diffusion-based-planning
Working idea







Diffusion-based planning

(Reference:)

## Getting Started

- Setup [nuPlan dataset](https://nuplan-devkit.readthedocs.io/en/latest/dataset_setup.html)
- Setup conda environment
```
conda create -n diffusion_planner python=3.9
conda activate diffusion_planner

# install nuplan-devkit
git clone https://github.com/motional/nuplan-devkit.git
cd nuplan-devkit
pip install -e .
pip install -r requirements.txt
```
If error: No matching distribution found for omegaconf==2.1.0.rc1
```
# Downgrade your pip
python -m pip install pip==24.0
```

Setup diffusion_planner
```
cd ..
git clone https://github.com/ZhengYinan-AIR/Diffusion-Planner.git
cd Diffusion-Planner
pip install -e .
pip install -r requirements_torch.txt
```

### Closed-loop Evaluation
- Download the model checkpoint from [Huggingface](https://huggingface.co/ZhengYinan2001/Diffusion-Planner) repository. Download, two files under `checkpoints` directory. 
```bash
mkdir -p checkpoints
wget -P ./checkpoints https://huggingface.co/ZhengYinan2001/Diffusion-Planner/resolve/main/args.json
wget -P ./checkpoints https://huggingface.co/ZhengYinan2001/Diffusion-Planner/resolve/main/model.pth
```
- Run the simulation
1. Set up configuration in sim_diffusion_planner_runner.sh.
2. Run
```bash 
bash sim_diffusion_planner_runner.sh
```
If error: $'\r': command not found
```
sed -i 's/\r$//' sim_diffusion_planner_runner.sh
```
Then re-run the bash command.

- Visualize the results
1. Set up configuration in run_nuboard.ipynb.
2. Launch Jupyter Notebook or JupyterLab to execute run_nuboard.ipynb.




