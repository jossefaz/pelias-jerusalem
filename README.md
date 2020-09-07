# Israel area

This project is configured to download/prepare/build a complete Pelias installation for Jerusalem City.

The Geocode csv is under copyright for that moment (only a sample of it is contained in this repository under data/csv/adress.csv), then if you would use it, you should ask for a copy of it from the municipality of Jerusalem.

# Setup

Please refer to the instructions at <https://github.com/pelias/docker> in order to install and configure your docker environment.

The minimum configuration required in order to run this project are [installing prerequisites](https://github.com/pelias/docker#prerequisites), [install the pelias command](https://github.com/pelias/docker#installing-the-pelias-command) and [configure the environment](https://github.com/pelias/docker#configure-environment).

Please ensure that's all working fine before continuing.

# Run a Build

To run a complete build, execute the following commands:

```bash
pelias compose pull
pelias elastic start
pelias elastic wait
pelias elastic create
pelias download all
pelias prepare all
pelias import all
pelias compose up
```

# Make an Example Query

You can now make queries against your new Pelias build:

<http://localhost:4000/v1/search?text=Jerusalem>
