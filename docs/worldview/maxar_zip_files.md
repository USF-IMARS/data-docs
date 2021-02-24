# An overview of what you get inside a `.zip` file from maxar and how to use it.

```
[root@thing1 jobos]# unzip wv_maxar_zip/WV220150715150031P00.zip -d wv_maxar_unzipped/
[root@thing1 jobos]# tree wv_maxar_unzipped/
wv_maxar_unzipped/
├── 013663600010_01_003
│   ├── 013663600010_01
│   │   ├── 013663600010_01_LAYOUT.JPG
│   │   ├── 013663600010_01_P001_MUL
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.ATT
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001-BROWSE.JPG
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.EPH
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.GEO
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.IMD
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.NTF
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001_README.TXT
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.RPB
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.TIL
│   │   │   ├── 20JAN08150533-M1BS-013663600010_01_P001.XML
│   │   │   └── NEXTVIEW.TXT
│   │   ├── 013663600010_01_P001_PAN
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.ATT
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001-BROWSE.JPG
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.EPH
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.GEO
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.IMD
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.NTF
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001_README.TXT
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.RPB
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.TIL
│   │   │   ├── 20JAN08150533-P1BS-013663600010_01_P001.XML
│   │   │   └── NEXTVIEW.TXT
│   │   ├── 013663600010_01_README.TXT
│   │   ├── 013663600010_01_README.XML
│   │   └── GIS_FILES
│   │       ├── 013663600010_01_ORDER_SHAPE.dbf
│   │       ├── 013663600010_01_ORDER_SHAPE.prj
│   │       ├── 013663600010_01_ORDER_SHAPE.shp
│   │       ├── 013663600010_01_ORDER_SHAPE.shx
│   │       ├── 013663600010_01_PRODUCT_SHAPE.dbf
│   │       ├── 013663600010_01_PRODUCT_SHAPE.prj
│   │       ├── 013663600010_01_PRODUCT_SHAPE.shp
│   │       ├── 013663600010_01_PRODUCT_SHAPE.shx
│   │       ├── 013663600010_01_STRIP_SHAPE.dbf
│   │       ├── 013663600010_01_STRIP_SHAPE.prj
│   │       ├── 013663600010_01_STRIP_SHAPE.shp
│   │       ├── 013663600010_01_STRIP_SHAPE.shx
│   │       ├── 013663600010_01_TILE_SHAPE.dbf
│   │       ├── 013663600010_01_TILE_SHAPE.prj
│   │       ├── 013663600010_01_TILE_SHAPE.shp
│   │       ├── 013663600010_01_TILE_SHAPE.shx
│   │       ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf
│   │       ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.prj
│   │       ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.shp
│   │       ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.shx
│   │       ├── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.dbf
│   │       ├── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.prj
│   │       ├── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.shp
│   │       └── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.shx
│   └── DeliveryMetadata.xml
├── fileRecords
│   └── 013663600010_01_P001.links
└── GIS_FILES
    ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf
    ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.prj
    ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.shp
    ├── 20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.shx
    ├── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.dbf
    ├── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.shp
    └── 20JAN08150533-P1BS-013663600010_01_P001_PIXEL_SHAPE.shx
```

Shape files in the two `GIS_FILES` directories do differ.
```
[root@thing1 jobos]# diff wv_maxar_unzipped/GIS_FILES/20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf wv_maxar_unzipped/013663600010_01_003/013663600010_01/GIS_FILES/20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf
Binary files wv_maxar_unzipped/GIS_FILES/20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf and wv_maxar_unzipped/013663600010_01_003/013663600010_01/GIS_FILES/20JAN08150533-M1BS-013663600010_01_P001_PIXEL_SHAPE.dbf differ
```
TODO: how do they differ? which do we want?