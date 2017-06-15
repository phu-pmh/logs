---
layout: post
title: "Reinforcement Learning မိတ်ဆက်"
description: "Reinforcement Learning အကျဉ်းချုပ် မိတ်ဆက်"
date: 2017-05-20
tags: [Reinforcement Learning, Burmese]
comments: true
share: true
mathjax: false
---


**Contents**
* မိတ်ဆက်  
* Some Applications of Reinforcement Learning 
* Natural Language Processing မှာ RL ကိုအသုံးပြုပုံ  
* RL ရဲ့အစိတ်အပိုင်းများ  
* Exploration Vs Exploitation  
* Supervised Learning နဲ့ဘာကွာသလဲ ??    
* Reinforcement Learning ကိုဘယ်လိုလေ့လာရမလဲ ??
* မှတ်ချက်
{:toc}

## မိတ်ဆက်  
**Machine Learning** မှာ **Supervised Learning၊ Unsupervised Learning နဲ့ Reinforcement Learning** ဆိုပြီး ၃မျိုးခွဲလို့ရပါတယ်။ ဒီ Post မှာ အဓိကပြောချင်တာက Reinforcement Learning ပါ။ 

**Supervised Learning** ကတော့ Data Science and Analyticsလုပ်တဲ့ လူတွေနဲ့ အရင်းနှီးဆုံး ဖြစ်မှာပါ။ Supervised Learning က လွယ်လွယ်ပြောရရင် ကိုယ့်မှာရှိတဲ့ Labeled Data ကိုကြည့်ပြီးတော့ ဒီ Input မျိုးဆိုရင် ဘယ်လို Output Label မျိုးထုတ်ပေးရမလဲဆိုတာကို ကွန်ပြူတာကိုသင်ခိုင်းတာပါ(Training)။ ဥပမာ ကွန်ပြူတာကို ပန်းသီးပုံတွေအများကြီးပြပြီး ဒါပန်းသီး ဒါပန်းသီးဆိုပြီးသင်ပေးမယ်။ တခြား မမြင်ဖူးသေးတဲ့ပန်းသီးပုံတွေလာရင် ပန်းသီးလို့ခန့်မှန်းတတ်အောင် သင်ပေးတာမျိုးပါ။

**Unsupervised Learning** ကတော့ Label ရယ်လို့မရှိဘူး။ ဒီ Input ပေးရင် ဒီလို Label မျိုးထုတ်ပေးရမယ်ဆိုပြီး သတ်သတ်မှတ်မှတ် သင်မပေးဘူး။ Clustering က Unsupervised Learning တစ်မျိုးပါပဲ။ အလွယ်ဆုံး ဥပမာပေးရရင် ကြောင်ပုံတွေနဲ့ခွေးပုံတွေ အများကြီးကို ကွန်ပြူတာထဲထည့်ပေးပြီး ကွန်ပြူတာကို အုပ်စု၂ခု (or ၃ခု) ခွဲတတ်အောင် သင်ပေးတာပါ။ သူ့ကို ပုံတွေပြပြီး ဒါကကြောင် ဒါကခွေးဆိုပြီး Label တပ်ပေးပြီး supervise ပေးစရာမလိုဘူး။ သူ့ဘာသူကြည့်ပြီး ဒီကောင်လေးတွေကရုပ်ဆင်တယ် တစ်အုပ်စုနေဆိုပြီး အစုခွဲလိုက်တာမျိုး။ 

