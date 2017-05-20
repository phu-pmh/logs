---
layout: post
title: "Reinforcement Learning မိတ္ဆက္"
description: "Reinforcement Learning အက်ဥ္းခ်ဳပ္ မိတ္ဆက္"
date: 2017-05-19
tags: [Reinforcement Learning]
comments: true
share: true
---


**Contents**
* မိတ္ဆက္  
* Some Applications of Reinforcement Learning 
* Natural Language Processing မွာ RL ကိုအသံုးျပဳပံု  
* RL ရဲ့အစိတ္အပိုင္းမ်ား  
* Exploration Vs Exploitation  
* Supervised Learning နဲ့ဘာကြာသလဲ ??    
* Reinforcement Learning ကိုဘယ္လိုေလ့လာရမလဲ ??
{:toc}

## မိတ္ဆက္  
**Machine Learning** မွာ **Supervised Learning၊ Unsupervised Learning နဲ့ Reinforcement Learning** ဆိုုျပီး ၃မ်ိဳးခြဲလို့ရပါတယ္။ ဒီ Post မွာ အဓိကေျပာခ်င္တာက Reinforcement Learning ပါ။ 

**Supervised Learning** ကေတာ့ Data Science and Analyticsလုပ္တဲ့ လူေတြနဲ့ အရင္းႏွီးဆံုး ျဖစ္မွာပါ။ Supervised Learning က လြယ္လြယ္ေျပာရရင္ ကိုယ့္မွာရွိတဲ့ Labeled Data ကိုၾကည့္ျပီးေတာ့ ဒီ Input မ်ိဳးဆိုရင္ ဘယ္လို Output Label မ်ိဳးထုတ္ေပးရမလဲဆိုတာကိုု ကြန္ျပဴတာကိုသင္ခိုင္းတာပါ(Training)။ ဥပမာ ကြန္ျပဴတာကို ပန္းသီးပံုေတြအမ်ားၾကီးျပျပီး ဒါပန္းသီး ဒါပန္းသီးဆိုျပီးသင္ေပးမယ္။ တျခား မျမင္ဖူးေသးတဲ့ပန္းသီးပံုေတြလာရင္ ပန္းသီးလို့ခန့္မွန္းတတ္ေအာင္ သင္ေပးတာမ်ိဳးပါ။

**Unsupervised Learning** ကေတာ့ Label ရယ္လို့မရွိဘူး။ ဒီ Input ေပးရင္ ဒီလို Label မ်ိဳးထုတ္ေပးရမယ္ဆိုျပီး သတ္သတ္မွတ္မွတ္ သင္မေပးဘူး။ Clustering က Unsupervised Learning တစ္မ်ိဳးပါပဲ။ အလြယ္ဆံုး ဥပမာေပးရရင္ ေၾကာင္ပံုေတြနဲ့ေခြးပံုေတြ အမ်ားၾကီးကို ကြန္ျပဴတာထဲထည့္ေပးျပီး ကြန္ျပဴတာကို အုပ္စု၂ခု (or ၃ခု) ခြဲတတ္ေအာင္ သင္ေပးတာပါ။ သူ ့ကို ပံုေတြျပျပီး ဒါကေၾကာင္ ဒါကေခြးဆိုျပီး Label တပ္ေပးျပီး supervise ေပးစရာမလိုုဘူး။ သူ့ဘာသူၾကည့္ျပီး ဒီေကာင္ေလးေတြကရုပ္ဆင္တယ္ တစ္အုပ္စုေနဆိုျပီး အစုခြဲလိုက္တာမ်ိဳး။ 

