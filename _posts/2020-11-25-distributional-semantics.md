---
layout: post
title: "Distributional Semantics"
date: 2020-11-25
comments: true  
tags: [Natural Language Processing]
draft: false
mathjax: true
---

tesgüino ဆိုတဲ့စကားလုံးရဲ့ အဓိပ္ပါယ်ကို သင်သိပါသလား? (google မခေါက်နဲ့နော်)
သင်အဲ့ဒီစကားလုံးရဲ့ အဓိပ္ပါယ်ကို နားမလည်ဘူးဆိုပါစို့။
အောက်ကစာကြောင်းလေးတွေဖတ်ကြည့်ပါ။ [^1]

[^1]:[Automatic Retrieval and Clustering of Similar Words (Lin et al., 1998).](https://www.aclweb.org/anthology/C98-2122.pdf)


1. A bottle of tesgüino is on the table.
2. Everybody likes tesgüino.
3. Tesgüino makes you drunk.
4. We make tesgüino out of corn.

ကဲခုလောက်ဆို tesgüino ကဘာလဲဆိုတာ ခန့်မှန်းပြီး နားလည်လောက်ပြီ ထင်ပါတယ်။ 
tesgüino ဆိုတဲ့ စကားလုံးဟာ ပြောင်းဖူးကနေ ထုတ်ထားတဲ့ အရက်တစ်မျိုးဆိုတာကို ပေးထားတဲ့စားကြောင်းတွေထဲမှာ အဲ့စကားလုံးကို ဘယ်လိုသုံးထားလဲဆိုတဲ့ context ကိုကြည့်ပြီး နားလည်နိုင်တယ်။
အဲဒီစာကြောင်းတွေက tesgüino ဆိုတဲ့စာလုံးကို wine နဲ့အစားထိုးကြည့်ရရင် အဓိပ္ပါယ်ရှိသေးတယ်။ ဒါပေမဲ့ tesgüino ကို rock နဲ့ အစားထိုးကြည့်ရင် အဓိပ္ပါယ်က သိပ်မရှိတော့ဘူး။ ဘာဖြစ်လို့လဲဆိုတော့ rock (ကျောက်ခဲ)က ပေးထားတဲ့ အရက်နဲ့သက်ဆိုင်တဲ့ context နဲ့ မသင့်တော်ဘူး။

Distributional Semantics ရဲ့သဘောတရားက ဒါပါပဲ။ အဓိပ္ပါယ်တူတဲ့ စကားလုံး တွေကို ခပ်ဆင်ဆင် context တွေမှာ အသုံးချခံရတတ်တယ်။
“If A and B have almost identical environments we say that they are synonyms.”  -- Harris (1954)

စကားလုံးတစ်လုံးရဲ့ အဓိပ္ပါယ်ကို သူ့နားမှာရှိတဲ့ တခြားစကားလုံးတွေကို ကြည့်ခြင်းဖြင့် သိနိုင်တယ်။
“You shall know a word by the company it keeps!” -- Firth (1957)

ဒီသဘောတရားလေးက ရိုးရှင်းပေမဲ့ အရမ်းအရေးကြီးတယ်။ Natural Language Processing ဆိုတဲ့ဘာသာရပ်မှာ အရမ်း အရေးပါတဲ့ word representation (word2vec) တွေ၊ contextual representation (ELMo, BERT) တွေဆိုတာ "စကားလုံးတစ်လုံးရဲ့ အဓိပ္ပါယ်ကိုသိဖို့ သူရဲ့ context ကိုသိရမယ်" ဆိုတဲ့ distributional semantics ကို အခြေခံပြီး တည်ဆောက်ထားတာပါ။  
Word representation	တွေနဲ့ပတ်သတ်ပြီး ဒီထက်ပို လေ့လာချင်ရင် ဒီ [blog post](https://lena-voita.github.io/nlp_course/word_embeddings.html) လေးကို ညွှန်းပါရစေ။


# References
---
