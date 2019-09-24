# Inspiring Depiction
              ![Christina's World](https://upload.wikimedia.org/wikipedia/en/a/a2/Christinasworld.jpg)

We were inspired by artists that have shaped our view on reality. From Van Gough to Dali, we wondered what Davinci would paint if he were living in our current time period. To experiment and experience what their pieces may appear as in our day and age, we created a style transfer based off of a [colab neural style transfer.](https://colab.research.google.com/github/tensorflow/models/blob/master/research/nst_blogpost/4_Neural_Style_Transfer_with_Eager_Execution.ipynb)

We used the base code and built up to a user interface. Our focus was on understanding the fundamentals of machine learning and create a fun application that would connect classical art with modern day snapshots. 

## Application

### Scraping
We scraped for the most [influential artists](http://www.theartwolf.com/articles/most-important-painters.htm) and fed the names into an [image site](https://www.wikiart.org/en/) which allowed us to extract famous pieces. 

We debated placing the data into a database, such as MongoDB, but ultimately decided to leave the data in a csv form.

### Back End
For our backend, we used python to load in our two images, an image with the desired style (style image) and an image that the style would be applied to (content image). From there, the content image would be copied (input image), keras and tensorflow would be used to extract the styles from the style image and applied to the input image. The increase in iterations would ultimately increase the style quality transferred, but also increase the time investment. 

As the iterations increased, the image comparison of the input against the style would decrease in variance, ultimately reaching a point that the visual depiction would be the content with the desired style.

### Framework
We used flask to connect our back end and front end. In flask, we created mutliple routes that would allow for separate webpages displaying past processed images and even a gif showing the style transformation of the content. 

### Front End
For the front end, we coded multiple HTML pages and styled using CSS with [bootstrap.](https://colab.research.google.com/github/tensorflow/models/blob/master/research/nst_blogpost/4_Neural_Style_Transfer_with_Eager_Execution.ipynb) Using JavaScript, we created an interactive user interface that allowed for image uploads, downloads, and quality selection. For the quality selection, we increased or lowered our iterations accordingly.

![](https://upload.wikimedia.org/wikipedia/commons/8/81/Edgar_Degas_-_The_Ballet_Class_-_Google_Art_Project.jpg)
