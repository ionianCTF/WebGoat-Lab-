# WebGoat-Lab-

# 🛡️ Εργασία: Ανάλυση Τρωτότητας με GitHub Security Code Scanning στο WebGoat

## 🎯 Σκοπός
- Η εργασία αυτή έχει στόχο να εξοικειωθείτε με τις τεχνικές στατικής ανάλυσης κώδικα και τη χρήση του εργαλείου **Security Code Scanning** του GitHub. Το αντικείμενο της μελέτης είναι η ευάλωτη εφαρμογή **WebGoat**. 
- Δοκιμάστε επίσης να κάνετε εγκατάσταση το WebGoat (Docker Based) και να αναγνωρίσετε τις ευπάθειες που βρίσκονται στα βήματα 00-HTTP-Basics κλπ).

---
Το WebGoat είναι ένα εκπαιδευτικό εργαλείο που αναπτύχθηκε από το OWASP (Open Web Application Security Project), έναν οργανισμό που προωθεί την ασφάλεια εφαρμογών ιστοσελίδων. Σκοπός του είναι να δώσει στους χρήστες (κυρίως προγραμματιστές, επαγγελματίες ασφαλείας, ή φοιτητές) την ευκαιρία να μάθουν πώς να εντοπίζουν και να εκμεταλλεύονται ευπάθειες σε εφαρμογές, αλλά και πώς να τις διορθώνουν.

## 🔹 Μέρος Α: Κλωνοποίηση του αποθετηρίου και Ενεργοποίηση Code Scanning

1. **Κλωνοποίηση του αποθετηρίου WebGoat:**
   - Μεταβείτε στο GitHub repository: [https://github.com/WebGoat/WebGoat](https://github.com/WebGoat/WebGoat)
   - Κάντε *Clone* του αποθετηρίου στο προσωπικό σας GitHub λογαριασμό.
   - Κλωνοποιήστε το τοπικά:
     ```bash
     git clone https://github.com/<το-username-σας>/WebGoat.git
     cd WebGoat
     ```

2. **Ενεργοποίηση GitHub Security Code Scanning:**
   - Στο forked repository:
     - Επιλέξτε **"Security"** → **"Code scanning alerts"**
     - Πατήστε **"Set up code scanning"**
     - Επιλέξτε το πρότυπο **"CodeQL Analysis"**
     - Πατήστε **"Set up this workflow"** και αποθηκεύστε το προτεινόμενο `.yml` αρχείο (π.χ. `.github/workflows/codeql.yml`)
   - Κάντε commit και push τις αλλαγές.

---

## 🔹 Μέρος Β: Ανάλυση και Αναφορά Αποτελεσμάτων

1. **Ανάλυση των Alerts:**
   - Αφού ολοκληρωθεί ο έλεγχος, μεταβείτε στο **Security > Code scanning alerts**
   - Καταγράψτε **όλες τις τρωτότητες με βαθμό “critical”**
   - Επιλέξτε **τουλάχιστον 3 τρωτότητες “high” severity**

2. **Σύνταξη Αναφοράς (vulnerability_report.md):**
   Περιλάβετε:
   - Πίνακα των ευρημάτων με τις στήλες:
     | Severity | Είδος Ευπάθειας | Αρχείο | Περιγραφή | Σύνδεσμος |
   - Περιγραφή κάθε ευπάθειας
   - Προτεινόμενα μέτρα αντιμετώπισης

---

## 🔹 Μέρος Γ: Εφαρμογή Διορθώσεων και Επαναξιολόγηση

1. **Υλοποίηση διορθώσεων:**
   - Τροποποιήστε τον κώδικα για να αντιμετωπίσετε κάθε μία από τις επιλεγμένες ευπάθειες

2. **Επαλήθευση με επανέλεγχο:**
   - Κάντε push τις αλλαγές και περιμένετε να εκτελεστεί ξανά ο έλεγχος
   - Ελέγξτε εάν τα alerts έχουν επιλυθεί

3. **Ολοκλήρωση αναφοράς:**
   - Προσθέστε ενότητα **“Κατάσταση μετά τη διόρθωση”** στο `vulnerability_report.md`
   - Αναφέρετε ποια προβλήματα επιλύθηκαν
   - Γράψτε το δικό σας VulnerabilityReport.md με βάση το template που σας δίνεται σε αυτό το αποθετήριο

---
