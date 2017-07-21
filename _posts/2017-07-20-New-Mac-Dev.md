---
layout: post
title: "New Macbook Dev Setup"
date: 2017-07-20
comments: true  
tags: [MISC]
draft: false
mathjax: false
---

ဒီနေ့ပဲ Macbookအသစ်ရလာတဲ့အတွက် ဂနာမငြိမ်ဘဲ ကလိပြီးဟိုသွင်းဒီသွင်းတာတွေကို ရေးထားတာပါ။  
[Mac-dev-setup](https://github.com/nicolashery/mac-dev-setup#homebrew)မှာ ပြောထားတာလေးတွေကို မှီငြမ်းပြီး ကိုယ်သုံးနေကျ Appတွေနဲ့ Machine Learningနဲ့ဆိုင်တာလေးတွေ ထည့်ထားပါတယ်။  
Pytorchကော Tensorflowကော လောလောဆယ် စမ်းတာတော့ ဘာမှပြသနာမတက်ဘဲ သွင်းလို့ရပါတယ်။  
နောင်တစ်ချိန် Macbook အသစ်ကို setupလုပ်ရင် ပြန်ကြည့်လို့ရအောင်နဲ့ တခြားလူတွေအတွက် အသုံးဝင်လိုဝင်ငြား မှတ်တမ်းတင်ထားတာပါ။ :)   
လောလောဆယ် မှတ်မိသလောက်ကတော့ ဒါပါပဲ။ နောက်မှ အသုံးဝင်တဲ့ package တွေ စိတ်ထဲပေါ်လာတာရှိရင် လာပြီး updateလုပ်ပါ့မယ်။



# Dev Setup
- iTerm2 
- beautiful terminal
- Homebrew
- Git
- Sublime Text  
-- Markdown Editing  
-- Markdown Preview  
-- Sublimelinter with pylint and pep8
- Vim
- [python3 and virtualenv](#python3-and-virtualenv)
- [Numpy and Scipy](#numpy-and-scipy)
- [Jupyter Notebook](#jupyter)
- [pytorch](#pytorch)
- [Tensorflow](#tensorflow)

# Apps
- Chrome and extensions
- SourceTree
- Google Drive
- Dropbox
- [Evernote](https://evernote.com/)
- [Zotero](https://www.zotero.org/)
- [MacTex](http://tug.org/mactex/mactex-download.html)
- [TexStudio](http://www.texstudio.org/)

# Python3 and Virtualenv
```
$ brew install python3
$ pip3 install virtualenv
```

# Numpy and Scipy
```
$ brew install numpy
$ brew install scipy
```

# Jupyter
```
$ pip3 install --upgrade jupyter
```

# Pytorch
```
$ virtualenv --system-site-packages -p python3 ~/py3torch
$ source ~/py3torch/bin/activate
$ pip install http://download.pytorch.org/whl/torch-0.1.12.post2-cp36-cp36m-macosx_10_7_x86_64.whl 
$ pip install torchvision
$ deactivate
```

# Tensorflow
```
$ virtualenv --system-site-packages -p python3 ~/tensorflow
$ source ~/tensorflow/bin/activate
$ pip3 install --upgrade tensorflow
$ deactivate
```
