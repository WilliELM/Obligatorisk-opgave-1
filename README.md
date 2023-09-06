# Obligatorisk-opgave-1


# Øvelse 2 - Post request lav ny mappe
<img width="1512" alt="Skærmbillede 2023-09-06 kl  09 20 46" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/1f11caed-9f52-41cf-802f-6a36343ec334">
[Link til mappe på dropbox] (https://www.dropbox.com/home/TestMappe?di=left_nav_browse)

## Beskriv desuden kort om dette flow er i overenstemmelse med princippet om "uniform interface" i REST principperne, og hvis ikke hvad der så kunne gøres bedre.

Flowet overholder overenstemmelserne om "uniform interface", da en client kan lave en request på et bestemt URL. Requesten kan slette eller oprette information på URL-en samt returnerer dets "state" til clienten via. body content, response og headers. 


# Øvelse 3 - Hent mappe detaljer

Til denne opgave brugte jeg Post request med url-en https://api.dropboxapi.com/2/files/get_metadata

<img width="883" alt="Skærmbillede 2023-09-06 kl  09 40 16" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/e57c697c-b142-4e3d-a136-0a158de5b206">

# Øvelse 4 - Upload en fil

<img width="875" alt="Skærmbillede 2023-09-06 kl  10 01 47" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/24a1f1ef-7b2e-4e7f-baf7-d8f35427b46d">

Ændrede body til binary og vedhæftede min fil.
Derefter tilføjede jeg Dropbox-API-Arg til min headers og {"path": "/TestMappe/screen.png","mode": {".tag": "add"},"autorename": true} for at tilføje min fil til den korrekte path i dropbox.

# Øvelse 5: Slet en fil

<img width="884" alt="Skærmbillede 2023-09-06 kl  10 07 31" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/1c098c92-b3fb-4d4f-b8ad-3a43f85ef503">

Endpoint : https://api.dropboxapi.com/2/files/delete_v2
Slettede filen på denne = "path": "/TestMappe/screen.png"

# Øvelse 7: Søg efter filer
<img width="894" alt="Skærmbillede 2023-09-06 kl  10 13 45" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/200df503-39d0-4a86-8bca-d69a67ae3e89">
Endpoint:
https://api.dropboxapi.com/2/files/search_v2
HTTP-verb:
Post

Jeg søger efter filer ved navn "new" på dropbox. Jeg får returneret alt data om min ene fil new.rtf.

# Øvelse 8: Flyt en fil
<img width="882" alt="Skærmbillede 2023-09-06 kl  10 17 30" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/72daa876-627b-48d3-8c84-c53b8d2fbcb5">

Endpoint:
https://api.dropboxapi.com/2/files/move_v2
HTTP-verb:
Post

Jeg flytter min fil new.rtf fra pathen "/TestMappe/new.rtf" til "/TestMappe/move/new.rtf".

# Øvelse 9: Kopier en fil

<img width="899" alt="Skærmbillede 2023-09-06 kl  10 21 00" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/7f8713ab-f828-4f56-add8-7677c81c210a">

Endpoint:
https://api.dropboxapi.com/2/files/copy_v2
HTTP-verb:
Post

Jeg kopierer min fil fra     "from_path": "/TestMappe/move/new.rtf",
til     "to_path": "/TestMappe/new.rtf"
Dette genererer filen på den nye path, så den ligger begge steder.

# Øvelse 10: Brug JavaScript's Fetch med Dropbox API

<img width="629" alt="Skærmbillede 2023-09-06 kl  10 52 04" src="https://github.com/WilliELM/Obligatorisk-opgave-1/assets/111922379/d498ba2d-5277-4bdb-b94f-64996dec9bc2">

Simpel html side der viser filer og mapper i min dropbox directory ved click på knap.

# Øvelse 11: Er https://api.dropboxapi.com/2/ Restfull or not?

Dropbox-API'et bruger HTTP-requests og json til client requests og returnering af data. Derudover bruger de endpoints til at definere deres forskellige dataressourcer, som man kan tilgå med hhv. GET, POST, DELETE mm. Clienten fortæller derfor hvad api'et skal gøre, og returnerer et svar til clienten. Brugen af det gør Dropbox-apiet til et pålideligt RESTful api.

