# panic-mode
panic-mode pour eviter les parents et les boss


Voici le code a copier-coller dans un editeur de code (vs code ou autre) ca peu etre dans note mais n oubliez pas de changer l'extension en .py apres.


voici le code :

import os
import webbrowser
from pynput import keyboard

def panic():
    print("🚀 Panic Mode : Nettoyage en cours...")
    
    # Liste des logiciels à fermer instantanément
    logiciels = ["discord.exe", "firefox.exe", "spotify.exe"]
    
    for app in logiciels:
        os.system(f"taskkill /f /im {app}")
    
    # Ouverture du site de secours
    webbrowser.open("https://fr.wikipedia.org/wiki/Physique_quantique")

# Déclencheur sur la touche F12
print("Script actif. Appuie sur F12 pour tout masquer.")
with keyboard.GlobalHotKeys({'<f12>': panic}) as h:
    h.join()


Add : vous pouvez changer les programme à fermer et l url du site a ouvrir en fonction de vos preferences
