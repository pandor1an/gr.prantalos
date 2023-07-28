---
layout: post
title:  Όταν ένας driver, σου κάνει την ζωή πατίνι
created:  2014-11-23 00:00:00 +0200
updated:  2021-03-19 00:00:00 +0200
categories: software
code_highlight: ["bash"]
---
Είπα λοιπόν να προσπαθήσω για μία ακόμη φορά να έχω Linux λειτουργικό ως κύριο
μετά από χρόνια. Επειδή μου αρέσει ιδιαιτέρως το xfce 
και λόγω της δημοτικότητας του Ubuntu, αποφάσισα να βάλω
Xubuntu 14.04 τόσο στο laptop όσο και στο desktop.

Στο laptop όλα λειτούργησαν τέλεια, στο desktop όμως όταν προσπαθούσα να 
κλείσω/επανεκκινήσω το μηχάνημα, φαινόταν το μήνυμα mount: / is busy και δεν
έκλεινε ποτέ.

Στην αρχή υποπτευόμουν ότι οι proprietary drivers της AMD για την κάρτα γραφικών
έκαναν την δουλειά, οπότε έβαλα τους open-source αλλά το πρόβλημα παρέμεινε.

Τελικά βρήκα ότι έφταιγαν οι drivers για το wifi (broadcom chipset) οπότε
χρησιμοποίησα τις παρακάτω εντολές

{% highlight bash %}
sudo apt-get remove --purge bcmwl-kernel-source
sudo apt-get install linux-firmware-nonfree
{% endhighlight %}

όπως πρότεινε ο [drphysic](http://ubuntuforums.org/member.php?u=706802) σε 
[αυτό το post](http://ubuntuforums.org/showthread.php?t=2217602&page=2&p=13006373#post13006373)
και όλα είναι πλέον ΟΚ.