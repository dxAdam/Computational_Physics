# Computational Physics
### Introduction
The notebook **physics.ipynb** runs in Jupyter Notebook.  

GitHub shows some of the static output but not the widgets or animations (which are the coolest part).  
The **saved_videos** folder contains a few saved video outputs.  
  
### Running physics.ipynb  
#### Install required packages to your environment    
Installation of Jupyter Notebook, along with Python and the Anaconda Distribution is covered at the __[Jupyter website](https://jupyter.readthedocs.io/en/latest/install.html#installing-jupyter-using-anaconda-and-conda)__ .  
#### Install container with required packages  
Instead of installing all of these packages to your environment you can instead use <strong>Docker</strong>.  
Docker is a <strong>container</strong> platform. We can use Docker to run a container <em>containing</em> all the required packages you will need to run this notebook without affecting your current setup.  

First we need to install Docker. This is covered for Windows 10, macOS, and Linux at [the Docker website](https://docs.docker.com/install). If using Ubuntu you can use my [Docker install script](https://github.com/dxAdam/Automation_Scripts/blob/master/install/install_docker.sh).  
  
Once Docker is installed you can run jupyter/scipy-notebook with  
  
`sudo docker run -p 8888:8888 jupyter/scipy-notebook:17aba6048f44`.

The command line output will show you a link containing a token you need to use the first time. Copy the link with form http://127.0.0.1:8888/?token=<token> into your browser (the next time you would only need http://127.0.0.1:8888).  
  
Next we need to upload the files from this repo into the jupyter notebook container. Clonethis repo with  
  
`git clone https://github.com/dxadam/Computational_Physics`  
  
and use Jupyter's upload button to upload physics.ipynb, Starwars.wav, energy_levels.txt, and trumpet.txt.  Then open physics.ipynb.  
  
Finally, to run the notebook you can execute each cell one-by-one using the play button, or you can ececute all cells by selecting kernel -> restart and run all cells. Cells that have run will have a number in square brackets to their left, and those that are still running will have an asterick.  
