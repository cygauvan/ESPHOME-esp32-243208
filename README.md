
# 🛠️ ESPHome Touch Control Panel – WLED Dashboard

## 🖥️ Interface tactile déportée pour Home Assistant

Ce projet met en œuvre une interface tactile complète basée sur un **ESP32 avec écran ILI9341**, dédiée au **contrôle domotique de plusieurs WLED** via **Home Assistant**. L’objectif est de disposer d’un **tableau de bord mural ou de bureau**, élégant et réactif.

---

## 🎯 Fonctionnalités

- 🟦 Écran ILI9341 SPI 240x320 avec interface graphique personnalisée
- 🖱️ Boutons tactiles (XPT2046) pour le contrôle de :
  - Logo lumineux
  - Bande LED X-Wing
  - Éclairage PC (Victus)
  - LED DeLorean
  - Sabre laser
  - All On/Off synchronisé
- 🌡️ Températures intérieure et extérieure (via Home Assistant)
- ☀️ Icône météo dynamique (basée sur l'état météo)
- 🕒 Horloge temps réel + date
- 🎨 Interface en grille, fond stylisé et icônes néon ON/OFF

---

## 🧩 Matériel utilisé

| Composant         | Référence                            |
|-------------------|--------------------------------------|
| Microcontrôleur   | ESP32-243208 avec ILI9341 intégré     |
| Écran TFT         | ILI9341 240x320 SPI                  |
| Contrôleur tactile| XPT2046                              |
| Home Assistant    | MQTT / API natif ESPHome             |

---

## 📁 Structure des fichiers

- `cyd.yaml` – configuration principale ESPHome
- `images/` – tous les fichiers BMP utilisés (icônes, météo, fond)
- `fonts/` – polices locales (`OpenSans-SemiBold.ttf`) ou Google Fonts (`Roboto`)

---

## ⚙️ Configuration rapide

1. Copier le contenu du fichier `cyd.yaml` dans ton projet ESPHome
2. Placer toutes les images BMP dans `/config/esphome/images/`
3. Placer les polices dans `/config/esphome/fonts/`
4. Adapter :
   - les entités Home Assistant (`light.x_wing_2`, `sensor.capteur_salon_temperature`, etc.)
   - le fond (`bg_full_240x320.bmp`) et les icônes selon ton thème
5. Flasher sur ton ESP32
6. Admire le résultat !

---

## 🖌️ Personnalisation

- Les icônes ON/OFF peuvent être modifiées en `.bmp` (60x60 ou 48x48)
- Le fond peut être changé (type RGB recommandé)
- Les couleurs ON/OFF (orange néon / bleu clair) sont paramétrées via `color:`
- Le style peut être ajusté dans le bloc `lambda:` de `display`

---

## 🤝 Remerciements

Projet conçu avec ❤ autour de la communauté Home Assistant et ESPHome.  
Merci à [WLED](https://kno.wled.ge/) pour leur écosystème LED formidable.
