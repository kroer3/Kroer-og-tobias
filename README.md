
# Project Title

et vignere enkryptions og dekryptions program der kan kryptere og dekryptere beskeder med et vis kodeord


process:

Start på projekt 

 

Opret repository i Unord community 

 

Lav simpel diagram hvordan programmet skal virke 

 

Start krypterings script 

Start dekrypterings script 

 

Gør scripts færdig og lav menu



pseudokode:

Funktion: encrypt_message

Input: message (tekst), keyword (tekst)
Output: encrypted_message (tekst)
Konverter message og keyword til store bogstaver.
Sæt keyword_index til 0.
For hver letter i message:
Hvis letter findes i ALFABETET:
Find row som indeks for keyword[keyword_index % længde(keyword)] i ALFABETET.
Find col som indeks for letter i ALFABETET.
Tilføj VIGENERE_TABLE[row][col] til encrypted_message.
stig keyword_index med 1.
Ellers:
Tilføj letter direkte til encrypted_message.
Returner encrypted_message.
Funktion: decrypt_message

Input: encrypted_message (tekst), keyword (tekst)
Output: decrypted_message (tekst)
Konverter encrypted_message og keyword til store bogstaver.
Sæt keyword_index til 0.
For hver letter i encrypted_message:
Hvis letter findes i ALFABETET:
Find row som indeks for keyword[keyword_index % længde(keyword)] i ALFABETET.
Find col som indeks for letter i VIGENERE_TABLE[row].
Tilføj ALFABETET[col] til decrypted_message.
Øg keyword_index med 1.
Ellers:
Tilføj letter direkte til decrypted_message.
Returner decrypted_message.
Funktion: main_menu

Loop indtil brugeren vælger at afslutte:
Vis menuen:
"1. Krypter en besked"
"2. Dekrypter en besked"
"3. Afslut"
Modtag brugerens valg.
Hvis valg er '1':
Modtag message og keyword.
Kald encrypt_message og vis resultatet.
Hvis valg er '2':
Modtag encrypted_message og keyword.
Kald decrypt_message og vis resultatet.
Hvis valg er '3':
Afslut loopet.
Ellers:
Vis "Ugyldigt valg."
Start programmet:

Kald main_menu.
