﻿---
layout: post
title: GNU Emacs Text Editor Basic Guide 
date:   2020-09-01 16:04:00 +0300
image:  emacs.png
tags:  Emacs Beginner Guide
---
What is Emacs (GNU Emacs)?

စိတ်ကြိုက်ပြင်ချင်တာလား၊ extension တွေထပ်တိုးချင်တာလား၊ Free and Libre ဖြစ်နေတဲ့  " GNU Emacs" က သင့်coding env ကို ပိုမို တွင်ကျယ် စမတ်ကျအောင်စွမ်းဆောင်ပေးနိုင်မယ့် Text Editor တစ်ခုဖြစ်ပါတယ်။

Emacs က ဘာတွေများ ထူးထူးခြားခြားစွမ်းဆောင်ပေးနိုင်လဲ ?
- code ရေးသားနေချိန်တွင် touch pad, mouse စသည်တို့ကို အသုံးပြုရန်မလိုအပ်အောင် စွမ်းဆောင်ပေးပါတယ်
-   code ရေးသားရာတွင် ခွဲခြားသတိမူနိုင်စေရန် အရောင်သတ်မှတ်ဖော်ပြပေးပါတယ်
-   အသုံးပြုသူတွေအတွက် ပြည့်စုံတဲ့ လမ်းညွှန်ချက်များ ပါရှိပြီး အလွယ်တကူဖတ်နိုင်ပါတယ်
-   လက်ရေးမူများအတွက် Unicode အပြည့်အဝ ထောက်ပံ့ပေးနိုင်ပါတယ်
-   စိတ်ကြိုက်ပြင်ဆင်ချက်များကို အလွယ်တကူ ဖန်တီးလို့ရပါတယ်
-   လုပ်ဆောင်ချက်တွေထပ်တိုးဖို့လည်း အဆင်သင့်ထုပ်ပိုးပြီးသား extension တွေရှိပါသေးတယ်


**Download and Install Emacs**

Cross Platform အသုံးပြုနိုင်ပါတယ်။ အောက်က လင့်မှာ Download && install လုပ်နိုင်ပါတယ်

https://www.gnu.org/software/emacs/download.html#gnu-linux


	$sudo apt-get update
    $sudo apt-get install -y emacs
    

Step2: Emacs ထံသို့ ချည်းကပ်ကြည့်ချင်း
 
- စက်မှာ install လုပ်ထားပြီးပြီဆိုရင်တော့ ဖွင့်လိုက်ပါ (Terminal ကဖြစ်ဖြဖစ် GUI နဲ့ဖြစ်ဖြစ်)

![ emacs start page]({{site.baseurl}}/img/emacs-termidology.png)အထက်ပါ ပုံအတိုင်း မြင်တွေ့ရမှာပါဖြစ်ပါတယ် ( နဲနဲရှင်းပြမယ်လေနော်)
***POINT*** : Cursor pointer ဖြစ်ပါတယ်
***FRAME Window*** : Emacs ရဲ့ မီနူးအပြင်အဆင် ထားရှိတဲ့ ဘောင်ဖြစ်တယ်
***BUFFER*** : ဖိုင်တွေဖွင့်ပေးနိုင်တဲ့နေရာဖြစ်တယ်
***Status Bar*** : လက်ရှိ buffer အတွင်းမှာရှိတဲ့ အချက်အလက်တွေကို ပြပေးတဲ့နေရာတစ်ခုဖြစ်တယ် ( စာလုံးရေ၊ command စသည်)
***Mini Buffer*** : Buffer အသေးစားလေးတစ်ခုဖြစ်ပြီး command execute လုပ်ခြင်းနဲ့ ဖိုင်များဖွင့်ရန် အသုံးပြုနိင်သည်.

****အမှာစာ****
 Emacs မှာ pointer ကို နေရာရွှေ့တဲ့အခါမှာ mouse or touch pad တွေအသုံးပြုစရာမလိုအပ်ပါဘူး၊
**ဒီနေရာမှာ အဓိက အသုံးပြုသွားမှာကတော့  C (Ctrl) နဲ့ M (Alt) တို့ဘဲဖြစ်ပါတယ်**

![ emacs start page]({{site.baseurl}}/img/emacs-keys.png)
 
အပေါ်က ပုံလေးကိုမြင်ရင် နဲနဲသဘောပေါက်သွားမယ်ထင်ပါတယ်

Step 3 : Let Rock ! 

