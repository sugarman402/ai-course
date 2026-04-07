# Spotify Top 50 elemzés

## Projekt célja
Ez a projekt egy end-to-end adatelemzési pipeline implementálása, amelynek célja a Spotify globális streaming-adatainak kvantitatív kiértékelése. A `top50.ipynb` notebook-ban a több mint 3500 egyedi rekordot tartalmazó, többdimenziós adathalmazból dolgozunk, ahol minden zenemű 21 különböző akusztikai jellemzővel és metaadat-paraméterrel rendelkezik.

A technikai megvalósítás során a Python data science moduljait alkalmaztuk. A folyamat kritikus pontja az adat-előkészítés (data preprocessing) és a többváltozós statisztikai szűrés volt. A kód célja, hogy a fájlrendszerben tárolt nyers adatforrást a memóriában olyan strukturált formátumba hozza, amely alkalmas a zenei jellemzők és a piaci siker közötti összefüggések feltárására.

A feldolgozási logikát három fő pillérre építettük:
- Adatkezelés: A Pandas könyvtár segítségével az adatokat egy optimalizált DataFrame objektumba töltöttük be. Itt végeztük el a leíró statisztikai elemzést a `describe()` metódussal, amely feltárta a változók eloszlását, az átlagértékeket és a szórásokat. Megállapítottuk például, hogy a globális slágerek tempóeloszlása egy viszonylag szűk tartományban, 121 BPM környékén mutat sűrűsödést.
- Vizuális diagnosztika: A Matplotlib és Seaborn könyvtárakat integráltuk a kódba a változók közötti korrelációk feltérképezéséhez. Ez lehetővé tette a többváltozós összefüggések (például a `Danceability` és a `Popularity` közötti kapcsolat) grafikus validálását közvetlenül a Jupyter notebook környezetben.
- Rendszerarchitektúra és prediktív modellezés: A scikit-learn keretrendszer bevezetése nem csupán előkészület volt, hanem a workflow központi eleme, amely lehetővé tette egy nagy pontosságú regressziós modell implementálását. A rendszer jelenleg 68,11%-os magyarázó erővel képes megbecsülni egy dal várható népszerűségét a zenei paraméterei alapján. A modell tanulsága szerint a hangosság (`Loudness`) és a hangszerelés jellege (`Acousticness`) a legerősebb prediktív faktorok, ami igazolja az eredeti feltételezésünket: a zenei siker paraméterezhető és adatvezérelt módszerekkel előrejelezhető.

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
