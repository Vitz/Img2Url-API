# Img2Url-API
API for image hosting eg. www.img2url.site
Its free, just register to get a  api key. 
Just remember it's an aplication to change your image into url link.  Don't use it as a permanent hosting. There is no any guarantee images will be stored.

I have made the app because I needed to change many images from disk into csv file (Woocomerce products) to upload products from csv files.  


# Install:
pip install Img2UrlApi  
You need to install also: PILLOW and requests   

# Example:
###  import ###
from PIL import Image   
import requests

from Img2UrlApi.ImgUploader import ImgUploader

### init ###
url = "http://img2url.site"     
user_key = "GwAwetQ90EnhoorB6wDaV0hjb9o"        
sec_key = "qqq"     
img_uploader = ImgUploader(url, user_key, sec_key)      

### upload ###
print(img_uploader.post_image("test.jpg"))

### get ###
print(img_uploader.get_image(107) )

### get all ###
print(img_uploader.get_images())

### remove ###
print(img_uploader.remove_image(109))

### removel all ###
print(img_uploader.remove_all())



