# 🎡 Fahrgeschäfte-Akten (GitHub Pages)

Eine Datenbank für Fahrgeschäfte im Stil einer Patientenakte – ohne eigenen Server.
Die Seite läuft kostenlos auf **GitHub Pages**, die Einträge liegen in `data/eintraege.json`
in diesem Repository. **Jeder darf lesen, nur Personen mit Schreibrechten dürfen eintragen.**
Jede Änderung ist ein Git-Commit (mit Name und Zeit) und steht zusätzlich im „Verlauf“ der Akte.

Felder: Bezeichnung, Typ, Schausteller, Hersteller, Baumaße (L/B/H/Gewicht), Umdrehungen,
Wichtige Infos, Infos, Weitere Infos, Notizen, Eingetragen von.

## Einrichtung (einmalig, ca. 10 Minuten)

1. Auf GitHub ein neues Repository anlegen, **Public**, z. B. `fahrgeschaefte-db`.
2. Alle Dateien aus diesem Ordner hineinhochladen (`index.html`, `config.js`, `data/eintraege.json`, `.nojekyll`, `README.md`).
3. Im Repository: **Settings → Pages → Build and deployment → Source: „Deploy from a branch“**, Branch `main`, Ordner `/ (root)`, speichern.
4. Nach etwa 1–2 Minuten ist die Seite erreichbar unter `https://DEIN-NAME.github.io/fahrgeschaefte-db/`.
5. Mitschreiber hinzufügen: **Settings → Collaborators → Add people**. Die Person muss die Einladung per E-Mail/GitHub annehmen.

## Eintragen (für jeden Mitschreiber)

1. Auf der Seite oben **„Anmelden zum Eintragen“** klicken.
2. Auf GitHub ein Token erzeugen: *Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token*, Haken bei **`public_repo`**, ein Ablaufdatum wählen.
3. Token in die Seite einfügen. Danach erscheinen „+ Neu“, „Bearbeiten“ und „Löschen“.

Hinweis: Mitschreiber auf dem Repository einer anderen Privatperson können laut GitHub-Doku
nur klassische Tokens benutzen (feingranulare Tokens funktionieren dort nicht). Ein klassisches
Token mit `public_repo` darf alle öffentlichen Repositories seines Besitzers ändern –
deshalb: kurzes Ablaufdatum, Token nie weitergeben, auf fremden Geräten „Abmelden“ klicken.
Sicherer: das Repository in einer (kostenlosen) GitHub-Organisation anlegen; dort können
Mitglieder feingranulare Tokens nur für dieses eine Repository mit „Contents: Read and write“ nutzen.

## Gut zu wissen

- Das Repository ist öffentlich: **alle Einträge sind für jeden im Internet sichtbar.**
  Keine privaten Daten (Privatadressen, Telefonnummern) eintragen.
- Wer nicht angemeldet ist, sieht Änderungen erst nach 1–2 Minuten (GitHub baut die Seite neu).
  Angemeldete sehen immer den neuesten Stand.
- Wer gleichzeitig speichert, überschreibt sich nicht: bei einem Konflikt versucht die Seite es automatisch erneut.
- Jeder mit Schreibrechten kann auch Code und Daten direkt im Repository ändern; Git-Verlauf und Rückgängig-Machen helfen dabei.
- Die Datei sollte unter ca. 1 MB bleiben (je nach Eintragslänge einige hundert bis tausend Akten).
- Wenn die Seite nicht unter `…github.io/REPOSITORY/` läuft, Besitzer und Repository in `config.js` eintragen.
