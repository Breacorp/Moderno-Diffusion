## How to run Moderno Diffusion from source 

Install the following:
- Miniforge / Conda
- Nodejs (v16 - v18)

Create the conda environment and activate it:

```
conda create -n moderno_diffusion_env python=3.9.10
conda activate moderno_diffusion_env
```

Install the python packages:

```
cd backends/stable_diffusion
pip install -r requirements.txt
```

Install the npm packages:

```
cd electron_app
npm install
```

Run the app:

```
npm run electron:serve
```

```