# Img2Url-API

API for image hosting eg. img2url.site

# Install:
pip install Img2UrlApi  
You need to install also: PILLOW and requests   

# Example:
###  import ###
from PIL import Image
import requests

from Img2UrlApi.ImgUploader   
import ImgUploader

### init ###
url = "http://img2url.site"     
user_key = "GwAwetQ90EnhoorB6wDaV0hjb9o"        
sec_key = "qqq"     
img_uploader = ImgUploader(url, user_key, sec_key)      

### upload ###
id = img_uploader.post_image("test.jpg")
print(id)

### get ###
img = img_uploader.get_image(107)       
print(img)

### get all ###
imgs = img_uploader.get_images()     
print(imgs)

### remove ###
print(img_uploader.remove_image(109))

### removel all ###
print(img_uploader.remove_all())



