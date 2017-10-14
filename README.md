# denseflow
Tensorflow with CV3 + Darkflow

### Build the Docker image locally
```bash
git clone https://github.com/teamsoo/denseflow.git
cd denseflow
```	

**CPU Version**
```bash
docker build -t teamsoo/denseflow:cpu -f Dockerfile.cpu .
```

**GPU Version**
```bash
docker build -t teamsoo/denseflow:gpu -f Dockerfile.gpu .
```
This will build a Docker image named `denseflow` and tagged either `cpu` or `gpu` depending on the tag your specify. Also note that the appropriate `Dockerfile.<architecture>` has to be used.

## Running the Docker image as a Container
Once we've built the image, we have all the frameworks we need installed in it. We can now spin up one or more containers using this image, and you should be ready to [go deeper](http://imgur.com/gallery/BvuWRxq)

**CPU Version**
```bash
docker run -it --name denseflow teamsoo/denseflow:cpu bash
```
	
**GPU Version**
```bash
nvidia-docker run -it --name denseflow teamsoo/denseflow:gpu bash
```
Note the use of `nvidia-docker` rather than just `docker`