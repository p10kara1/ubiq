#Timeline Of Eurozone Crisis - Twitter Visualisation
Παναγιώτης Μπλέτσος
Π2011030

###[Timeline Of Eurozone Crisis - Website](http://83.212.123.239/d3)

###[Source Code](https://github.com/Panagiotis-Bletsos/Timeline_Of_Eurozone_Crisis-Twitter_Visualization)

##Tελική Αναφορά

###Εισαγωγή

Η εργασία πραγματεύεται την οπτικοποίηση των tweets (Twitter Visualization) που αφορούν την Ευρωπαϊκή Κρίση. Πιο συγκεκριμένα, η εφαρμογή λαμβάνει tweets που έχουν το hashtag “eurocrisis” ή “eurozonecrisis” και τα προβάλει σε χάρτη ανάλογα με την τοποθεσία του χρήστη που έκανε το tweet. Επιπλέον η εφαρμογή διαθέτει timeline ώστε ο χρήστης να μπορεί να επιλέξει συγκεκριμένη χρονική περίοδο για τα tweets που εμφανίζονται στον χάρτη. Σκοπός της εφαρμογής είναι να δείχνει στον χρήστη με εύκολο τρόπο σε ποιες χώρες συζητιέται περισσότερο το θέμα της Ευρωπαϊκής κρίσης και σε ποια χρονική περίοδο (π.χ. διεξαγωγή Eurogroup, συναντήσεις πολιτικών αρχηγών κτλ.).

###Επιλογή εργαλείων

Τα εργαλεία που χρησιμοποιήθηκαν για την ανάπτυξη της εφαρμογής είναι η γλώσσα php τα frameworks D3.js, Leaflet.js και Mapbox.js, το Rest API του Twitter και το Geocode API της Google. Πιο συγκεκριμένα για την δημιουργία του backend της εφαρμογής χρησιμοποιήθηκε η γλώσσα php ώστε να γίνει το αίτημα στο Twitter και να λάβει τα tweets με το Rest API και να μετατρέψει τις τοποθεσίες των χρηστών σε γεωγραφικές συντεταγμένες με το Geocode API της Google. Για την διεπαφή χρήστη χρησιμοποιήθηκαν τα frameworks D3.js, για την δημιουργία του timeline και την επεξεργασία των δεδομένων, Leaflet.js για την ομαδοποίηση των markers στον χάρτη και Mapbox.js για την δημιουργία του χάρτη και την τοποθέτηση των markers και javascript για την δημιουργία του ημερολογίου.

###Διαδικασία ανάπτυξης

Το backend της εφαρμογής λαμβάνει τα tweets από το Rest API του Twitter και στην συνέχεια μετατρέπει με το Geocode API της Google τις τοποθεσίες των χρηστών που έκαναν τα tweets σε γεωγραφικές συντεταγμένες (εάν κάποιος χρήστης δεν έχει ορίσει τοποθεσία ή το Geocode API δεν μπορεί να βρει τις γεωγραφικές συντεταγμένες τότε το tweet αυτό αγνοείται). Στην συνέχεια αποθηκεύονται με την μορφή geojson σε ένα αρχείο το κείμενο του tweet, το όνομα και το username του χρήστη, οι γεωγραφικές συντεταγμένες της τοποθεσίας του καθώς και η ημερομηνία που έγινε το tweet.
To frontend της εφαρφμογής δημιουργεί τον χάρτη με το Mapbox.js στην συνέχεια ανοίγει το αρχείο που έχουν αποθηκευτεί τα tweets, τοποθετεί τα markers στον χάρτη και δημιουργεί το timeline ή το ημερολόγιο αν η εφαρμογή ανοίξει σε οθόνη με width<1000px (πχ. smartphone, tablet).

Η εφαρμογή ανανεώνεται ανά 1 ώρα.

###Διάγραμμα λειτουργίας συστήματος

![Διάγραμμα λειτουργίας συστήματος](https://raw.githubusercontent.com/courses-ionio/ubiq/master/projects_2015/Π2011030/img/ubiq-di.001.png)

###Συμπεράσματα

Όπως φαίνεται και από τα screenshots η εφαρμογή δείχνει πως ο κύριο όγκος των tweets που αναφέρονται στην Ευρωπαϊκή κρίση είναι από την Ευρώπη και την Αμερική. Ακόμη δεν έχει υπάρξει κάποιο γεγονός (π.χ. διεξαγωγή Eurogroup, συναντήσεις πολιτικών αρχηγών κτλ.) οπότε δεν μπορούμε να ξέρουμε αν το timeline έχει κάποια χρησιμότητα.

Όσον αφορά την σχεδίαση της εφαρμογής ο όγκος των tweets θα αυξηθεί πολύ σε ένα χρόνο και μικρές συσκευές όπως κινητά θα είναι δύσκολο να διαχειριστούν τέτοιο όγκο πληροφορίας, οπότε μελόντικα η εφαρμογή θα αλλάξει στο να δείχνει τα tweets ανά μήνα και όχι όλα μαζί.

###Screenshots

![Screenshot-1](https://raw.githubusercontent.com/courses-ionio/sw/master/projects_2015/Π2011030/img/Screen%20Shot%202015-05-31%20at%2000.48.13.png)

![Screenshot-2](https://github.com/courses-ionio/sw/blob/master/projects_2015/Π2011030/img/Screen%20Shot%202015-05-31%20at%2000.48.29.png)

![Screenshot-1-Mobile](https://raw.githubusercontent.com/courses-ionio/ubiq/master/projects_2015/Π2011030/img/iOS%20Simulator%20Screen%20Shot%202015%20-%2019.27.34.png)

![Screenshot-2-Mobile](https://raw.githubusercontent.com/courses-ionio/ubiq/master/projects_2015/Π2011030/img/iOS%20Simulator%20Screen%20Shot%202015%20-%2019.28.06.png)

![Screenshot-3-Mobile](https://github.com/courses-ionio/sw/blob/master/projects_2015/Π2011030/img/Screen%20Shot%202015-05-31%20at%2000.48.29.png)

![Screenshot-4-Mobile](https://raw.githubusercontent.com/courses-ionio/ubiq/master/projects_2015/Π2011030/img/iOS%20Simulator%20Screen%20Shot%202015%20-%2019.28.26.png)