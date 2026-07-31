Export.table.toDrive({
  collection: watershedsFC,
  description: 'Sutlej_Nested_Watersheds_3PourPoints',
  folder: 'PhD_Sutlej_DigitalTwin',
  fileFormat: 'SHP'
});
 
Export.table.toDrive({
  collection: zonesFC,
  description: 'Sutlej_Incremental_Zones_3PourPoints',
  folder: 'PhD_Sutlej_DigitalTwin',
  fileFormat: 'SHP'
});
 
Export.image.toDrive({
  image: demMasked,
  description: 'Sutlej_FullBasin_DEM_GLO30_30m',
  folder: 'PhD_Sutlej_DigitalTwin',
  fileNamePrefix: 'Sutlej_FullBasin_DEM_GLO30',
  region: wsBhakra.geometry(),
  scale: 30,
  crs: 'EPSG:32643',
  maxPixels: 1e10,
  fileFormat: 'GeoTIFF'
});
