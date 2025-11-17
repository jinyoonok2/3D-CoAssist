# 3D-CoAssist Environment Setup

Quick setup guide for the 3D-CoAssist development environment with Habitat-Lab.

## Prerequisites

- Conda (Miniconda or Anaconda)
- Git

## Quick Start

### First-time Setup

Run the setup script to create the environment and install all dependencies:

```bash
./setup
```

This will:
- Create a conda environment named `3d-coassist` with Python 3.9
- Install habitat-sim, habitat-lab, and habitat-baselines
- Clone the habitat-lab repository (stable branch)

### Activate Environment

After setup, activate the environment with:

```bash
source ./activate
```

Or manually with conda:

```bash
conda activate 3d-coassist
```

## Additional Commands

### Reset and Reinstall

If you need to start over and reinstall everything:

```bash
./setup --reset
```

This will remove the existing environment and perform a clean installation.

### Checking Environment

To verify the installation:

```bash
source ./activate
python -c "import habitat; print(habitat.__version__)"
```

## What Gets Installed

- **Python 3.9** with CMake 3.14.0
- **habitat-sim** (stable version from conda-forge)
- **Pillow 10.4.0** (for compatibility)
- **habitat-lab** (from GitHub stable branch, editable install)
- **habitat-baselines** (editable install)

## Troubleshooting

If the setup fails:
1. Ensure conda is properly initialized in your shell
2. Check that you have sufficient disk space
3. Try running `./setup --reset` to start fresh

For more details, see the [Habitat-Lab documentation](https://github.com/facebookresearch/habitat-lab).
