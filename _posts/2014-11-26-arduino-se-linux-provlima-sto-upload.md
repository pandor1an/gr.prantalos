---
layout: post
title:  "Arduino σε Linux: Πρόβλημα στο Upload"
created:  2014-11-26 00:00:00 +0200
updated:  2021-03-19 00:00:00 +0200
categories: software
code_highlight: ["bash"]
---
Αν κατά το upload του sketch σου, σού εμφανίζεται μήνυμα ότι δεν βρέθηκε το 
Arduino στην επιλεγμένη θύρα, τότε κλείσε το Arduino IDE, άνοιξε ένα terminal 
και γράψε την παρακάτω εντολή:

{% highlight bash %}
sudo arduino
{% endhighlight %}

Στην συνέχεια πήγαινε στο Tools>Serial Ports και επέλεξε την θύρα που σου έχει. 
Αν σου έχει πάνω από μία θύρες, δοκίμασέ τες όλες μέχρι να βρεις την σωστή.