**Reinforcement Learning** ကေတာ့ Goal-directed Agentကို အျပင္ေလာက(Environment)နဲ့ ထိေတြ့ခိုင္းျပီး Environmentကျပန္ေပးတဲ့ Feedbackအေပၚမူတည္ျပီး ဒီလိုအေျခအေနမ်ိဳးဆို ဘာActionလုပ္သင့္တယ္ဆိုျပီးသင္တာပါ။ ဆုေပး ဒဏ္ေပးစနစ္မ်ိဳးလို့လဲ  ယူဆႏိုင္ပါတယ္။ ဥပမာ - Robot ကို Mazeထဲကဘယ္လိုထြက္မလဲ သင္ခိုင္းတာမ်ိဳး။ လမ္းေလွ်ာက္ရင္း နံရံရွိတဲ့ဆီကိုဝင္တိုက္ရင္ ဒဏ္ေပးမယ္၊ ဝင္မတိုက္ဘဲ ေဘးကိုေကြ့သြားရင္ ဆုေပးမယ္။ Mazeအျပင္ကိုထြက္ႏိုင္ရင္ ရတဲ့ဆုကအမ်ားဆံုး။ အဲလိုနဲ့ သူက ေရရွည္မွာ ဆုမ်ားမ်ားရတဲ့Actionေတြ လုပ္တတ္ေအာင္ သင္ယူသြားတာမ်ိဳးပါ။ ***အေရးအၾကီးဆံုးက ေရရွည္မွာဆုအမ်ားဆံုးရဖို့ျဖစ္တယ္။*** အဲဒီအတြက္ တစ္ခါတစ္ေလမွာ လက္ငင္းရႏိုင္တဲ့ ဆုအေသးေလးေတြကိုု စြန့္လႊတ္ျပီး ဒီထက္ပိုုၾကီးတဲ့ အနာဂတ္ဆုုလာဒ္ေတြကို ေစာင့္တတ္ဖို့လဲလိုတယ္။ 
ဥပမာ စစ္တုရင္ကစားရင္ ကိုယ့္အေရွ့မွာ အေကာင္အေသးေလးေတြ စားလို့ရတာရွိလိမ့္မယ္။ အဲလိုစားလိုုက္ရင္ ဆုရလိမ့္မယ္။ ဒါေပမယ့္ စားလိုက္ရင္ ေရရွည္မွာေကာင္းခ်င္မွ ေကာင္းမယ္။ ဟိုဘက္က Strategy အရ သူတို့အေကာင္အၾကီးေတြေရြႊ့ဖို့ အေကာင္အေသး(Pawn)ေတြကို တမင္ခ်ေၾကြးထားတာလည္း ျဖစ္ႏိုင္တယ္။ ဒါေၾကာင့္ **Immediate Reward** (လက္ငင္းဆု)ထက္ **Cumulative Rewardအမ်ားဆံုးရမယ့္ Action** ေတြလုပ္တတ္ေအာင္ သင္ယူရပါမယ္။ ဒါကေတာ့ Reinforcement Learning ရဲ့အေျခခံ သေဘာတရားပါ။ 

