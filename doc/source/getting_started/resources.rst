ICESat-2 Open-Source Resources Guide
====================================

This guide contains information regarding available resources for working with ICESat-2 datasets, both specifically (e.g. for ICESat-2 data) and more broadly (e.g. point cloud analysis of LiDAR datasets). It includes resources formally developed by/with support from NASA as well as individual and community efforts stemming from personal interest to ongoing research workflows.

Please feel free to add your project or another resource to this guide by submitting a pull request. We reserve the right to reject suggested resources that fall outside the scope of icepyx.

Resources Used in the Initial Development of icepyx
---------------------------------------------------

First ICESat-2 Cryospheric Hackweek at the University of Washington
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This June 2019 event resulted in the production of a series of `tutorials <https://github.com/ICESAT-2HackWeek/ICESat2_hackweek_tutorials>`_, developed primarily by members of the ICESat-2 Science Team and early data users, aimed at educating the cryospheric community in obtaining and using ICESat-2 datasets. During the actual Hackweek, teams of researchers and data scientists developed a series of interesting `projects <https://github.com/ICESAT-2HackWeek/projects_2019>`_ related to their interests/research. 

The available tutorials, most of which contain one or more Jupyter Notebooks to illustrate concepts, are listed below. Additional information for citing (including licensing) and running (e.g. through a Pangeo Binder) these tutorials can be found at the above link.

1. `Overview of the ICESat-2 mission (slides) <https://github.com/ICESAT-2HackWeek/intro_ICESat2>`_
2. `Introduction to Open Science and Reproducible Research <https://github.com/ICESAT-2HackWeek/intro-jupyter-git>`_
3. `Access and Customize ICESat-2 Data via NSIDC API <https://github.com/ICESAT-2HackWeek/data-access>`_
4. `Intro to HDF5 and Reduction of ICESat-2 Data Files <https://github.com/ICESAT-2HackWeek/intro-hdf5>`_
5. `Clouds and ICESat-2 Data Filtering <https://github.com/ICESAT-2HackWeek/Clouds_and_data_filtering>`_
6. `Gridding and Filtering of ICESat/ICESat-2 Elevation Change Data <https://github.com/ICESAT-2HackWeek/gridding>`_
7. `ICESat-2 for Sea Ice <https://github.com/ICESAT-2HackWeek/sea-ice-tutorials>`_
8. `Geospatial Data Exploration, Analysis, and Visualization <https://github.com/ICESAT-2HackWeek/geospatial-analysis>`_
9. `Correcting ICESat-2 data and related applications <https://github.com/ICESAT-2HackWeek/data-correction>`_
10. `Numerical Modeling <https://gitlab.com/danshapero/icesat-2019-06-20>`_

Though in many cases preliminary, these `project repositories <https://github.com/ICESAT-2HackWeek/projects_2019>`_ can provide useful starting points to develop effective cryospheric workflows where more formal examples and functionality have not yet been developed.

*Sea Ice*

- `Floes are Swell <https://github.com/ICESAT-2HackWeek/Floes-are-Swell>`_

  - Calculate chord length (CLD) and lead width (LWD)

- `Segtrax <https://icesat2hackweek2019.slack.com/messages/CKQ08MBBR>`_

  - Create trajectories of sea ice motion (creates Python trajectory class)

*Glaciers and Ice Sheets*

- `Crackup <https://github.com/ICESAT-2HackWeek/crackup>`_

  - Investigating small-scale features such as crevasses and water depth

- `GlacierSat2 <https://github.com/ICESAT-2HackWeek/glaciersat2>`_

  - Constrain surface types (e.g. wet vs. dry snow) using ICESat-2 data over the Juneau Icefield, working towards looking at seasonal elevation changes

- `WaterNoice <https://github.com/ICESAT-2HackWeek/WaterNoice>`_

  - Detection of hydrologic features (e.g. meltwater ponds, firn aquifer seeps, blue ice megadunes, icebergs, etc.) in ATL06 land ice product

- `SnowBlower/blowing snow <https://github.com/ICESAT-2HackWeek/Snowblower>`_

  - Evaluate the blowing snow flag and look at blowing snow models

- `Cross-trak (xtrak) <https://github.com/ICESAT-2HackWeek/xtrak>`_

  - Interpolation between ICESat-2 tracks
  - Create gridded elevation data from multiple ICESat-2 tracks

- `Ground2Float <https://github.com/ICESAT-2HackWeek/ground2float>`_

  - Identify grounding zones using ICESat-2 data (using the slope-break method)

- `Topohack <https://github.com/ICESAT-2HackWeek/topohack>`_

  - Resolve topography over complex terrain

Other Relevant GitHub Repositories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Here we describe a selection of publicly available Python code posted on GitHub with potential applicability for working with ICESat-2 data within the context of icepyx. This includes repositories that extend its capabilities for working with LiDAR datasets in general.

*Note: Listing here does not suggest endorsement or recommended use of these tools; this list is simply a compilation of publicly available GitHub repositories relevant to icepyx and annotations to reflect how they may relate to icepyx. Please check the licensing information before using any of this code. Additional resources having to do specifically with ICESat-2 are noted in the last section of this document.*

- `PointDatabase <https://github.com/SmithB/PointDatabase>`_

  - by Ben Smith
  - Efficiently create and query a database of points using this set of utilities
  
- `Nsidc-subsetter <https://github.com/tsutterley/nsidc-subsetter>`_

  - by Tyler Sutterly
  - Retrieve IceBridge, ICESat, and ICESat-2 data using the NSIDC subsetter API
  - Command line tool
  - Download data and convert it into a georeferenced format (e.g. geojson, kml, or shapefile)

- `Icesat2-viz <https://github.com/abarciauskas-bgse/icesat2-viz>`_

  - by Aimee Barciauskas-bgse
  - Exploration for visualizing ICESat-2 data products; focused on 3-D visualization using mapbox tools

- `Chasingseaice <https://github.com/akpetty/chasingseaice>`_

  - by Alek Petty, Linette Boisvert, Jeremy Harbeck
  - Correct IceBridge flight path to account for ice drift relative to ICESat-2

- `captoolkit <https://github.com/fspaolo/captoolkit>`_

  - by Fernando Paolo, Johan Nilsson, Alex Gardner
  - NASA's JPL Cryosphere Altimetry Processing Toolkit
  - Set of command line utilities to process, reduce, change format, etc. altimetry data from ICESat-2 and several other altimeters (e.g. ERS, CryoSat-2, IceBridge)
  - Includes utilities to read and extract variables of interest, compute and apply various corrections (e.g. tides, inverse barometer), detrend and correct data, do a variety of geographic computations and manipulations (e.g. raster math, masking, slope/aspect), and tile/grid/reduce data


Other Ways to Access ICESat-2 Data
----------------------------------
- `NSIDC (DAAC) Data Access <https://nsidc.org/data/icesat-2>`_

  - Select “ICESat-2 Data Sets” from the left hand menu. Choose your dataset (ATL##). Then, use the spatial and temporal filters to narrow your list of granules available for download.

- `OpenAltimetry <https://openaltimetry.org/>`_

  - Collaboration between NSIDC, Scripps, and San Diego Supercomputer Center
  - Enables data browsing on a map and selection of tracks and interactive data exploration for the higher level ICESat-2 datasets (i.e. ATL06+)