# 🐧 Arch Light Install GNOME

**Migrer de Windows 7/10 vers Arch Linux (avec GNOME) sur vieux PC fatigué**

---

## ✨ Pourquoi ce projet ?

Tu galères avec un vieux PC sous Windows 7 ou 10 ?  
T’ouvres Chrome et t’as l’impression de lancer GTA 6 ?  
Tu mérites mieux. Ton PC aussi.  
➡️ Passe à **Arch Linux** : rapide, léger, moderne, stylé.

Ce guide est basé sur une installation **réelle**, testée par quelqu’un qui, comme toi, voulait juste un PC fonctionnel sans lag ni prise de tête.

---

## ⚙️ Ce que tu vas faire

✅ Créer une clé USB bootable  
✅ Installer Arch en mode automatique (`archinstall`)  
✅ Utiliser LXQt comme interface temporaire  
✅ Passer à GNOME (version Xorg, pas Wayland)  
✅ Supprimer tout ce qui ne sert à rien  
✅ Avoir une machine propre, rapide, et élégante  
✅ Utiliser moins de **800 Mo de RAM** (GNOME compris !)

---

## 🔧 Prérequis

- Une clé USB de 4 Go minimum
- Un PC sous Windows (même lent)
- Une connexion Wi-Fi
- Du calme, du café, et un minimum de logique

---

## 🧭 Étapes détaillées

### 1. Créer la clé USB bootable
- Télécharge l’ISO d’Arch depuis [archlinux.org]()
- Utilise **Rufus** (Windows) ou `dd` (Linux) pour créer la clé
- Démarre dessus (boot menu)
- ou carrement ton telephone avec lapplication etchdroid
---

### 2. Se connecter au Wi-Fi

- 🧠 Méthode 2 : Connexion directe avec nmcli (mode pro 😎)

🔍 Étape 1 – Voir les réseaux disponibles :

¹nmcli device wifi list¹

📡 Étape 2 – Se connecter :

¹nmcli device wifi connect "Nom_Du_WiFi" password "motdepasse"¹

Exemple :

nmcli device wifi connect "Tenda_B64AF0" password "azerty123" modifer le avec votre wifi
---

### 3. Lancer l’installation automatique

archinstall

    Suis les menus (disque, langue, utilisateur, mot de passe…).
    Choisis LXQt comme environnement de bureau.
    
    ca va prendre un peux de temps sur ssd je sais pas si cest vite perso moi je lai installer su rune cle usb ca march sur tout disque dure ssd cle usb je vous dit on rigole pas votre pc sera comme neuve
---

### 4. Démarrer sous LXQt (style Windows XP)

C’est moche, oui. Mais c’est temporaire.
On va vite le remplacer par GNOME.
---

### 5. Déconnexion → Choisir "GNOME on Xorg"

Depuis l’écran de session, change ton environnement :

✅ GNOME on Xorg
❌ Pas "GNOME (Wayland)" (trop instable sur certains vieux PC)
6. Installer le strict nécessaire

sudo pacman -S gnome-terminal gnome-control-center networkmanager network-manager-applet gnome-bluetooth nautilus firefox

💡 Ajoute gnome-tweaks si tu veux personnaliser les thèmes et polices.
---

### 7. Supprimer LXQt

sudo pacman -Rns lxqt lxqt-panel lxqt-session

Bye bye, Windows XP look 👋
---

### 8. Vérifier la RAM utilisée

free -h

Tu devrais voir autour de 800 Mo utilisés avec GNOME.
Ton PC va respirer.
🎁 Bonus

    Active le mode sombre dans les paramètres GNOME

    Installe Brave ou Firefox pour un navigateur stylé

    Tu peux ajouter btop pour surveiller ta RAM de façon classe

📸 Captures d’écran

📷 À venir ! Tu peux contribuer en envoyant tes avant/après !
❤️ Contribution

- et si ta eu une belle interface avec un minimum de ram utiliser bah bravo a toi tes officielmet lellite de arch et envoi moi un petit retour sur insta : @yanis_archlinux 
