# pgAdmin 4

Questa è una semplice immagine di Docker per eseguire pgAdmin4 in un container.
La configurazione è settata per lanciare la modalità "Desktop", quindi senza autenticazione.
Per vedere la conf applicata visionare il "config_distro.py"

Viene utilizzato un utente senza privilegi e la porta di default in ascolto è la 5050 (sovrascrivibile).

# switch to SERVER MODE

Passare le seguienti variabili d'ambiente:

PGADMIN_SETUP_SERVER_MODE = True

PGADMIN_SETUP_EMAIL = mail di autenticazione (obbligatorio se SERVER MODE, formato mail)

PGADMIN_SETUP_PASSWORD = password di autenticazione (obbligatorio se SERVER MODE)