**Ctrl key သုံးပြိး လိုက်လုပ်ကြည့်လိုက်ရအောင်**
ကျွန်တော်တို့ emacs ဖွင့်လိုက်တဲ့အခါမှာ Emacs Tutorial ဆိုတဲ့ ခေါင်းစဉ်လေးတစ်ခုပါပါတယ်။ အဲ့နေရာကို Pointer ရွှေ့ဖို့ဆိုရင် 
- Next Line (bottom line) ကိုဆင်းမှာ ဖြစ်တဲ့အတွက် C+n (Ctrl + n ) ကိုတစ်ချက်ချင်းနှိပ်ပြီး သွားနိုင်ပါတယ်
- အပေါ်လိုင်းတွေကို ပြန်တက်ချင်ရင် Previous Line (C+p) ကိုနှိပ်လို့ရပါတယ်
- ရှေ့ဘက်ကို pointer ရွှေ့လိုတဲ့အခါ Forward  (C+f) ကိုသုံးပြီး 
-  နောက်ဘက်ကိုပြန်ဆုတ်ချင်ရင်တော့ Backward (C+b) ပါ
- စာကြောင်းတစ်ကြောင်းရဲ့ အစကိုပြန်သွားချင်ရင်တော့ (C+a) အသုံးပြုပြီး
- စာကြောင်းရဲ့ အဆုံးသတ်ကို တော့ (C+e) နဲ့ သွားနိုင်ပါတယ်

**M ( Alt key ) သုံးကြည့်မယ်**
ကျွန်တော်တို့ အထက်မှာ Ctrl (C) နဲ့တွဲပြီး အသုံးပြုခဲ့တာကို တွေ့ရမှာပါ၊ (C) နဲ့ သုံးတဲ့အခါ စာလုံး တစ်လုံးစီသာ ရွေ့တာကို မြင်ရမှာပါ၊
M (Alt Key) နဲ့ အသုံးပြုမယ်ဆိုရင်တော့ စကားစု တစ်ခုချင်းစီအတွက် ရွေ့လျားတာကို မြင်တွေ့ရပါတယ်

- M+a = ဝါကျတစ်ကြောင်း၏အစသို့သွားရန်
- M+e = ဝါကျတစ်ကြောင်း၏ နောက်ဆုံးသို့
- M+b = နောက်စကားစု တစ်စုဆီသို့
- M+f = ရှေ့စကားစု တစ်စုဆိသို့
- M+< = မူလအစသို့
- M+> = အဆုံးသတ်ဆီသို့

**Jumping**
	အထက်မှာ ရှင်းပြခဲ့တဲ့နည်းလမ်းတွေကို ပိုမိုမြန်ဆန်အောင် Jumping Key (C+u) နဲ့ တွဲဖက်အသုံးပြုလို့ရပါတယ်
	-ဉပမာ-
	"Walk To The Height Walls " ဆိုတဲ့ စာကြောင်းအစမှာ pointer ရှိတယ်ဆိုပါစို့
	ကျွန်တော်က ရှေ့ဆယ်လုံးမြောက်ကို သွားဖို့လိုနေတဲ့အခါမှာ C-f 10 ခါနှိပ်ရပါမယ်
	**jumping လုပ်လိုက်ရင်တော့ C-u 10 C-f ဆိုပြီး တန်းသွားလို့ရပါတယ်**

**Searching**
 Emacs မှာလည်း စာလုံးတွေကို အလွယ်တကူ ရှာဖွေနိုင်ပါတယ်
 - C+s နဲ့ C+r တို့ဘဲဖြစ်ပါတယ်
- C+s ကတော့ ပုံမှန် pointer to bottom lines ရှာသွားမှာဖြစ်ပြီးတော့
-  C+r ကတော့ ပြောင်းပြန် Pointer to to lines ရှာပေးမှာဘဲဖြစ်ပါတယ်

**Force Stop**
Emacs မှာ query တွေရိုက်တာများလို့ cancel လုပ်ချင်တဲ့အခါ C-g ကိုအသုံးပြုပါတယ်

---
**Save Files**
File တွေကို Save ဖို့ဆိုရင်တော့ C-x C-s ကိုအသုံးပြုနိုင်ပါတယ်

---

**Multiple Windows နဲ့ Frames တွေကိုတော့ part II မှာဆက်လက်ဖော်ပြပေးသွားပါမယ်**

Reference learning Emacs Basic
[https://www.gnu.org/software/emacs/manual/html_node/emacs/](https://www.gnu.org/software/emacs/manual/html_node/emacs/)

![]({{site.baseurl}}/img/emacs.png)

