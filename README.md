# PARKETAR STREGOL, sajt

## Šta je u folderu
- `index.html`: sajt
- `support.js`: JavaScript bez koga sajt ne radi, ne brisati
- `image-slot.js`: prikaz fotografija
- `assets/images/`: fotografije (spisak imena je u assets/images/README.md)
- `.nojekyll`: potreban za GitHub Pages
- `SADRZAJ.md`: svi tekstovi sa sajta i šta klijent još treba da dostavi

## Objava na GitHub Pages
1. Napravite novi repozitorijum na GitHub-u.
2. Prebacite sve iz ovog foldera u koren repozitorijuma (Add file, pa Upload files, ili git push).
3. Otvorite Settings, pa Pages. Za Source izaberite Deploy from a branch, granu `main` i folder `/ (root)`, pa Save.
4. Posle minut-dva sajt je na `https://<korisnik>.github.io/<repo>/`.

Sajt ne radi ako otvorite `index.html` dvoklikom. Na računaru ga pokrenite preko servera, npr. `npx serve .` ili `python -m http.server`.

## Kontakt forma
Forma ne šalje ništa dok je ne povežete sa servisom za slanje. Do tada posle klika na dugme ispiše da još nije povezana i uputi na Instagram.

Povezivanje preko Formspree-a:
1. Napravite formu na formspree.io i kopirajte njenu adresu (https://formspree.io/f/XXXX).
2. U `index.html` nađite `"formEndpoint"` u data-props JSON-u i umesto praznog `"default":""` upišite tu adresu.

## Oznake za klijenta
Isprekidane oznake („klijent treba da dostavi/potvrdi“) se gase u `index.html`: u data-props JSON-u kod `"showNotes"` promenite `"default":true` u `false`.
