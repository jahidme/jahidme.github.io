---
layout: post
title: Analogy of Generative Adversarial Network(GAN)
author: Md. Jahid Hasan
date: '2020-04-14 09:15:23 +0600'
category: GAN
summary: Generative Adversarial Network(GAN)
thumbnail: gan_analogy01.png
---


👉Part : 01
> ✍ Topic : Generative Adversarial Network(GAN)


<h2> <b>  <center> Analogy </center>  </b> </h2>

<p>The easiest way to understand what GANs are is through a simple analogy:</p>

<p>Suppose there is a shop which buys certain kinds of wine from customers which they will later resell.</p>

<figure>
			 <img src="/assets/img/blog/gan_analogy/1.png"  width="360" alt="gan">
</figure>

<p>  
However, there are nefarious customers who sell fake wine in order to get money. In this case, the shop owner has to be able to distinguish between the fake and authentic wines.

</p>

<figure>
			 <img src="/assets/img/blog/gan_analogy/2.png"  width="360" alt="gan">
</figure>

<p>  
You can imagine that initially, the forger might make a lot of mistakes when trying to sell the fake wine and it will be easy for the shop owner to identify that the wine is not authentic. Because of these failures, the forger will keep on trying different techniques to simulate the authentic wines and some will eventually be successful. Now that the forger knows that certain techniques got past the shop owner's checks, he can start to further improve the fake wines based on those techniques.</p>
<p>
At the same time, the shop owner would probably get some feedback from other shop owners or wine experts that some of the wines that she has are not original. This means that the shop owner would have to improve how she determines whether a wine is fake or authentic. The goal of the forger is to create wines that are indistinguishable from the authentic ones, and the goal of the shop owner is to accurately tell if a wine is real or not.
</p>

<h4> 👉 Components of a Generative Adversarial Network </h4>

<p>
Using the example above, we can come up with the architecture of a GAN.
<p>

<figure>
			 <img src="/assets/img/blog/gan_analogy/3.png"  width="360" alt="gan">
</figure>

<p>  
There are two major components within GANs: the generator and the discriminator. The shop owner in the example is known as a discriminator network and is usually a convolutional neural network (since GANs are mainly used for image tasks) which assigns a probability that the image is real.
</p>

<p>
The forger is known as the generative network, and is also typically a convolutional neural network (with deconvolution layers). This network takes some noise vector and outputs an image. When training the generative network, it learns which areas of the image to improve/change so that the discriminator would have a harder time differentiating its generated images from the real ones.
</p>

<p>
The generative network keeps producing images that are closer in appearance to the real images while the discriminative network is trying to determine the differences between real and fake images. The ultimate goal is to have a generative network that can produce images which are indistinguishable from the real ones.
</p>


<h2> <b>  <center> Another Analogy </center>  </b> </h2>

<p>  
You can think of a GAN as the opposition of a counterfeiter and a cop in a game of cat and mouse, where the counterfeiter is learning to pass false notes, and the cop is learning to detect them. Both are dynamic; i.e. the cop is in training, too (to extend the analogy, maybe the central bank is flagging bills that slipped through), and each side comes to learn the other’s methods in a constant escalation.
</p>




<p>
The key intuition of GAN can be easily considered as analogous to art
forgery, which is the process of creating works of art (https://en.wikipedia.org
/wiki/Art) that are falsely credited to other, usually more famous, artists.
GANs train two neural nets simultaneously, as shown in the next diagram.
The generator G(Z) makes the forgery, and the discriminator D(Y) can judge
how realistic the reproductions based on its observations of authentic pieces
of arts and copies are. D(Y) takes an input, Y, (for instance, an image) and
expresses a vote to judge how real the input is--in general, a value close to
zero denotes real and a value close to one denotes forgery. G(Z) takes an
input from a random noise, Z, and trains itself to fool D into thinking that
whatever G(Z) produces is real. </p>

