# Krisi’s Sweet Studio – CMS-Version

Diese Version basiert **optisch auf Version 7**. Das Design bleibt im `index.html`; die Inhalte, die du später selbst ändern möchtest, liegen in `content/` und werden von Pages CMS bearbeitet.

## Was du später ohne Code ändern kannst

- Starttext und Lotus-Hauptbild
- Kategorien/Kreationen
- Galerie: Bilder, Bildtitel und **Reihenfolge**
- Kontakttexte, E-Mail, Instagram- und TikTok-Link
- Ablauf, Kurzinfos und FAQ
- Impressum-/Datenschutztexte
- Footer-Texte

## Dateien

- `index.html` – deine Website und das bestehende Design
- `content/site.json` – Texte und allgemeine Website-Inhalte
- `content/gallery.json` – Galeriebilder in der angezeigten Reihenfolge
- `media/images/` – alle Bilder
- `.pages.yml` – Konfiguration für Pages CMS
- `backup/krisis_sweet_studio_v7_singlefile.html` – unveränderte Sicherung von Version 7

## Einmalige Einrichtung

### 1. GitHub
1. Kostenloses GitHub-Konto erstellen/anmelden.
2. Ein neues Repository anlegen, z. B. `krisis-sweet-studio`.
3. **Den Inhalt dieses Ordners** in das Repository hochladen. Wichtig: `index.html` und `.pages.yml` müssen direkt oben im Repository liegen.

### 2. Pages CMS
1. `https://app.pagescms.org` öffnen.
2. Mit GitHub anmelden.
3. Die Pages-CMS-GitHub-App für dein Repository erlauben.
4. `krisis-sweet-studio` öffnen.
5. Danach erscheinen zwei Bereiche: **Website-Inhalte** und **Galerie-Bilder**.
6. Änderungen dort speichern. Pages CMS schreibt sie direkt in dein GitHub-Repository.

### 3. Cloudflare Pages
1. Kostenloses Cloudflare-Konto erstellen/anmelden.
2. **Workers & Pages → Create application → Pages → Import an existing Git repository**.
3. Dein GitHub-Repository auswählen.
4. Production branch: `main`.
5. Framework preset: keines / None.
6. Build command: `exit 0` (oder leer, falls die Oberfläche das zulässt).
7. Build output directory: `.`
8. Deploy starten.

Danach erhältst du eine kostenlose Adresse wie `krisis-sweet-studio.pages.dev`. Jede gespeicherte Änderung in Pages CMS landet in GitHub und Cloudflare Pages veröffentlicht sie automatisch neu.

## Wichtig zum Bearbeiten

Die **Reihenfolge der Galerie** wird durch die Reihenfolge der Einträge in `Galerie-Bilder` bestimmt. Mini Pavlovas steht im Startzustand an erster Stelle. Wenn du später einen Eintrag verschiebst, ändert sich auch die Reihenfolge auf der Website.

Die Website enthält zusätzlich den kompletten aktuellen Inhalt als visuellen Fallback im `index.html`. Dadurch bleibt Version 7 als Sicherheitsnetz erhalten, falls die JSON-Dateien lokal einmal nicht geladen werden können.
