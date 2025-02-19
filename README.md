# Politique de Confidentialité de YAN1ONE

📅 **Dernière mise à jour** : [Date]  
🔗 **Lien vers la politique** : https://github.com/abidarlahcen/YAN1ONE

---

## 📸 Accès à la Caméra
L'application utilise l'accès à la caméra **uniquement** pour :
- [Fonctionnalité 1] (ex: scanner des codes QR).

**Données collectées** :
- Les images/vidéos sont traitées **localement sur l'appareil**.
- Aucune donnée brute de la caméra n'est stockée ou partagée.

---

## 🔒 Sécurité des Données
| Type de Donnée       | Stockage          | Partage avec des Tiers |
|----------------------|-------------------|-------------------------|
| Images de la caméra  | Aucun stockage    | Non                     |

---



fun checkCameraPermission() {
    if (ContextCompat.checkSelfPermission(this, Manifest.permission.CAMERA) 
        != PackageManager.PERMISSION_GRANTED) {
        requestPermissionLauncher.launch(Manifest.permission.CAMERA)
    }
}
