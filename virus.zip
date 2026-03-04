#!/bin/bash
# On force l'environnement graphique
export DISPLAY=:0
export DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/$(id -u)/bus

# On utilise le chemin complet pour être sûr
/usr/bin/notify-send "Alerte" "Netanyahou, bombarde cet ordinateur"

# PREUVE : Crée un fichier sur le bureau pour montrer que ça a marché
echo "HACKÉ LE $(date)" > ~/Desktop/ALERTE_OBCNIBOX.txt