	AIgri
  
	Ο «ψηφιακός γεωπόνος» αποτελείται από ανατροφοδοτούμενο νευρωνικό δίκτυο, συνδυάζοντας τεχνικές data mining. 
	Σε προγραμματιστικό επίπεδο, είναι δομημένος σε Visual Studio 2017 στη γλώσσα προγραμματισμού Visual C#. 
	Για την εκτέλεση του, όντας στο επόμενο στάδιο μετά το διάβασμα της εικόνας για το οποίο απαιτείται υπολογιστική
	όραση και έχει υλοποιηθεί σε άλλη φάση στον ίδιο διαγωνισμό φορτώνοντας 
	API IBM Watson για επίδειξη, απαιτείται ένα αρχείο της μορφής:
	0.45696
	0.245668
	0.956658
	
	Τα παραπάνω αντιστοιχούν σε τριπλέτα (R,G,B), ενώ υπό κανονικές συνθήκες τα ίδια δεδομένα δίνονται απευθείας
	από το διάβασμα της εικόνας, με χρήση ενός αλγορίθμου υπολογιστικής όρασης.
	Μετά το διάβασμα του αρχείου, ο αλγόριθμος προσπαθεί να ομαδοποιήσει τα χρώματα, 
	λαμβάνοντας υπόψιν τις αποχρώσεις του φυτού που μας ενδιαφέρει, ώστε να απομονωθεί η κωδικοποίηση του φυτού 
	από το αδιάφορο για αυτόν περιβάλλον.
	Έχοντας εκπαιδεύσει το ανατροφοδοτούμενο νευρωνικό δίκτυο το οποίο βρίσκεται σε πρώιμο στάδιο λόγω έλλειψης χρόνου 
	και το οποίο βασίστηκε σε διαφορετική version, προερχόμενη από το crowdhackathon #insurance 2019, προσπαθεί να συγκρίνει
	την κατάσταση του φυτού τόσο σε επίπεδο οπτικής όσο και σε επίπεδο υπέρυθρης λήψης, 
	με καταστάσεις υγειών φυτών στα οποία έχει ήδη εκπαιδευτεί.


Πώς λειτουργεί το πρόγραμμα:

	Ο προγραμματιστής πρέπει να θέσει το σωστό path του υπολογιστή στο οποίο βρίσκεται το .txt.
	Για λόγους διευκόλυνσης υπάρχει το aa.txt μαζί με τον κώδικα. 
	Τρέχουμε το πρόγραμμα πατώντας το Start και αυτό που μας επιστρέφει είναι ένα ομαδοποιημένο Dataset.
	Οι κατηγορίες στις οποίες θα κατηγοριοποιηθούν τα data είναι:
		1) το αναγκαίο περιβάλλον (εν προκειμένω το φυτό που μας απασχολεί)
		2) το αδιάφορο περιβάλλον (όπως χώμα) και
		3) το μη αναγκαίο περιβάλλον το οποίο όμως παρουσιάζει συσχετίσεις με το αναγκαίο περιβάλλον
		και είναι αυτό που δυσκολεύει την ομαδοποίηση (το τελευταίο μάλιστα είναι το βασικότερο σημείο διαχωρισμού).
	
	
Ακρίβεια Αλγορίθμου:

	Σε μια ολοκληρωμένη υλοποίηση, το νευρωνικό δίκτυο έχει Accuracy ~98%, Precision ~0,9 και Recall 1,000 το οποίο είναι βέλτιστο αν αναλογιστεί κανείς ότι οι μέχρι στιγμής προσπάθειες για αναγνώριση της υγείας του φυτού (βασισμένες σε επιστημονική έρευνα) έιχαν ακρίβεια ελάχιστα μεγαλύτερη από 80%. 
	Όπως γίνεται σαφές, ο αλγόριθμος μας με κατάλληλη σύνδεση και το σωστό όγκο δεδομένων για εκπαίδευση μπορεί να ξεπεράσει κατά πολύ μεγάλα ποσοστά αυτήν την επίδοση και να βελτιώσει τους χρόνους έως και 15%.
