# Spotify Top 50 elemzés

## Projekt célja
Ez a projekt egy end-to-end adatelemzési pipeline implementálása, amelynek célja a Spotify globális streaming-adatainak kvantitatív kiértékelése. A `top50.ipynb` notebook-ban a több mint 3500 egyedi rekordot tartalmazó, többdimenziós adathalmazból dolgozunk, ahol minden dalhoz 21 különböző akusztikai jellemző és metaadat-paraméter tartozik.

A Python data science moduljait használjuk az adatelőkészítéstől az elemzésig. A fő célok között szerepel az adatok strukturálása, a leíró statisztika felállítása, a változók közötti korrelációk feltérképezése és egy prediktív regressziós modell kialakítása a dalok népszerűségének becslésére.

A feldolgozás három fő pillérre épül:
- Adatkezelés: Pandas DataFrame segítségével betöltöttük és előkészítettük az adatokat. A `describe()` metódussal feltártuk a változók eloszlását, átlagait és szórásait; például a globális slágerek tempóeloszlása 121 BPM környékén sűrűsödik.
- Vizuális diagnosztika: Matplotlib és Seaborn grafikonokkal vizsgáltuk a változók közötti összefüggéseket, például a `Danceability` és a `Popularity` kapcsolatát.
- Rendszerarchitektúra és prediktív modellezés: scikit-learn segítségével regressziós modellt építettünk, amely jelenleg 68,11%-os magyarázó erővel becsüli a dalok várható népszerűségét a zenei paraméterek alapján. A modell szerint a `Loudness` és az `Acousticness` a legerősebb prediktív faktorok.

## Csapattagok
- Ladóczki-Szabó Ágnes Lilla - B4LQZ2
- Farkas István-DGXP7K
- Németh Tamás - FGCBKF
- Somogyi Dániel - F4HWCL

## Jupyter notebook beállítása

Kövesd az alábbi lépéseket a Jupyter notebook beállításához. A leírás feltételezi, hogy a Python már telepítve van; ha nincs, telepítsd a [python.org](https://www.python.org/downloads/) oldalról.

### 1. lépés: Jupyter telepítése
A `jupyter` parancs akkor érhető el, ha a Jupyter csomagok telepítve vannak a futtatott Python környezetben.
Linuxon (Ubuntu/Debian) használj `python3`-at és pipet:
```bash
python3 -m pip install --user notebook jupyterlab
```
Ha a telepítés után a `jupyter` parancs továbbra sem található, add hozzá a felhasználói binárisok útvonalát a PATH-hoz:
```bash
export PATH="$HOME/.local/bin:$PATH"
```
Ezután indíthatod a Jupyter Notebookot vagy Labot:
```bash
jupyter notebook
jupyter lab
```
Ha pip nincs telepítve, előbb ezt futtasd:
```bash
sudo apt update
sudo apt install python3-pip
```

### 2. lépés: Munkaterület könyvtár létrehozása
Lépj be a már meglévő mappába, ahol az `ipynb` és a `csv` fájl is található:

### 3. lépés: Jupyter indítása
Indítsd el a Jupyter Notebookot vagy JupyterLab-et:
```bash
jupyter notebook
```

Ekkor megnyílik egy böngészőablak a `http://localhost:8888` címen a Jupyter felülettel.