## Some Applications of Reinforcement Learning     
Roboticsဘက္မွာ Robotကို အျပင္ေလာကနဲ့ဆက္ဆံျပီး ဆံုးျဖတ္ခ်က္ေတြ ခ်တတ္လာေအာင္ သင္ေပးတဲ့ေနရာမ်ိဳးမွာ RLကိုသံုးတယ္။ ေမာင္းသူမဲ့ ကားေတြ Droneေလးေတြမွာလည္း သူ့ကိုုသံုးတယ္။
DeepMindရဲ့ AlphaGoအေၾကာင္းကို ေတာ္ေတာ္မ်ားမ်ားၾကားဖူးၾကမွာပါ။ AlphaGoက Reinforcement Learningကိုသံုးထားတာပါ။ Computerကို Gameေတြေဆာ့တတ္ေအာင္ သင္ေပးတဲ့ေနရာမွာ RLကိုအသံုးျပဳတယ္။[^1][^2]  
[^1]: [AlphaGo](https://deepmind.com/research/alphago/)  
[^2]: [Reinforcement learning with unsupervised auxiliary tasks](https://deepmind.com/blog/reinforcement-learning-unsupervised-auxiliary-tasks/)  

Roboticsတို့ Gameတို့အျပင္ Medicine၊ Manufacturingအစရွိသျဖင့္ တျခားနယ္ပယ္ေတြမွာလည္း RLကိုသံုးတယ္။ ဥပမာေပးရရင္ Googleက Reinforcement Learningကိုသံုးျပီး Data Center Cooling ကုန္က်ေငြကို ၄၀ရာခိုင္ႏွဳန္း ေလွ်ာ့ခ်ခဲ့တယ္။[^3][^4]
[^3]: [DeepMind AI Reduces Google Data Centre Cooling Bill by 40%](https://deepmind.com/blog/deepmind-ai-reduces-google-data-centre-cooling-bill-40/)
[^4]: [The AI That Cut Google’s Energy Bill Could Soon Help You](https://www.technologyreview.com/s/601938/the-ai-that-cut-googles-energy-bill-could-soon-help-you/)

## Natural Language Processing အတြက္ RLအသံုးျပဳပံုတခ်ိဳ့  
က်မက NLP researcherဆိုေတာ့ NLPနဲ့ပတ္သတ္တဲ့ ဥပမာေတြကို သတ္သတ္ခြဲေရးပါရေစ။  
အရင္တုန္းက Reinforcement Learningက NLPဘက္မွာ တျခား Machine Learning methodေတြေလာက္ မသံုးၾကဘူး။ RL for NLPကို Researchလုပ္ေနတဲ့ အုပ္စုေတြေတာ့ရွိတယ္။ ဒါေပမယ့္ Deep Learningေလာက္ မမ်ားဘူး။ ျပီးခဲ့တဲ့ ႏွစ္ႏွစ္ သံုးႏွစ္အတြင္းမွာေတာ့ NLPဘက္မွာလည္း RLကေခတ္စားစ ျပဳလာတယ္။ 
အဓိကအားျဖင့္ RLကိုသံုးတာက Dialog Systemsေတြနဲ့ Question Answeringအတြက္ပါ။ Dialog နဲ့ Question Answering Systemsဆိုတာက အျပင္က Environment(User)နဲ့ ထိေတြ့ဆက္ဆံေနရတာေလ။ အဲေတာ့ Userေျပာတဲ့ Feedbackအေပၚမူတည္ျပီး အလုပ္လုပ္ႏိုင္ဖို့ အေရးၾကီးတယ္။  

ဥပမာ Chatbotဆိုပါေတာ့။ ေအာက္က Google Assistantကို အိမ္ကေန Sentosaကို ဘယ္လိုသြားရမလဲလို့ေမးတဲ့ dialogကိုၾကည့္ၾကည့္ပါ။ Chatbotက ေမးခြန္းကိုၾကည့္တယ္၊ ေျဖႏိုင္ဖို့ၾကိဳးစားတယ္၊ ဒါေပမယ့္ အိမ္လိပ္စာကို မသိဘူး။ မသိေတာ့ Userကိုျပန္ေမးမယ္။ Userကဘာဆက္ေျပာလည္း အေပၚမူတည္ျပီး လုပ္စရာရွိတာ ဆက္လုပ္မယ္။ Userနဲ့ botနဲ့ၾကားမွာ Interactionရွိတယ္။ ဒါ့အျပင္ စကားေျပာသြားတာလည္း အေပၚနဲ့ ေအာက္နဲ့ ဆက္စပ္မွဴ Sequenceရွိတယ္။

![Chatbot]({{ site.url }}/logs/images/RLIntro/GoogleAssistant.jpg)

Supervised Learning လိုမ်ိဳး Inputေပး၊ Output Predictionလုပ္တဲ့ methodမ်ိဳးဆို Interactionကိုထည့္စဥ္းစားဖို့ေတာ္ေတာ္ခက္တယ္။ Supervised learningကိုလည္း Dialog Systemsေတြမွာသံုးတာမရွိဘူးမဟုတ္ဘူး။ အမ်ားၾကီး ရွိတယ္။ ဒါေပမယ့္ Deep Reinforcement Learningကိုသံုးရင္ User Interactionကိုပါ ထည့္စဥ္းစားလို့ရတယ္။ ဒါ့အျပင္ Supervised Learningလိုမ်ိဳး Reinforcement Learningက ဒီေမးခြန္းေမးရင္ ဒါမ်ိဳးေျဖပါဆိုျပီး သင္ေပးရမယ့္ အေမးအေျဖ Data setေတြအမ်ားၾကီးမလိုဘူး။ Dialog ဆိုတာမ်ိဳးက အမ်ိဳးမ်ိဳးေပါက္ကရေျပာလို့ရတာေလ။ အဲေတာ့ User Interactionကေနလည္း သင္ယူဖို့ အေရးၾကီးတယ္။  

Dialogကေတာ့ အျမင္သာဆံုး ဥပမာေပါ့။ [Information Retrieval and Extraction](https://arxiv.org/pdf/1603.07954.pdf)ဘက္မွာလည္း RLကိုသံုးဖို့ Researchလုပ္ေနတာေတြ ရွိတယ္။ ဥပမာ Computer ကို သူ့ဟာသူ [Googleတတ္ေအာင္ သင္ေပးတာ](https://arxiv.org/abs/1704.04572)တို့ [Manualေတြဖတ္တတ္ေအာင္](http://people.csail.mit.edu/regina/my_papers/civ11.pdf) သင္ေပးတာတို့။ [Parsingတို့](https://cs.stanford.edu/~pliang/papers/sample-aistats2015.pdf)၊ [Text based gamesတို့](https://arxiv.org/abs/1506.08941) အစရွိသျဖင့္ application ေတြမွာလည္း RL ကိုသံုးတယ္။ ဒါက RLကိုNLP မွာဘယ္လိုသံုးလဲဆိုတာ ဥပမာေပးတာပါ။ အေသးစိတ္ကိုေရးရင္ ဒီSectionနဲ့တင္ postကအရမ္းရွည္သြားမွာမို့လို့ ေနာက္မွ အားလို့ စိတ္ကူးေပါက္ရင္ ထပ္ေရးပါ့မယ္။ 

## RL ရဲ့အစိတ္အပိုင္းမ်ား  
{To Be Continued}  

## Exploration Vs Exploitation  
{To Be Continued}  


## Supervised Learning နဲ့ဘာကြာသလဲ ??  
Reinforcement Learningက Agentကေန Environmentကိုထုတ္ေပးတဲ့ Actionေတြပါတယ္။ ကိုယ္အရင္အဆင့္က ထုတ္ေပးတဲ့ Actionက ေနာက္အဆင့္ေတြအေပၚမွာပါ သက္ေရာက္မွဴရွိတယ္။ Chessကစားရင္ ကိုယ္အရင္က ေရႊ့ခဲ့တဲ့ Actionက ေနာက္အဆင့္ေတြမွာ အၾကိဳးသက္ေရာက္မွဴရွိတယ္။ အဆင့္(State)တစ္ခုုစီမွာ Agentက ဘာActionလုပ္ရင္ေကာင္းမလဲဆိုျပီး ဆံုးျဖတ္ရတယ္(Decision Making)။ သူလုပ္လိုက္တဲ့ Actionက Environmentအေပၚ အၾကိဳးသက္ေရာက္မွဴရွိတယ္။ Environmentကေန သူ့Actionအေပၚမူတည္ျပီး သူ့ကိုု ဆုေပးတာျဖစ္ျဖစ္ ဒဏ္ေပးတာျဖစ္ျဖစ္ Feedbackတစ္ခုခုျပန္ေပးတယ္။ 
Supervised Learningက အဲလိုမဟုတ္ဘူး။ Dataထဲမွာပါတဲ့ Independent Examplesေတြအေပၚ အေျခခံျပီးသင္ယူသြားတာျဖစ္တယ္။ ဒီ Inputမ်ိဳးေတြ့ရင္ ဘယ္လိုOutputမ်ိဳးထုတ္ရမယ္ဆိုတာမ်ိဳးျပသနာေတြအတြက္ အသံုးဝင္တယ္။ 
![RL vs SL]({{ site.url }}/logs/images/RLIntro/RLvsSL.png)  
{: .center-image}
*Supervised Learning Vs Reinforcement Learning*[^5]
{: .center}   
[^5]: [Introduction to Reinforcement Learning - Joelle Pineau](http://videolectures.net/deeplearning2016_pineau_reinforcement_learning/)  
## Reinforcement Learning ကိုဘယ္လိုေလ့လာရမလဲ ??
ေအာက္က ၂ခုကေတာ့ က်မကိုယ္တိုင္ သံုးခဲ့တဲ့ Resource ေတြပါ။ အဲဒီ ၂ခုနဲ့တင္ အေျခခံရျပီး တျခား Research Paper ေတြ သူမ်ားေရးထားတဲ့ Open Source Code ေတြကို ဖတ္ရင္ နားလည္ႏိုင္ပါတယ္။
* David Silver’s Reinforcement Learning Lectures [[Videos](https://youtu.be/2pWv7GOvuf0?list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT)][[Notes](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)]
* [Textbook: Reinforcement Learning: An Introduction ](http://people.inf.elte.hu/lorincz/Files/RL_2006/SuttonBook.pdf)   

ေအာက္က Resourceေတြကေတာ့ က်မကိုယ္တိုင္ မတက္ဖူးေသးတဲ့ နာမည္ၾကီး RL courseနဲ့ Tutorialေတြပါ။ ကိုယ္တိုင္မတက္ဖူးေသးလို့ အသံုးဝင္မဝင္ကိုေတာ့ မေျပာႏိုင္ပါဘူး။  Deep Reinforcement Learning Courseကေတာ့ ေတာ္ေတာ္ေကာင္းတယ္လို့ၾကားပါတယ္။
* [Udacity Reinforcement Learning Course](https://www.udacity.com/course/reinforcement-learning--ud600)  
* [Simple Reinforcement Learning with Tensorflow series](https://medium.com/@awjuliani/super-simple-reinforcement-learning-tutorial-part-1-fd544fab149)  
* [Deep Reinforcement Learning](http://rll.berkeley.edu/deeprlcourse/)