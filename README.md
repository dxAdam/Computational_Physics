# Computational Physics
## Introduction
This project is an exploration of how Python can be used to solve problems in physics.  We begin with simple topics like functions and IO and progress to advanced topics like Fourier transforms and Markov chain Monte Carlo simulations. A more complete list of topics is shown below.  
  
Topics: 
1. Electron Energy Levels (Functions & IO)  
2. Plotting Electric Potential (1D, 2D, Scatter, & Contour Plots)  
3. Waves in 2D (Plots, Widgets, Animations)
4. Electric Field of a Charge Distribution (1D & 2D Integration, Quiver Plots)  
5. Eigenfrequencies (Linear Algebra, Drawing & Animating Shapes)
6. Lagrange Points (Minimization/Maximization)  
7. Fourier Transform of Sound (Fourier Transforms)
8. Double Pendulum (Ordinary Differential Equations)
9. Standing Waves on a String (Partial Differential Equations)  
10. Ising Model of Magnetism (Markov Chain Monte Carlo)  
  
The notebook **physics.ipynb** runs in Jupyter Notebook.  

GitHub shows some of the static output of a run notebook but not the widgets or animations (which are the coolest part).  
The **saved_videos** folder contains a few saved video outputs.  
  
## Running the notebook (physics.ipynb) 
### Option 1: Install required packages to your environment    
Installation of Jupyter Notebook, along with Python and the Anaconda Distribution is covered at the [Jupyter website](https://jupyter.readthedocs.io/en/latest/install.html#installing-jupyter-using-anaconda-and-conda).  
### Option 2: Run a container with required packages  
Instead of installing all of these packages to your environment you can instead use **Docker**.  
Docker is a **container** platform. We can use Docker to run a container *containing* all the required packages you will need to run this notebook without affecting your current environment setup.  

First we need to install Docker. This is covered for Windows 10, macOS, and Linux at [the Docker website](https://docs.docker.com/install). If using Ubuntu you can use my [Docker install script](https://github.com/dxAdam/Automation_Scripts/blob/master/install/install_docker.sh).  
 
#### Running the container (Linux) 
Once Docker is installed you can run jupyter/scipy-notebook with  
  
`sudo docker run -p 8888:8888 jupyter/scipy-notebook:17aba6048f44`.  
  
Depending on your internet speed this could take a while. The download size is about 3.4Gb.  
  
When finished the command line output will show you a link containing a token you need to use the first time accessing Jupyter Notebook. Copy the link of form `http://127.0.0.1:8888/?token=<token>` to your browser (the next time you would only need `http://127.0.0.1:8888`).  
  
Next we need to upload the files from this repo into the Jupyter Notebook container. Clone this repo with  
  
`git clone https://github.com/dxadam/Computational_Physics`  
  
and use Jupyter Notebook's upload button to upload physics.ipynb, Starwars.wav, energy_levels.txt, and trumpet.txt.  Then open physics.ipynb.  
  
Finally, to run the notebook you can execute each cell one-by-one using the Run button, or you can execute all cells by selecting Cell->Run All from the menu. To reset use Kernel->Restart. Cells that have run will have a number in square brackets to the left, and those that are still running will have an asterisk. 


#### Remove container and image (Linux)
When finished with jupyter/scipy-notebook click 'Quit' in Jupyter Notebook. You then can remove the container and image from your computer by running  
  
`sudo docker ps`  
  
to find the container ID of the jupyter/scipy-notebook and then removing it with  
  
`sudo docker rm <container ID>`. 
  
If this is the only container you've downloaded you can remove all containers in one step with   
  
`sudo docker rm (sudo ps -a -q)`. 
  
To remove the image run  
  
`sudo docker rmi jupyter/scipy-notebook`.
