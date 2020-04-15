---
layout: post
title: Introduction to Machine Learning
author: Md. Jahid Hasan
date: '2020-04-12 01:05:23 +0600'
category: guides
summary: 𝐓𝐡𝐞 𝐌𝐚𝐜𝐡𝐢𝐧𝐞 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐋𝐚𝐧𝐝𝐬𝐜𝐚𝐩𝐞
---




principal component analysis(PCA) বহুল ব্যবহিত Dimensionality Reduction Algorithm.
PCA মুলত একটি ডাটাসেটে ডাটাগুলোর  Orthogonal Projection ( লম্ব অভিক্ষেপ)  খুজে বের করে। Orthogonal projection এর মাধ্যমে PCA ডাটাসেটের সরবচ্ছ Variance খুজে বের করে, জার সাহায্য ডাটাসেট এবং Feature মধ্যে linear-corelation বের করা জাই!।

আরথাত,  আমাদের কাছে জদি একটি নিদিশত দাতাসএতের  linearlg corelated কিছু ফিচার থাকে  তাইলে PCA একটা suitability  orthogonal direction খুজে বের করতে পারবে জা আমদেএ দাতাসের এর সমসস্ত দাতা কে এক্তা direction এ তুলে ধরতে পারবে।

PCA  কতগুলি principal component  নিয়ে গঠিত,  চলুন Principal component কি দেখে নেয়

Principal component :
Principal component হলো Initial Variable ( Raw dataset)  থেকে স্রস্ত Linear combination or mixure এর মাধ্যমে একটি New Variable( New Dataset).  

New Variable টি কতগুল Principal component  নিয়ে গতিত। Principal component এক বা একাধিক হতে পারে।  অরথাত একটি ডাতাসেতের ডিমেনশন জদি ১০০ হঅই তিবে তার principal component hobe 100তি। Principal component গুল দাতার ইনফরমেশন এর উপরে ভিত্তি করে নিম্নক্ত বিনাস আকারে সাজানো থাকে
.............

New variable টি totally uncorrelated হয়ে থাকে এবং Initail variable এর অধিকাংশ ইনফরমেশন compressed হয়ে 1st pricipal component create kore thake.

PCA try করে অধিকাংশ নিরভর ইনফরমেশন
1st principal component এ রাখার তারপর অবশিষ্ট অধিকাংশ ইনফরমেশন  2nd principal component এ রাখার এবং এইভাবে ইনফরমেশন এর উপরে ভিত্তি করে principal component এর বিনাস create হয়ে থাকে। নিম্নে ছিত্রে দেখানো হলো।
picture here......

উপরিউক্ত বিন্নাস(higher information to lower information)  আকারে principal components গুলা সাজিয়ে খুব সহজে আমরা কম ইনফরমেশন নষ্ট করে একটি Lower dimensional Dataset( new Dataset) create hoi.

সুতরাং, এইভাবে lower information principal component বাদ দিয়ে অবশিস্ট principal component নিয়ে initail varaiable(Raw Dataset)  থেকে new Variable ( new Dataset)
create hoye thake.

Example :
আমরা জানি একটা দাতাসেত এর dimension jodi 100D hoye tobe tar principal component o hobe 100ti.  PCA jokhon dimension reduction kore tokhon low variance feature ke bad diye higher dimension theke lower dimension dataset create kore thake.. Orthat optimal principal component khuje ber korar jonno PCA sob somoi low information feature or low variance data ke noise hisabe bibecona kore. Ei noise feature gula PCA bad diye ekta notun dataset create kore thake jar dimension hoii Main dataset er dimension theke onkk kom ( deoend on infomation gather by each princiapl component).

Dhoren main datasert er name A.  A datser er dimension hosce 100D ebong er principal component o 100ti. 100 ti principal component er mjhee 1st 20 principal component  e 95% data information hold kore.

PCA tokhon 21-100 porjonto dimension er data ke noise hisabe bibchone kore ogula reomve kore dibe. Baki 20 principle component niye ekta new Dataset create kore B.

sutrang PCA apply kore, B dataset ti A dataset  95% information hold kore,  higher dimensional dataset (A: 100 dimension)  theke lower dimensional dataset( B : 20 dimension)  create korbe.

Note ::
Dekha gese noise feature or low variance  data gula suoervied