<figure>
			 <img src="/assets/img/blog/gan_analogy/4.png"  width="360" alt="gan">
</figure>


<p>
 So, the goal of training the discriminator D(Y) is to maximize D(Y) for every image from the true data
distribution, and to minimize D(Y) for every image not from the true data
distribution. So, G and D play an opposite game; hence the name adversarial
training. Note that we train G and D in an alternating manner, where each of
their objectives is expressed as a loss function optimized via a gradient
descent. The generative model learns how to forge more successfully, and the
discriminative model learns how to recognize forgery more successfully. The
discriminator network (usually a standard convolutional neural network) tries
to classify whether an input image is real or generated. The important new
idea is to backpropagate through both the discriminator and the generator to
adjust the generator's parameters in such a way that the generator can learn
how to fool the the discriminator for an increasing number of situations. At
the end, the generator will learn how to produce forged images that are
indistinguishable from real ones:

</p>

<p>
Of course, GANs require finding the equilibrium in a game with two players.
For effective learning it is required that if a player successfully moves
downhill in a round of updates, the same update must move the other player
downhill too. Think about it! If the forger learns how to fool the judge on
every occasion, then the forger himself has nothing more to learn. Sometimes
the two players eventually reach an equilibrium, but this is not always
guaranteed and the two players can continue playing for a long time.
</p>


<h2>👉 Learn more about GAN network and algorithm here. </h2>
<p> </p>
<br>
<a style= "border-radius: 4px;
						background-color: #f4511e;
						border: none;
						color: #FFFFFF;
						text-align: center;
						font-size: 30px;
						padding: 15px;
						width: 100px;
						transition: all 0.5s;
						cursor: pointer;
						margin: 5px;
						text-decoration: none"

					href="https://jahidme.github.io/deep%20learning,%20cnn,%20gan/2020/04/11/gan-intro/#/" >Read</a>
<p>  </p>
<br>
<h2>👉 Application of GAN</h2>


<h3>GAN applications into the following areas:</h3>
<ul>
    <li>Generate Examples for Image Datasets</li>
		<li>Semantic-Image-to-Photo Translation</li>
    <li>Generate Photographs of Human Faces</li>
    <li>Generate Realistic Photographs</li>
	  <li>Face Frontal View Generation</li>
		<li>Generate Cartoon Characters</li>
		<li>Image-to-Image Translation</li>
		<li>Text-to-Image Translation</li>
		<li>Generate New Human Poses</li>
		<li>3D Object Generation</li>
		<li>Clothing Translation</li>
		<li>Photograph Editing</li>
    <li>Video Prediction</li>
    <li>Photos to Emojis</li>
    <li>Photo Inpainting</li>
		<li>Super Resolution</li>
		<li>Photo Blending</li>
    <li>Face Aging</li>
</ul>

<br>

<h2>👉 Problem of GAN</h2>

<p> GANs have a number of common failure modes. All of these common problems are areas of active research. While none of these problems have been completely solved, we'll mention some things that people have tried.<p>
<ul>
    <li><p> <b><u>None convergence:  </u></b> The model parameter oscillate, destabilize and never converge. Cost function may not converge by using gradient descent in a common minimize game. <p>
    <li><p> <b><u>Model Collapse:  </u></b> The gradient collapse which produce limited varieties of sample. <p>
    <li><p> <b><u>Diminished gradient:  </u></b> The discriminator gets too successful that the generator gradient vanished and learns nothing. <p>
    <li>Unbalanced between generator and discriminator causing overfitting</li>
    <li>Highly sensitive to select hyperparamter</li>
    <li>Text-to-Image Translation</li>



<hr>
<br>
<br>

<h3>Reference:</h3>
<ul>
		    <li>https://www.datacamp.com/community/tutorials/generative-adversarial-networks</li>
				<li>https://pathmind.com/wiki/generative-adversarial-network-gan</li>


</ul>
