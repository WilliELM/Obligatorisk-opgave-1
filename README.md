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

