Luontopeli app

Perus koodit kopioitu Villen sivuilta.

Toimii:
-Paikannus
-Askelmittari
-Kamera
-Kuvan tallennus
-Kuvan tunnistus

Ei toimi (ainkaan minulla):
-Reitin piirtäminen

Lisäominaisuudet:
-Extra luontosanoja
-Kuvan jälkeen voi lisätä kommentin/huomion


Projektirakenne
```
app/src/main/java/com/example/luontopeli/
├── data/
│   ├── local/
│   │   ├── entity/          ← NatureSpot, WalkSession
│   │   ├── dao/             ← NatureSpotDao, WalkSessionDao
│   │   └── AppDatabase.kt
│   ├── remote/firebase/     ← AuthManager, FirestoreManager, StorageManager
│   └── repository/          ← NatureSpotRepository, WalkRepository
├── sensor/                  ← StepCounterManager
├── location/                ← LocationManager
├── camera/                  ← CameraScreen
├── ml/                      ← PlantClassifier
├── ui/
│   ├── theme/               ← Color, Theme, Type
│   ├── navigation/          ← Screen, BottomBar, NavHost
│   ├── map/                 ← MapScreen
│   ├── discover/            ← DiscoverScreen
│   └── stats/               ← StatsScreen
├── viewmodel/               ← MapViewModel, CameraViewModel, WalkViewModel,
│                               DiscoverViewModel, StatsViewModel
├── LuontopeliApplication.kt
└── MainActivity.kt
```