**Reinforcement Learning** ကတော့ Goal-directed Agentကို အပြင်လောက(Environment)နဲ့ ထိတွေ့ခိုင်းပြီး Environmentကပြန်ပေးတဲ့ Feedbackအပေါ်မူတည်ပြီး ဒီလိုအခြေအနေမျိုးဆို ဘာActionလုပ်သင့်တယ်ဆိုပြီးသင်တာပါ။ ဆုပေး ဒဏ်ပေးစနစ်မျိုးလို့လဲ  ယူဆနိုင်ပါတယ်။ ဥပမာ - Robot ကို Mazeထဲကဘယ်လိုထွက်မလဲ သင်ခိုင်းတာမျိုး။ လမ်းလျှောက်ရင်း နံရံရှိတဲ့ဆီကိုဝင်တိုက်ရင် ဒဏ်ပေးမယ်၊ ဝင်မတိုက်ဘဲ ဘေးကိုကွေ့သွားရင် ဆုပေးမယ်။ Mazeအပြင်ကိုထွက်နိုင်ရင် ရတဲ့ဆုကအများဆုံး။ အဲလိုနဲ့ သူက ရေရှည်မှာ ဆုများများရတဲ့Actionတွေ လုပ်တတ်အောင် သင်ယူသွားတာမျိုးပါ။ ***အရေးအကြီးဆုံးက ရေရှည်မှာဆုအများဆုံးရဖို့ဖြစ်တယ်။*** အဲဒီအတွက် တစ်ခါတစ်လေမှာ လက်ငင်းရနိုင်တဲ့ ဆုအသေးလေးတွေကို စွန့်လွှတ်ပြီး ဒီထက်ပိုကြီးတဲ့ အနာဂတ်ဆုလာဒ်တွေကို စောင့်တတ်ဖို့လဲလိုတယ်။  

ဥပမာ စစ်တုရင်ကစားရင် ကိုယ့်အရှေ့မှာ အကောင်အသေးလေးတွေ စားလို့ရတာရှိလိမ့်မယ်။ အဲလိုစားလိုက်ရင် ဆုရလိမ့်မယ်။ ဒါပေမယ့် စားလိုက်ရင် ရေရှည်မှာကောင်းချင်မှ ကောင်းမယ်။ ဟိုဘက်က Strategy အရ သူတို့အကောင်အကြီးတွေရွှေ့ဖို့ အကောင်အသေး(Pawn)တွေကို တမင်ချကြွေးထားတာလည်း ဖြစ်နိုင်တယ်။ ဒါကြောင့် **Immediate Reward** (လက်ငင်းဆု)ထက် **Cumulative Rewardအများဆုံးရမယ့် Action** တွေလုပ်တတ်အောင် သင်ယူရပါမယ်။ ဒါကတော့ Reinforcement Learning ရဲ့အခြေခံ သဘောတရားပါ။ 

## Some Applications of Reinforcement Learning     
Roboticsဘက်မှာ Robotကို အပြင်လောကနဲ့ဆက်ဆံပြီး ဆုံးဖြတ်ချက်တွေ ချတတ်လာအောင် သင်ပေးတဲ့နေရာမျိုးမှာ RLကိုသုံးတယ်။ မောင်းသူမဲ့ ကားတွေ Droneလေးတွေမှာလည်း သူ့ကိုသုံးတယ်။  

DeepMindရဲ့ AlphaGoအကြောင်းကို တော်တော်များများကြားဖူးကြမှာပါ။ AlphaGoက Reinforcement Learningကိုသုံးထားတာပါ။ Computerကို Gameတွေဆော့တတ်အောင် သင်ပေးတဲ့နေရာမှာ RLကိုအသုံးပြုတယ်။[^1],[^2]  

