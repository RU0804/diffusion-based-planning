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



