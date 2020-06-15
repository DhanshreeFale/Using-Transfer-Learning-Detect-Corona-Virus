# Using-Transfer-Learning-to-detect-corona-Virus
<!-- wp:heading {"level":4} -->
<h4>Data Preparation</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In this project data is taken from the Guangzhou Women and Children’s Medical Center and kaggle, which consist of 219 images of corona infected lungs X-ray and 1341 images of normal lungs X-ray. The data is split into training set and testing set manually in separate folder. For training set I took 75% of total data and remaining 25% for testing set. </p>
<!-- /wp:paragraph -->
<!-- wp:image {"id":438,"sizeSlug":"large"} -->
<figure class="wp-block-image size-large"><img src="https://capablemachine.files.wordpress.com/2020/05/image-79.png?w=507" alt="" class="wp-image-438"/><figcaption>X-Ray</figcaption></figure>
<!-- /wp:image -->
Transfer learning is a process that allows us to use knowledge obtained from other tasks.
<!-- wp:image {"id":426,"width":537,"height":256,"sizeSlug":"large"} -->
<figure class="wp-block-image size-large is-resized"><img src="https://capablemachine.files.wordpress.com/2020/05/image-75.png?w=773" alt="" class="wp-image-426" width="537" height="256"/></figure>
<!-- /wp:image -->
I employed four different pre-trained model, VGG16, Inception-v3,  ResNet-18, GoogLeNet. 
<!-- wp:heading {"level":4} -->
<h4>Results</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The primary goal of our transferring learning approach was to correctly diagnose COVID-19 among normal chest X-ray images. For this I prepared all of the models as Mention above and trained them separately.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For training, I used the Adam optimizer and the cross-entropy loss function. The learning rate is started from the value of 0.001 and is reduced by 2 after every three epochs. Inception V3 was trained for 10 iterations at learning rate of 0.001 and then trained at very low learning rate of 0.00001. it achieved a test accuracy of 87.5% and a train accuracy of 97.5%, which lead to little overfitting. VGG16 did better than Inception V3 and other models; it achieved train accuracy of 99.87% and test accuracy of 99.73%.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>figure shows plots of accuracy against epochs. The best results were obtained by the VGG16 network and worst by the Inception V3 in terms of accuracy.</p>
<!-- /wp:paragraph -->
