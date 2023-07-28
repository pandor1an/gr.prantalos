---
layout: post
title:  Windows 10 Upgrade, με το ζόρι...
created:  2015-07-29 00:00:00 +0200
updated:  2021-03-19 00:00:00 +0200
categories: software
thumb: I4LYzzI
code_highlight: ["command-line"]
---

29 Ιουλίου σήμερα, η ημέρα που το νέο λειτουργικό της Microsoft, Windows 10,
υποτίθεται ότι θα είναι διαθέσιμο για λήψη ώστε οι έχοντες Windows 7, 8 και 8.1
να μεταπηδήσουμε δωρεάν (περισσότερα εδώ) στο 10. Κι όμως πολλοί ακόμη
περιμένουμε. Όχι για πολύ όμως. Δες εδώ πως με 2 εντολές θα "υποχρεώσεις" την
Microsoft να κατεβάσει το 10 στο PC σου

{% include alert.html type="info" message="Το παρακάτω άρθρο είχε αρχικά
δημοσιευτεί στο AllTheGeek.gr"%}

Για να μην γκρινιάζουμε μόνο, αξίζει να σημειωθεί ότι το δωρεάν upgrade είναι
ένα επίποπονο task για τους servers της Microsoft και λογικά θα επιτρέπουν την
λήψη ανά waves για να μην υπάρχει υπερβολική φόρτιση. Λογικό και θεμιτό από
μεριάς Microsoft.

Έχοντας αυτό στο μυαλό, μπορείτε να περιμενέτε υπομονετικά να έρθει η σειρά σας.
Για τους υπόλοιπους που σαν και εμένα δεν τους αρέσει να περιμένουν σε ουρές
υπάρχει ένα πανεύκολο bypass της αναμονής.

Το παρακάτω το δοκίμασα σε Windows 8.1 και τα screenshots είναι από εκεί, αλλά
λογικά δουλεύει και σε Windows 7.

# Βήμα 1 - Εκκαθάριση της cache του Windows Update

Για να είμαστε 100% σίγουροι, θα πρέπει να σβήσουμε την cache του Windows Update
πριν ξεκινήσουμε. Για να το κάνουμε αυτό, πάμε στο

{% highlight command-line %}C:\Windows\SoftwareDistribution\{% endhighlight %}

και σβήνουμε το φάκελο Download.


# Βήμα 2 - Άνοιγμα του Windows Update for Desktop

 Για αρχή θα πρέπει να ανοίξουμε το Windows Update. Επειδή είμαστε σε Windows
 8.1 θα πρέπει να σημειωθεί ότι θα πρέπει να ανοίξουμε την Desktop έκδοση και
 όχι αυτή του Metro.

Για να γίνει αυτό, ενώ είστε στο desktop, πατήστε το Windows Key (αυτό με την
σημαιούλα αριστερά από το space) και γράψτε Windows Update. Επιλέξτε το σχετικό
link:

{% include imgur.html id="gvFJcfW" thumbnail="enlarge" %}

Μόλις ανοίξει το Windows Update **ΔΕΝ ΚΑΝΟΥΜΕ ΤΙΠΟΤΑ**

# Βήμα 3ο - Άνοιγμα του cmd ως Διαχειριστής 

Όπως και πριν πατάμε Windows Key στο desktop και γράφουμε cmd, αλλά αυτή τη φορά
κάνουμε δεξί κλικ στο Command Line και πατάμε Run as Administrator:

{% include imgur.html id="9RF8jff" thumbnail="enlarge" %}

 Στο παράθυρο που θα ανοίξει γράφουμε (χωρίς να πατήσουμε ENTER)

{% highlight command-line %}wuauclt.exe /updatenow{% endhighlight %}

{% include imgur.html id="sH6RZS9" thumbnail="enlarge" %}

# Βήμα 4ο - Εκκίνηση του update

Επιστρέφουμε στο παράθυρο του Windows Update που ανοίξαμε στο Βήμα 2 και πατάμε
Check for updates:

{% include imgur.html id="GJGrebf" thumbnail="enlarge" %}

Μόλις αρχίσει η αναζήτηση για updates, πηγαίνουμε πίσω στο cmd και πατάμε ENTER.
Αν όλα τα κάναμε σωστά, η λήψη του Windows 10 ξεκινά:

{% include imgur.html id="upVUNno" thumbnail="enlarge" %}

# Πηγές

* https://www.reddit.com/r/Windows10/comments/3ezkrm/its_1201_eastern_time/

* http://venturebeat.com/2015/07/28/how-to-force-windows-to-start-downloading-the-windows-10-update-files/