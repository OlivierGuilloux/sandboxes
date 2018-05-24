# Test pdf2svg on centos 6 and centos 7 #

* pdf2svg : http://www.cityinthesky.co.uk/opensource/pdf2svg/

pdf2svg can crash on centos 6 with big pdf or pdf with images


## Testing ##

Build the images from centos6: `docker build -t pdf2svg:centos6 pdf2svg_centos6`.

Run the test:

```
docker run -m=1G --rm -v $PWD:/shared pdf2svg:centos6 /shared/somefile.pdf /shared/svg/content%d.zvgz all
```

Build the images from centos7: `docker build -t pdf2svg:centos7 pdf2svg_centos7`.


Run the test:
```
docker run -m=1G --rm -v $PWD:/shared pdf2svg:centos7 /shared/somefile.pdf /shared/svg/content%d.zvgz all
```
