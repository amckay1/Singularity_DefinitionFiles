# Singularity_DefinitionFiles
Definition files for building Singularity container (https://www.sylabs.io/docs/) that runs DeepLabCut (without GUI!) with Nvidia-GPU support on slurm HPC cluster

## Installation and Usage
1. Pull built container from Singularity Hub () onto login node
2. Request interactive session with gpu support:
```
srun --pty --partition=gpu --gres=gpu:1 --time=05:00:00 $SHELL -l
```
3. Enter container:
```
singularity --nv shell dlc.sif
```
4. Now start python3, import deepcutlab as before, and everything except GUI will be functional with GPU support
