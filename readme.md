# Festival Bridge

## Introduction
There are two types of map layers
- Polygon layers
- Point layers

## Polygon layers
Use a standardised CSV file uploaded into the control panel. Change the Entry Type to "Polygons".

### Required columns:
```name```

```geometry```
```geometry2```

### Optional columns
```description_1```
```description_2```
```description_3```
```description_4```
```description_5```
```description_6```
```description_7```
```description_8```
```description_9```
```description_10```
```description_11```
```description_12```
```description_13```
```description_14```
```description_15```
```description_16```
```description_17```
```description_18```
```description_19```
```description_20```

```cyp_n``` (CYP number)

```cyp_pp``` (CYP % of parent)

```cyp_pn``` (CYP % to national)

```cyp_v``` (Variance of CYP % to national)

```aa_n``` (AA awards in 18/19)

```aa_pp``` (AA % of parent)

```aa_pc``` (AA per capita of parent)

```es_n``` (ES number)

```es_pp``` (ES % of parent)

```am_n``` (AM number)

```am_pp``` (AM % of parent's Artsmarks)

```am_ppes``` (AM % of parent's ES)


Column names are case-sensitive and must be identical to those listed above if the data is to be extracted and displayed. If not correct, the data will either be missing (for optional columns) or prevent the layer from loading in the browser (required columns).

### Colours
When uploading, there is a table where you can add a row for each column. Below that, you enter the name of the column used to identify which colour to use. This column should contain integers corresponding to the row in the table, with row 1 being the top row. For example, if your column has values from 1-10, you should make sure there are 10 colours added to the colour table.

You can still add colours if you don't have a colour column - just add the hex codes to the table and they'll be assigned randomly.

Failing that, there is an option for a default colour fo all the polygons.

## Points layers
Use a KMZ file uploaded into the control panel. The Entry Type should be "Points", which is the default.

You get hold of the KMZ file by visiting a Google MyMap and exporting to KMZ. Check the following option: "Keep data up to date with network link..."

Note that for the exported KMZ file to be displayed, we require the lat/lng to be exported as well. Google will not do this if you have imported a data set into MyMaps without providing your own lat/lng. The points will display on your MyMap because Google will geocode the addresses when you import, but if this happens they won't be exported.

> Working

## Common issues
If your polygon layers doesn't display, it's likely to be:
1. Your column names aren't what we're expecting. Check they are exactly the same as above.
2. Your geometry data has errors in it. If you suspect this, it's a case of uploading again and again with different rows excluded to see where the problem is. If the geometry is in JSON format, check it with an online JSON validator

If your points layer doesn't display, it's likely you did not provide your own lat/lng values. You can check this by exporting as a KML file and examining the contents. If you've provided your own, the coordinates will be in there. If not, they won't.

## Specific examples
### Wards
This is a polygon layer, so requires name and geometry. Not all data is available for the Wards, so expect just descriptions and the three CYP columns only.

> Working

### Districts
Polygon layer. Has limited numerical data.
> Working

### Counties
This is a polygon layer, so requires name and geometry. No numerical data.

> Working

### LSOAs
Polygon layer, with colours and decile_rank to manage them. No numerical data.

> Working

## To add
- Look to add hover labels to polygons