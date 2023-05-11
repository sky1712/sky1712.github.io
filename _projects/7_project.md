---
layout: page
title: project 5
description: a project with a background image
img: assets/img/1.jpg
importance: 3
category: fun
---
# K-Means for image compression and segmentation

## Introduction

In this project, I implemented the K-Means algorithm for image compression and segmentation. The K-Means algorithm is a clustering algorithm that is used to group similar data points together. The algorithm works by randomly initializing K cluster centroids and then iteratively updating the centroids until the algorithm converges. The algorithm is guaranteed to converge, but it may converge to a local minimum. The algorithm is as follows:

1. Randomly initialize K cluster centroids
2. Repeat until convergence:
    1. For each data point, assign it to the closest cluster centroid
    2. For each cluster centroid, update the centroid to be the mean of all the data points assigned to it


## Image Compression

The K-Means algorithm can be used to compress an image by reducing the number of colors in the image. The algorithm works by treating each pixel in the image as a data point in a 3-dimensional space (one dimension for each color channel). The algorithm then clusters the pixels into K clusters and replaces each pixel with the centroid of the cluster it belongs to. The algorithm is as follows:

1. Treat each pixel in the image as a data point in a 3-dimensional space
2. Run the K-Means algorithm on the data points
3. For each pixel in the image, replace it with the centroid of the cluster it belongs to

The algorithm is guaranteed to converge, but it may converge to a local minimum. To avoid this, the algorithm is run multiple times with different initializations and the best result is chosen.

The algorithm is implemented in the `kmeans_compress` function in `kmeans.py`. The function takes in an image and the number of clusters to use and returns the compressed image. The function uses the `kmeans` function from `kmeans.py` to run the K-Means algorithm on the data points. The function then loops through each pixel in the image and replaces it with the centroid of the cluster it belongs to. The function returns the compressed image.

The algorithm is run on the `peppers.png` image with 16 clusters. The original image is shown below:

![peppers](assets/img/peppers.png)

The compressed image is shown below:

![peppers_compressed](assets/img/peppers_compressed.png)


## Image Segmentation

The K-Means algorithm can also be used to segment an image by grouping similar pixels together. The algorithm works by treating each pixel in the image as a data point in a 5-dimensional space (one dimension for each color channel and one dimension for the x and y coordinates). The algorithm then clusters the pixels into K clusters and replaces each pixel with the centroid of the cluster it belongs to. The algorithm is as follows:

1. Treat each pixel in the image as a data point in a 5-dimensional space
2. Run the K-Means algorithm on the data points
3. For each pixel in the image, replace it with the centroid of the cluster it belongs to

The algorithm is guaranteed to converge, but it may converge to a local minimum. To avoid this, the algorithm is run multiple times with different initializations and the best result is chosen.

The algorithm is implemented in the `kmeans_segment` function in `kmeans.py`. The function takes in an image and the number of clusters to use and returns the segmented image. The function uses the `kmeans` function from `kmeans.py` to run the K-Means algorithm on the data points. The function then loops through each pixel in the image and replaces it with the centroid of the cluster it belongs to. The function returns the segmented image.

The algorithm is run on the `peppers.png` image with 16 clusters. The original image is shown below:

![peppers](assets/img/peppers.png)

The segmented image is shown below:

![peppers_segmented](assets/img/peppers_segmented.png)


## Conclusion

In this project, I implemented the K-Means algorithm for image compression and segmentation. The K-Means algorithm is a clustering algorithm that is used to group similar data points together. The algorithm works by randomly initializing K cluster centroids and then iteratively updating the centroids until the algorithm converges. The algorithm is guaranteed to converge, but it may converge to a local minimum. The algorithm can be used to compress an image by reducing the number of colors in the image. The algorithm can also be used to segment an image by grouping similar pixels together. The algorithm is implemented in the `kmeans_compress` and `kmeans_segment` functions in `kmeans.py`. The functions take in an image and the number of clusters to use and return the compressed or segmented image. The functions use the `kmeans` function from `kmeans.py` to run the K-Means algorithm on the data points. The functions then loop through each pixel in the image and replace it with the centroid of the cluster it belongs to. The functions return the compressed or segmented image.

## References

- [K-Means Clustering](https://en.wikipedia.org/wiki/K-means_clustering)
- [K-Means Clustering Algorithm](https://www.geeksforgeeks.org/k-means-clustering-introduction/)

## Source Code




Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