[^1]: [AlphaGo](https://deepmind.com/research/alphago/)  

[^2]: [Reinforcement learning with unsupervised auxiliary tasks](https://deepmind.com/blog/reinforcement-learning-unsupervised-auxiliary-tasks/)  

Roboticsတို့ Gameတို့အပြင် Medicine၊ Manufacturingအစရှိသဖြင့် တခြားနယ်ပယ်တွေမှာလည်း RLကိုသုံးတယ်။ ဥပမာပေးရရင် Googleက Reinforcement Learningကိုသုံးပြီး Data Center Cooling ကုန်ကျငွေကို ၄၀ရာခိုင်နှုန်း လျှော့ချခဲ့တယ်။[^3],[^4]  

[^3]: [DeepMind AI Reduces Google Data Centre Cooling Bill by 40%](https://deepmind.com/blog/deepmind-ai-reduces-google-data-centre-cooling-bill-40/)  

[^4]: [The AI That Cut Google’s Energy Bill Could Soon Help You](https://www.technologyreview.com/s/601938/the-ai-that-cut-googles-energy-bill-could-soon-help-you/)

## Natural Language Processing အတွက် RL applicationတချို့  
ကျမက NLP သမားဆိုတော့ NLPနဲ့ပတ်သတ်တဲ့ applicationတချို့အကြောင်းလည်း ပြောချင်ပါတယ်။  
အရင်တုန်းက Reinforcement Learningက NLPဘက်မှာ တခြား Machine Learning methodတွေလောက် မသုံးကြဘူး။ RL for NLPကို Researchလုပ်နေတဲ့ အုပ်စုတွေတော့ရှိတယ်။ ဒါပေမယ့် Deep Learningလောက် မများဘူး။ ပြီးခဲ့တဲ့ နှစ်နှစ် သုံးနှစ်အတွင်းမှာတော့ NLPဘက်မှာလည်း RLကခေတ်စားစ ပြုလာတယ်။ 
အဓိကအားဖြင့် RLကိုသုံးတာက Dialog Systemsတွေနဲ့ Question Answeringအတွက်ပါ။ Dialog နဲ့ Question Answering Systemsဆိုတာက အပြင်က Environment(User)နဲ့ ထိတွေ့ဆက်ဆံနေရတာလေ။ အဲတော့ Userပြောတဲ့ Feedbackအပေါ်မူတည်ပြီး အလုပ်လုပ်နိုင်ဖို့ အရေးကြီးတယ်။  

ဥပမာ Chatbotဆိုပါတော့။ အောက်က Google Assistantကို အိမ်ကနေ Sentosaကို ဘယ်လိုသွားရမလဲလို့မေးတဲ့ dialogကိုကြည့်ကြည့်ပါ။ Chatbotက မေးခွန်းကိုကြည့်တယ်၊ ဖြေနိုင်ဖို့ကြိုးစားတယ်၊ ဒါပေမယ့် အိမ်လိပ်စာကို မသိဘူး။ မသိတော့ Userကိုပြန်မေးမယ်။ Userကဘာဆက်ပြောလည်း အပေါ်မူတည်ပြီး လုပ်စရာရှိတာ ဆက်လုပ်မယ်။ Userနဲ့ botနဲ့ကြားမှာ Interactionရှိတယ်။ ဒါ့အပြင် စကားပြောသွားတာလည်း အပေါ်နဲ့ အောက်နဲ့ ဆက်စပ်မှူ Sequenceရှိတယ်။

![Chatbot]({{ site.url }}/images/RLIntro/GoogleAssistant.jpg)

Supervised Learning လိုမျိုး Inputပေး၊ Output Predictionလုပ်တဲ့ methodမျိုးဆို Interactionကိုထည့်စဉ်းစားဖို့တော်တော်ခက်တယ်။ Supervised learningကိုလည်း Dialog Systemsတွေမှာသုံးတာမရှိဘူးမဟုတ်ဘူး။ အများကြီး ရှိတယ်။ ဒါပေမယ့် Deep Reinforcement Learningကိုသုံးရင် User Interactionကိုပါ ထည့်စဉ်းစားလို့ရတယ်။ Dialog ဆိုတာမျိုးက အမျိုးမျိုးပေါက်ကရပြောလို့ရတာလေ။ အဲတော့ User Interactionကနေလည်း သင်ယူဖို့ အရေးကြီးတယ်။  

Dialogကတော့ အမြင်သာဆုံး ဥပမာပေါ့။ [Information Retrieval and Extraction](https://arxiv.org/pdf/1603.07954.pdf)ဘက်မှာလည်း RLကိုသုံးတာတွေ ရှိတယ်။ ဥပမာ Computer ကို သူ့ဟာသူ [Googleတတ်အောင် သင်ပေးတာ](https://arxiv.org/abs/1704.04572)တို့ [Manualတွေဖတ်တတ်အောင်](http://people.csail.mit.edu/regina/my_papers/civ11.pdf) သင်ပေးတာတို့။ [Parsingတို့](https://cs.stanford.edu/~pliang/papers/sample-aistats2015.pdf)၊ [Text based gamesတို့](https://arxiv.org/abs/1506.08941) အစရှိသဖြင့် application တွေမှာလည်း RL ကိုသုံးတယ်။  

ဒါက RLကိုNLP မှာဘယ်လိုသုံးလဲဆိုတာ ဥပမာပေးတာပါ။ အသေးစိတ်ကိုရေးရင် ဒီSectionနဲ့တင် postကအရမ်းရှည်သွားမှာမို့လို့ နောက်မှ အားလို့ စိတ်ကူးပေါက်ရင် ထပ်ရေးပါ့မယ်။ 

## RL ရဲ့အစိတ်အပိုင်းများ  
![RL]({{ site.url }}/images/RLIntro/RL.png)
{: .center-image }

Reinforcement Learningကဘာလဲဆိုတာ အပေါ်မှာ ပြောခဲ့တာကို ပြန်ပြီး recapပြန်လုပ်တာပေါ့။ 
ပုံမှာပြထားတဲ့အတိုင်း Time Step t မှာ Agentက Actionတစ်ခုခုကိုလုပ်လိုက်မယ်။ အစပိုင်းမှာ သူက ဘယ် Actionကကောင်းမှန်းမသိသေးဘူး။ အဲတော့ ဒီအတိုင်း random action တစ်ခုကို Tryကြည့်တယ်။ သူ့Actionအပေါ်မူတည်ပြီး State S<sub>t+1</sub>ကပြောင်းသွားမယ်။ ပြီးရင် Reward ပြန်ရမယ်။

### Policy  
Policy ဆိုတာ Stateကနေ Actionကို Mapလုပ်ပေးတဲ့ functionဖြစ်တယ်။ Agentရဲ့ behaviorကို Policyကဆုံးဖြတ်ပေးတယ်။

### Value Function  
Value Functionက အနာဂတ်မှာရလာမယ့် စုစုပေါင်း Rewardကိုခန့်မှန်းတဲ့ Functionဖြစ်တယ်။ ဒီStateမှာနေရင် ရေရည်မှာ စုစုပေါင်း Rewardဘယ်လောက်ရမယ်ဆိုတာကို Value Functionသုံးပြီးခန့်မှန်းလို့ရတယ်။ များသောအားဖြင့် ဘယ်Actionလုပ်ရမလဲဆိုတဲ့ Policyကိုသင်ယူတာက Value Functionကိုအရင်တွက်ပြီး Value အများဆုံးပေးမယ့် Stateနဲ့ Actionကို Greedyရှာတာဖြစ်တယ်။  

ဥပမာ Maze မှာဆို Action က အရှေ့၊ အနောက်၊ ဘယ်၊ညာဆိုပြီး ရှိတယ်ထားပါတော့။ အရှေ့နဲ့ ဘယ်ကိုသွားရင် ချောက်ထဲကျမယ်။ ညာနဲ့ အနောက်က Safeဖြစ်တယ်။ ဒါပေမယ့် ညာကတစ်ဆင့်သွားရင် ခရီးပိုရှည်မယ်၊ အနောက်ကိုသွားရင် မြန်မြန်နိုင်လိမ့်မယ်ဆိုပါဆို့။ ဒါဆိုရင် အနောက်အကွက်က Valueကကျန်တာတွေထက် အများဆုံးဖြစ်လိမ့်မယ်။ အဲဒီအတွက် အများဆုံး Value ရှိတဲ့ဘက်ကို ရွေ့ဖို့ Policyကဆုံးဖြတ်ပေးလိမ့်မယ်။  
Value functionကိုမရှာဘဲ Policyကိုတန်းသင်တဲ့နည်းတွေလည်းရှိတယ်။

## Exploration Vs Exploitation  
Agentကို စသင်ပေးတဲ့အချိန်မှာ Value Function တွေ Policyတွေကိုမသိသေးဘူး။ အဲတော့ ဘယ်Actionနဲ့ ဘယ်Stateက Rewardကောင်းကောင်းပေးမလဲဆိုတာကို သူ့ဟာသာ Trial and Errorစနစ်နဲ့ စမ်းကြည့်ဖို့လိုတယ်။ ဘယ်Stateမှာ ဘယ်Actionကိုလုပ်ရင် ဘယ် Return(Total Reward)ရမယ်။ အဲလို မသိသေးတဲ့ဟာတွေကို လျှောက်စမ်းတာကို Explorationလို့ခေါ်တယ်။
အဲလိုနဲ့ အများကြီးစမ်းကြည့်ပြီးတော့ Environmentရဲ့သဘောတရားကို နည်းနည်းပါးပါး နားလည်လာတဲ့အခါ အဲဒီKnowledgeကို အသုံးချပြီး ကိုယ့်အတွက် Rewardအများဆုံးရမယ့် Actionမျိုးတွေကိုရွေးရမယ်။ ဒါကို Exploitationလို့ခေါ်တယ်။ 

Reinforcement Learningမှာ Explorationနဲ့ Exploitationကို မျှမျှတတ လုပ်ဖို့လိုတယ်။ ဥပမာပေးရရင် ကိုယ်က ပတ်ဝန်းကျင်အသစ်ကို ပြောင်းသွားတယ်ဆိုပါဆို့။ အဲနားပတ်ဝန်းကျင်မှာ ဘာစားသောက်ဆိုင်တွေ ကောင်းမှန်းမသိဘူး။ အဲတော့ စားသောက်ဆိုင်တစ်ခုချင်းစီကို စမ်းစားကြည့်ဖို့လိုတယ်။ Explorationလုပ်တာပေါ့နော်။ အဲလိုစားကြည့်ပြီးတော့မှ နောက်ဆို ကိုယ်ကြိုက်တဲ့စားသောက်ဆိုင်ကို ရွေးစားလို့ရတယ်။ ဒါက ကိုယ်သိထားတဲ့ Knowledgeအပေါ်မူတည်ပြီး Exploitationလုပ်တာ။ Exploreမလုပ်ဘဲ စားနေကျဆိုင် မှာချည်းပဲ စားရင် တခြားပိုကောင်းတဲ့ဆိုင်တွေရှိမှန်း သိမှာမဟုတ်ဘူး။ Exploreချည်းပဲလုပ်နေလို့ရှိရင်လည်း ကိုယ်အရင်စားနေကျဆိုင်လောက် မကောင်းတဲ့ဆိုင်တွေနဲ့ချည်းကြုံနေရင် ပြသနာ။


## Supervised Learning နဲ့ဘာကွာသလဲ ??  
Reinforcement Learningက Agentကနေ Environmentကိုထုတ်ပေးတဲ့ Actionတွေပါတယ်။ ကိုယ်အရင်အဆင့်က ထုတ်ပေးတဲ့ Actionက နောက်အဆင့်တွေအပေါ်မှာပါ သက်ရောက်မှူရှိတယ်။ Chessကစားရင် ကိုယ်အရင်က ရွှေ့ခဲ့တဲ့ Actionက နောက်အဆင့်တွေမှာ အကြိုးသက်ရောက်မှူရှိတယ်။ အဆင့်(State)တစ်ခုစီမှာ Agentက ဘာActionလုပ်ရင်ကောင်းမလဲဆိုပြီး ဆုံးဖြတ်ရတယ်(Decision Making)။ သူလုပ်လိုက်တဲ့ Actionက Environmentအပေါ် အကြိုးသက်ရောက်မှူရှိတယ်။ Environmentကနေ သူ့Actionအပေါ်မူတည်ပြီး သူ့ကို ဆုပေးတာဖြစ်ဖြစ် ဒဏ်ပေးတာဖြစ်ဖြစ် Feedbackတစ်ခုခုပြန်ပေးတယ်။  

Supervised Learningက အဲလိုမဟုတ်ဘူး။ Dataထဲမှာပါတဲ့ Independent Examplesတွေအပေါ် အခြေခံပြီးသင်ယူသွားတာဖြစ်တယ်။ ဒီ Inputမျိုးတွေ့ရင် ဘယ်လိုOutputမျိုးထုတ်ရမယ်ဆိုတာမျိုးပြသနာတွေအတွက် အသုံးဝင်တယ်။ 
![RL vs SL]({{ site.url }}/images/RLIntro/RLvsSL.png)  
{: .center-image}
*Supervised Learning Vs Reinforcement Learning*[^5]
{: .center}   
[^5]: [Introduction to Reinforcement Learning - Joelle Pineau](http://videolectures.net/deeplearning2016_pineau_reinforcement_learning/)  

## Reinforcement Learning ကိုဘယ်လိုလေ့လာရမလဲ ??  
ဒီPostက RLကို မသိသေးသူတွေအတွက် မိတ်ဆက်ရုံသက်သက်ပါ။ ဒါဖတ်ပြီး စိတ်ဝင်စားလို့ လေ့လာချင်တယ်ဆိုရင် အောက်က ၃ခုကတော့ ကျမကိုယ်တိုင် သုံးခဲ့တဲ့ Resource တွေပါ။ အဲဒီ ၃ခုနဲ့တင် အခြေခံရပြီး တခြား Research Paper တွေ သူများရေးထားတဲ့ Open Source Code တွေကို ဖတ်ရင် နားလည်နိုင်ပါတယ်။ David Silverရဲ့ Videoတွေကို အရင်ကြည့်ပြီး သူနဲ့ဆိုင်တဲ့ Textbookက Chapterတွေကိုလိုက်ဖတ်ကြည့်ပါ။ ပြီးတော့ Exerciseတွေလိုက်လုပ်ကြည့်ပါ။
* David Silver’s Reinforcement Learning Lectures [[Videos](https://youtu.be/2pWv7GOvuf0?list=PL7-jPKtc4r78-wCZcQn5IqyuWhBZ8fOxT)][[Notes](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)]
* [Textbook: Reinforcement Learning: An Introduction -  ](http://incompleteideas.net/sutton/book/bookdraft2016sep.pdf)  
* [Exercises: WildML - Learning RL](http://www.wildml.com/2016/10/learning-reinforcement-learning/)

အောက်က Resourceတွေကတော့ ကျမကိုယ်တိုင် မတက်ဖူးသေးတဲ့ နာမည်ကြီး RL courseနဲ့ Tutorialတွေပါ။ ကိုယ်တိုင်မတက်ဖူးသေးလို့ အသုံးဝင်မဝင်ကိုတော့ မပြောနိုင်ပါဘူး။  Deep Reinforcement Learning Courseကတော့ တော်တော်ကောင်းတယ်လို့ကြားပါတယ်။
* [Udacity Reinforcement Learning Course](https://www.udacity.com/course/reinforcement-learning--ud600)  
* [Simple Reinforcement Learning with Tensorflow series](https://medium.com/@awjuliani/super-simple-reinforcement-learning-tutorial-part-1-fd544fab149)  
* [Deep Reinforcement Learning](http://rll.berkeley.edu/deeprlcourse/)

## မှတ်ချက်
တချို့ Conceptတွေကို မြန်မာလိုတတ်နိုင်သလောက် ကြိုးစားရေးထားပေမယ့် အရေးအသားညံ့ဖျင်းတဲ့အတွက် မရှင်းတာတွေ၊ မြန်မာစာအရေးအသား မှားနေတာရှိလဲ ထောက်ပြနိုင်ပါတယ် :P