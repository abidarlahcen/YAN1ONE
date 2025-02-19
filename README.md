# Politique de Confidentialité de YAN1ONE

📅 **Dernière mise à jour** : [Date]  
🔗 **Lien vers la politique** : [https://votresite.com/privacy](https://votresite.com/privacy)

---

## 📸 Accès à la Caméra
L'application utilise l'accès à la caméra **uniquement** pour :
- [Fonctionnalité 1] (ex: scanner des codes QR).
- [Fonctionnalité 2] (ex: appliquer des filtres en temps réel).

**Données collectées** :
- Les images/vidéos sont traitées **localement sur l'appareil**.
- Aucune donnée brute de la caméra n'est stockée ou partagée.

---

## 🔒 Sécurité des Données
| Type de Donnée       | Stockage          | Partage avec des Tiers |
|----------------------|-------------------|-------------------------|
| Images de la caméra  | Aucun stockage    | Non                     |
| Métadonnées          | Chiffrées (SSL)   | Uniquement avec consentement |

---

## 🛠️ Implémentation Technique
### Demande de Permission (Kotlin)
```kotlin
val requestPermissionLauncher = registerForActivityResult(
    ActivityResultContracts.RequestPermission()
) { isGranted ->
    if (isGranted) {
        // Accès autorisé
    } else {
        showRationaleDialog()
    }
}

fun checkCameraPermission() {
    if (ContextCompat.checkSelfPermission(this, Manifest.permission.CAMERA) 
        != PackageManager.PERMISSION_GRANTED) {
        requestPermissionLauncher.launch(Manifest.permission.CAMERA)
    }
}
