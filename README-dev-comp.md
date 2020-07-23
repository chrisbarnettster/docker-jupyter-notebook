
# For local testing:

include this in startup.sh
jupyter notebook --no-browser --allow-root

mkdir import and include a volume flag
mkdir import
cp ipython_galaxy_notebook.ipynb import
LOCAL_PATH=`pwd`/import
docker run -p 7777:8888 -v $LOCAL_PATH:/import -i -t jupyter-notebook

# ideas
## Compchem envs
- [ ] make comp environments. A multienv - but that may not work. So start with one usecase based way and example notebook
  - [ ] View and select traj's
    - [ ] mdanalysis and nglview
    - [ ] mdtraj
    - [ ] vmd
    - pytraj
  - [ ] Run a short OpenMM calc
    - [ ] omnia
  - Test Free energy tools?
    - [ ] free energy
  - [ ] cheminformatics and tox with rdkit
  - Convert parameters with greater flexibility
    - parmed

## jupyterlab
Also try localhost:7777/ipython/lab not just /ipython

- [ ] make a popup welcome work in jupyterlab - see jupyterlab_enkiintro on gitlab.com



# Issues

- trying to conda activate in the notebook gives that annoying conda init error. Also ipykernels should work.... 
  - fixed with ipykernel and nb_conda_kernels
