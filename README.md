# OpenStreetMap to GeoTIFF for Switzerland

In this small project, we leverage open data to extract feature maps. We rely on [OpenStreetMap](https://www.openstreetmap.org/) to extract topographical features at a 100x100 meters resolution. The output is stored as GeoTIFF, for convenience.


## Getting started

If you us Conda, an [`environment.yml`](environment.yml) is provided:

```
conda env create --file environment.yml
```

Alternatively, you can install [`requirements.txt`](requirements.txt) using Pip. The [Cairo](https://www.cairographics.org/) library must be installed separately, typically using a package manager; here is an example on Ubuntu:

```
sudo apt-get install libcairo2
pip install -r requirements.txt
```

In order to download an extract of OpenStreetMap data for Switzerland, we rely on [Geofabrik GmbH](https://download.geofabrik.de/europe/switzerland.html) dumps, which are updated daily. To proceed, download [`switzerland-latest-free.shp.zip`](https://download.geofabrik.de/europe/switzerland-latest-free.shp.zip) to `./data/`:

```
curl -o ./data/switzerland-latest-free.shp.zip https://download.geofabrik.de/europe/switzerland-latest-free.shp.zip
```

The recommended way to process this input file is to open and run [`./notebooks/generate.ipynb`](./notebooks/generate.ipynb) using Jupyter, which provides an interactive session:

```
jupyter notebook
```

Alternatively, you can use [papermill](https://papermill.readthedocs.io/) to run it from the terminal:

```
papermill --cwd ./notebooks/ ./notebooks/generate.ipynb ./notebooks/generate.out.ipynb
```

...
