#### Docker image build
```
docker build -t devopsworkslab/intelli-simple-webapp .
```
#### Docker push image
```
docker push devopsworkslab/intelli-simple-webapp
```
#### Docker run container
```
docker run --rm -d -p 90:80 devopsworkslab/intelli-simple-webapp
```