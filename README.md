# swiss-tile

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

...
