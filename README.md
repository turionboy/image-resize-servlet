# Imagemagick resize servlet example 
Super simple example for using imagemagick (http://www.imagemagick.org/) from within a servlet. The servlet will resize an already existing original 
image to one of the predefined desired sizes (or whatever size you want, depending on configuration).

# What you need
1. Imagemagick needs to be installed and the user of the servlet engine needs to have it on the path
2. Simple as that :)

# How to use it
1. Setup the servlet in your web.xml (you can configure the request parameter name, original image folder, thumbnail base folder and a list of valid sizes of images)

2. Access the servlet with the your predefined request parameter with the value of the image you want.

```
/SERVLET/?img=MY_ORIGINAL_IMAGE-120x94.png
```

The servlet will check if the image already exist, if the file exists, it is forwarded to the user. Else the servlet checks if the 
original image exist (named MY_ORIGINAL_IMAGE.png). If it does and the size 120x94 exists in the list of valid sizes (or all sizes are ok), 
it will be created used imagemagick, and returned to the user.

Default tomcat is setup using https://github.com/jsimone/webapp-runner, please checkit it out for how to start tomcat etc.

