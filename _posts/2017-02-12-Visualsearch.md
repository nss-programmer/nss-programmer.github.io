---
layout: post
comments: true
title: An Image is worth a thousand words
---

   Lets say you are roaming in the heart of the city and just discovered a gorgeous lady walking down the street wearing an outstanding outfit which makes her even looking more beautiful. Now according to you there can be nothing more perfect and more important than that particular outfit which you would definitely like to purchase for your love on her next special occasion. But from where on earth you will search for a similar outfit ? Would you run after the lady and ask her the details of the dress she has worn ? **No way**. Then what should be your immediate step ? **Wait**. You can simply do onething. Take a picture of the lady may be with your mobile phone or a camera whatever you prefer to before she disappears. If your picture is clear enough with less background noise I think you are apparently done. Lets discuss how.
   
![_config.yml]({{ site.baseurl }}/images/visuallady.jpg)
![_config.yml]({{ site.baseurl }}/images/visualladydress.jpg)

   One of the most overlooked aspects of human cognition is vision. When we try to dwelve into the scope of the problem from a computational perspective we realize just how powerful the human brain actually is, going from the real world to a series of neuron activations inorder to recognize and response in the blink of an eye. Now-a-days a large portion of sales in the ecommerce domain is indeed driven by fashion and lifestyle, which constitutes apparel, footwear, bags, accessories and many more. A differentiating characteristic of the fashion category is that a consumer's buying decision is primarily influenced by the product's visual appearance.
So in today's image-driven world its getting more and more difficult to find specific products using a text query. So here comes the concept of **Visual Search**.

   Visual Search allows us to search using an image, against an inventory of hundreds, if not thousands of images and finding an exact match or similar images without the need for textual data such as keywords or metadata in the blink of an eye. It literally stops the keyword guessing game inorder to find image of a particular product. Visual search is altogether different from image search (which returns images for a text-based query) or reverse image search (which often relies on metadata to match results). Visual search derives its result from the supplied image itself.

   Now lets discuss some of the technical aspects of **Visual Search**. The core task here is quantitative estimation of visual similarity between a pair of images. The visual similarity of a pair of images can  be quantitatively estimated through learnt models on top of traditional image processing techniques such as **SIFT** ( **S**cale-**I**nvariant **F**eature **T**ransform ) and **HOG** ( **H**istogram of **O**riented **G**radients ). However these models are limited by the expressive power of these features. In this case **deep convolutional neural networks** stand out to be a better choice. First of all a deep CNN maps a high-dimensional image on to a low dimensional latent space and then makes an attempt to find its neighbors within the latent space.
   
![_config.yml]({{ site.baseurl }}/images/logisticregression.png)
![_config.yml]({{ site.baseurl }}/images/logisticregression.png)
