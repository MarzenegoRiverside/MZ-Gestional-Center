# Gestionale MARZENEGO RIVERSIDE

## 1. Regole Firestore (progetto mz-gestional-center)
Console Firebase → Firestore Database → Regole → incolla e pubblica:

    rules_version = '2';
    service cloud.firestore {
      match /databases/{database}/documents {
        match /{document=**} { allow read, write: if true; }
      }
    }

(Il vecchio progetto marzenego-2e266 deve già consentire la lettura: è così, perché le vecchie PWA lo usano.)

## 2. Pubblicazione su GitHub Pages
1. Crea un repository e carica TUTTI i file di questa cartella (index.html, manifest.json, sw.js, logo.png, icon-192.png, icon-512.png).
2. Settings → Pages → Branch: main, cartella /(root) → Save.
3. Apri l'indirizzo https://<utente>.github.io/<repo>/ e accedi (al primo accesso viene creata l'utenza admin).
4. Dal browser: "Installa app" per averla come PWA.
