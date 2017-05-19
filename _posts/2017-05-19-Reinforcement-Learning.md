---
layout: post
title: "Reinforcement Learning - ခ်ယ္ရီခူးျခင္း"
description: "Reinforcement Learning မိတ္ဆက္"
date: 2017-05-19
tags: [Reinforcement Learning]
comments: true
share: true
---


## Contents
* မိတ္ဆက္  
* Reinforcement Learning အသံုးျပဳပံုတစ္ခ်ိဳ  
* Natural Language Processing မွာ RL ကိုအသံုးျပဳပံု  
* RL ရဲ့အစိတ္အပိုင္းမ်ား  
* Exploration Vs Exploitation  
* Supervised Learning နဲ့ဘာကြာသလဲ ??    
* ေခါင္းစဥ္ကို ဘာလို့ ခ်ယ္ရီခူးျခင္းလို့ ေပးထားတာလဲ ??  
* Reinforcement Learning ကိုဘယ္လိုေလ့လာရမလဲ ??
{:toc}

## မိတ္ဆက္  
**Machine Learning** မွာ **Supervised Learning၊ Unsupervised Learning နဲ့ Reinforcement Learning** ဆိုုျပီး ၃မ်ိဳးခြဲလို့ရပါတယ္။ ဒီ Post မွာ အဓိကေျပာခ်င္တာက Reinforcement Learning ပါ။ 

**Supervised Learning** ကေတာ့ Data Science and Analytics လုပ္တဲ့လူေတြနဲ့အရင္းႏွီးဆံုးျဖစ္မွာပါ။ Supervised Learning က လြယ္လြယ္ေျပာရရင္ ကိုယ့္မွာရွိတဲ့ Labeled Data ကိုၾကည့္ျပီးေတာ့ ဒီ Input မ်ိဳးဆိုရင္ ဘယ္လို Output Label မ်ိဳးထုတ္ေပးရမလဲဆိုတာကိုု ကြန္ျပဴတာကိုသင္ခိုင္းတာပါ(Training)။ ဥပမာ ကြန္ျပဴတာကို ပန္းသီးပံုေတြအမ်ားၾကီးျပျပီး တျခား မျမင္ဖူးေသးတဲ့ပန္းသီးပံုေတြလာရင္ ပန္းသီးလို့ခန့္မွန္းတတ္ေအာင္သင္ေပးတာမ်ိဳးပါ။

**Unsupervised Learning** ကေတာ့ Label ရယ္လို့မရွိဘူး။ ဒီ Input ေပးရင္ ဒီလို Output ထုတ္ေပးရမယ္ဆိုျပီး သတ္သတ္မွတ္မွတ္မရွိဘူး။ Clustering က Unsupervised Learning တစ္မ်ိဳးပါပဲ။ အလြယ္ဆံုး ဥပမာေပးရရင္ ေၾကာင္ပံုေတြနဲ့ေခြးပံုေတြ အမ်ားၾကီးကို ကြန္ျပဴတာထဲထည့္ေပးျပီး ကြန္ျပဴတာကို အုပ္စု၂ခု (or ၃ခု) ခြဲတတ္ေအာင္ သင္ေပးတာပါ။ သူ ့ကိုု ဘယ္ပံုကေၾကာင္ ဘယ္ပံုကေခြးဆိုျပီး Label တပ္ေပးျပီး supervise ေပးစရာမလိုုဘူး။ သူ့ဘာသူၾကည့္ျပီး ဒီေကာင္ေလးေတြကရုပ္ဆင္တယ္ တစ္အုပ္စုေနဆိုျပီး အစုခြဲလိုက္တာမ်ိဳး။ 

**Reinforcement Learning** ကေတာ့ Agent ကိုအျပင္ေလာက (Environment) နဲ့ ထိေတြ့ခိုင္းျပီး Environment ကျပန္ေပးတဲ့ Feedback အေပၚမူတည္ျပီး ဒီလိုအေျခအေနမ်ိဳးဆိုဘာ Action လုပ္သင့္တယ္ဆိုျပီးသင္တာပါ။ ဆုေပး ဒဏ္ေပးစနစ္မ်ိဳးလို့လဲ  ယူဆႏိုင္ပါတယ္။ ဥပမာ - Robot ကို လမ္းေလွ်ာက္ရင္းနံရံရွိတဲ့ဆီကိုဝင္တိုက္ရင္ ဒဏ္ေပးမယ္၊ ဝင္မတိုက္ဘဲ ေဘးကိုု ေကြ့သြားရင္ဆုေပးမယ္။ အဲလိုနဲ့ သူက ေရရွည္မွာ ဆုမ်ားမ်ားရတဲ့ Action ေတြလုပ္တတ္ေအာင္သင္ယူသြားတာမ်ိဳးပါ။ ***အေရးအၾကီးဆံုးက ေရရွည္မွာဆုအမ်ားဆံုးရဖို့ျဖစ္တယ္။*** အဲဒီအတြက္ တစ္ခါတစ္ေလမွာ လက္ငင္းရႏိုင္တဲ့ဆုအေသးေလးေတြကိုု စြန့္လႊတ္ျပီး ဒီထက္ပိုုၾကီးတဲ့ အနာဂတ္ဆုုလာဒ္ေတြကို ေစာင့္တတ္ဖို့လဲလိုတယ္။ ဥပမာ စစ္တုရင္ကစားရင္ ကိုယ့္အေရွ့မွာ အေကာင္အေသးေလးေတြ စားလို့ရတာရွိလိမ့္မယ္။ အဲလိုစားလိုုက္ရင္ ဆုရလိမ့္မယ္။ ဒါေပမယ့္ စားလိုက္ရင္ ေရရွည္မွာေကာင္းခ်င္မွ ေကာင္းမယ္။ ဟိုဘက္က Strategy အရ သူတို့အေကာင္အၾကီးေတြေရြႊ့ဖို့ အေကာင္အေသး Pawnေတြကိုတမင္ခ်ေၾကြးထားတာလည္းျဖစ္ႏိုင္တယ္။ ဒါေၾကာင့္ **Immediate Reward** (လက္ငင္းဆု) ထက္ **Cumulative Reward အမ်ားဆံုးရမယ့္ Action** ေတြလုပ္တတ္ေအာင္ သင္ယူရပါမယ္။ ဒါကေတာ့ Reinforcement Learning ရဲ့အေျခခံ သေဘာတရားပါ။ 

{To Be Continued}

## Reinforcement Learning အသံုးျပဳပံုတစ္ခ်ိဳ့    
{To Be Continued}  

## Natural Language Processing မွာ RL ကိုအသံုးျပဳပံု  
{To Be Continued}  

## RL ရဲ့အစိတ္အပိုင္းမ်ား  
{To Be Continued}  

## Exploration Vs Exploitation  
{To Be Continued}  


## Supervised Learning နဲ့ဘာကြာသလဲ ??  
{To Be Continued}  


## ေခါင္းစဥ္ကို ဘာလို့ ခ်ယ္ရီခူးျခင္းလို့ ေပးထားတာလဲ ??  
{To Be Continued}  


## Reinforcement Learning ကိုဘယ္လိုေလ့လာရမလဲ ??
 * David Silver’s Reinforcement Learning Lectures [[Videos](https://youtu.be/2pWv7GOvuf0?list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT)][[Notes](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)]
* [Textbook: Reinforcement Learning: An Introduction ](http://people.inf.elte.hu/lorincz/Files/RL_2006/SuttonBook.pdf)
 