# 🛒 Ons Boodschappenlijstje

Gezamenlijke boodschappenlijst als web-app: je vrouw stelt de lijst samen (ingrediëntenlijsten, bekende producten, laatste bestelde), jij tikt in de winkel af en ziet alles gesorteerd op looproute per winkel (Lidl + Albert Heijn, Haringvlietplein Zierikzee).

Deze pagina wordt gesynchroniseerd tussen twee telefoons via de privé-repo `boodschappenlijst-data`.

## Eenmalig activeren ( dummyproof)

1. **GitHub Pages aanzetten**: ga naar [Instellingen → Pages](../../settings/pages), kies bij *Branch* `main` en map `/ (root)`, en druk op **Save**. Na ±1 minuut staat de app live op:
   ```
   https://jkarthaus-netizen.github.io/boodschappenlijst/
   ```
2. **Token maken voor synchronisatie**: op de computer → github.com → rechtsboven je foto → *Settings* → *Developer settings* → *Personal access tokens* → *Fine-grained tokens* → *Generate new token*:
   - Repository access: **Only select repositories** → `boodschappenlijst-data`
   - Permissions → Repository permissions → **Contents: Read and write**
   - Genereer en kopieer de token (begint met `github_pat_`).
3. **Op beide iPhones**: open de link uit stap 1 in Safari → deel-menu → **Zet op beginscherm**. De app staat nu met eigen icoon op het beginscherm en opent volledig scherm. Tik in de app rechtsonder op ⋯ → **🔄 Synchroniseren tussen telefoons** → plak de token → *Verbinding testen en gebruiken*.
4. Bestaande gegevens meenemen: in de oude app ⋯ → **Gegevens exporteren**, in deze app ⋯ → **Gegevens importeren**.

## Werking

- Elke wijziging wordt na ±2 seconden naar de privé-opslag gestuurd; het andere toestel haalt elke 5 seconden de laatste stand op.
- Werkt ook even zonder internet: alles wordt bijgewerkt zodra er weer verbinding is.
- De groene stip rechtsonder geeft de synchronisatiestatus aan (groen = OK, oranje = bezig/wacht, rood = mislukt).
