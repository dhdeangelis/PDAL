(readers)=

# Readers

PDAL processes files in a variety of formats, listed below, with each
tied to a reader.

Readers provide {ref}`dimensions` to {ref}`pipeline`. PDAL attempts to
normalize common dimension types, like X, Y, Z, or Intensity, which are often
found in LiDAR point clouds. Not all dimension types need to be fixed, however.
Database drivers typically return unstructured lists of dimensions.  A reader
might provide a simple file type, like {ref}`readers.text`, a complex database
like {ref}`readers.pgpointcloud`, or a network service like {ref}`readers.ept`.

PDAL supports streaming a file from a remote server with {ref}`VSI`.

<!-- ```{toctree}
:glob: true
:hidden: true
:maxdepth: 1

readers.arrow
readers.bpf
readers.buffer
readers.copc
readers.draco
readers.ept
readers.e57
readers.faux
readers.fbi
readers.gdal
readers.hdf
readers.i3s
readers.ilvis2
readers.las
readers.matlab
readers.memoryview
readers.mbio
readers.nitf
readers.numpy
readers.obj
readers.optech
readers.pcd
readers.pgpointcloud
readers.ply
readers.pts
readers.ptx
readers.qfit
readers.rdb
readers.rxp
readers.sbet
readers.smrmsg
readers.slpk
readers.stac
readers.terrasolid
readers.text
readers.tiledb
readers.tindex
``` -->

{ref}`readers.arrow`

: Read GeoArrow/GeoParquet formatted data.

{ref}`readers.bpf`

: Read BPF files encoded as version 1, 2, or 3. BPF is an NGA specification
  for point cloud data.

{ref}`readers.copc`

: COPC, or Cloud Optimized Point Cloud is an LAZ 1.4 file stored as a
  clustered octree.

{ref}`readers.buffer`

: Special stage that allows you to read data from your own PointView rather
  than fetching data from a specific reader.

{ref}`readers.draco`

: Read a buffer in Google Draco format

{ref}`readers.ept`

: Used for reading [Entwine Point Tile](https://entwine.io) format.

{ref}`readers.e57`

: Read point clouds in the E57 format.

{ref}`readers.faux`

: Used for testing pipelines. It does not read from a file or database, but
  generates synthetic data to feed into the pipeline.

{ref}`readers.fbi`

: Read TerraSolid FBI format

{ref}`readers.gdal`

: Read GDAL readable raster data sources as point clouds.

{ref}`readers.hdf`

: Read data from files in the HDF5 format.

{ref}`readers.i3s`

: Read data stored in the Esri I3S format.  The data is read from an
  appropriate server.

{ref}`readers.ilvis2`

: Read from files in the ILVIS2 format.

{ref}`readers.las`

: Read ASPRS LAS versions 1.0 - 1.4. Does not support point formats
  containing waveform data. LASzip support is also enabled through this
  driver if LASzip  or LAZperf are found during compilation.

{ref}`readers.matlab`

: Read point cloud data from MATLAB .mat files where dimensions are stored as
  arrays in a MATLAB struct.

{ref}`readers.mbio`

: Read sonar bathymetry data from formats supported by the MB-System library.

{ref}`readers.memoryview`

: Read data from memory where dimension data is arranged in rows.  For
  use only with the PDAL API.

{ref}`readers.nitf`

: Read point cloud data (LAS or LAZ) wrapped in NITF 2.1 files.

{ref}`readers.numpy`

: Read point cloud data from Numpy `.npy` files.

{ref}`readers.obj`

: Read points and a mesh from Wavefront OBJ files.

{ref}`readers.optech`

: Read Optech Corrected Sensor Data (.csd) files.

{ref}`readers.pcd`

: Read files in the PCD format.

{ref}`readers.pgpointcloud`

: Read point cloud data from a PostgreSQL database with the PostgreSQL
  Pointcloud extension enabled.

{ref}`readers.ply`

: Read points and vertices from either ASCII or binary PLY files.

{ref}`readers.pts`

: Read data from Leica Cyclone PTS files.

{ref}`readers.ptx`

: Read data from Leica Cyclone PTX files.

{ref}`readers.qfit`

: Read data in the QFIT format originated for NASA's Airborne Topographic
  Mapper project.

{ref}`readers.rxp`

: Read data in the RXP format, the in-house streaming format used by RIEGL.
  The reader requires a copy of RiVLib during compilation.

{ref}`readers.rdb`

: Read data in the RDB format, the in-house database format used by RIEGL.
  The reader requires a copy of rdblib during compilation and usage.

{ref}`readers.sbet`

: Read the SBET format.

{ref}`readers.slpk`

: Read data stored in an Esri SLPK file.

{ref}`readers.smrmsg`

: Read from POSPac MMS post-processed accuracy files.

{ref}`readers.stac`

: Read STAC JSON Catalogs and Items with the Pointcloud extension.

{ref}`readers.terrasolid`

: TerraSolid Reader

{ref}`readers.text`

: Read point clouds from ASCII text files.

{ref}`readers.tiledb`

: Read point cloud data from a TileDB instance.

{ref}`readers.tindex`

: The tindex (tile index) reader allows you to automatically merge and query
  data described in tile index files that have been generated using the PDAL
  tindex command.
