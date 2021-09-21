# MESMER Training

This WIPP Plugin trains PanopticNet using MESMER Pipeline.

Contact [Vishakha Goyal](mailto:vishakha.goyal@nih.gov) for more information.

For more information on WIPP, visit the [official WIPP page](https://isg.nist.gov/deepzoomweb/software/wipp).

## Building

To build the Docker image for the conversion plugin, run
`./build-docker.sh`.

## Install WIPP Plugin

If WIPP is running, navigate to the plugins page and add a new plugin. Paste the contents of `plugin.json` into the pop-up window and submit.

## Options

This plugin takes ten input arguments and one output argument:

| Name          | Description             | I/O    | Type   |
|---------------|-------------------------|--------|--------|
| `--tilesize` | Tile size to be processed by the model. Default is 256. | Input | number |
| `--batchSize` | Batch size for training. Default is 1. | Input | number |
| `--iterations` | Number of training iterations. Default is 10. | Input | number |
| `--testingImages` | Input testing image collection to be processed by this plugin | Input | collection |
| `--trainingImages` | Input training image collection to be processed by this plugin | Input | collection |
| `--testingLabels` | Input testing mask collection to be processed by this plugin | Input | collection |
| `--trainingLabels` | Input training mask collection to be processed by this plugin | Input | collection |
| `--outDir` | Output collection | Output | genericData |
