# circalizer
(WIP) Flexible stacked visualization of circadian data from multiple sources and devices. Out-of-core and big data ready.

## Description
The first step to understand any kind of data is to observe it. Hence this tool, which aims to accept any kind of input data as long as it can be loaded through Dask's DataFrames. All the data will be plotted through datashader and stacked on the same timeline, synchronized by the timestamp, as to allow full exploration without any loss of information. A small timeline is shown to ease selection of data segments, along with zooming tools to any resolution.

This tool is not meant to analyze the data, although it may include rudimentary tools in the future. Consider it as a no-hassle tool to visualize your periodic data of any shape and size. Since it's leveraging Dask's DataFrames, which are converted on-the-fly to HDF5 databases to allow for faster out-of-core random access (speeds up visualizations), and Datashader with Bokeh for visualizations of big data without summarization, this allows out-of-core computing (ie, data of any size can be read as long as there is enough storage space, RAM is irrelevant, although more RAM speeds up visualization refresh).

The tool is available as an Jupyter Notebook and can also be deployed on a Heroku or similar server thanks to HoloViz's Panel. Although it can work online thanks to Panel's file upload capabilities, this tool is mostly useful to plot big data from multiple sources (hundreds of GBs to dozens of TB), in which case it's better to launch the server or load the notebook locally as transferring file of such size is practically impossible over current internet connections.

## Current state

The previous section describes what aims to be the final product. For now, preliminary work on visualization was finished, so that this serves as a proof-of-concept that the aim is reachable. The visualizations must now be polished, stacked together, generalized to be data-agnostic and finally made into a dashboard using Panel to be used online with file upload capability (through Panel again).

See also https://github.com/jtpio/jupyterlite to run in browser until a HoloViz Panel is implemented.
