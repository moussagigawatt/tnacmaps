tnacmaps
========
ogr2ogr -f 'ESRI Shapefile' shp/delegations.shp geojson/delegations.geojson -lco ENCODING=UTF-8

ogrinfo -al -geom=SUMMARY shp/delegations.shp

topojson --id-property adm_id -p -o topojson/delegations.json geojson/delegations.geojson

topojson -p -o topojson/tunisia.json geojson/governorates.geojson geojson/circonscriptions.geojson geojson/delegations.geojson


inspirations:
- swiss cantons and municipalities: http://bl.ocks.org/d/4327678/
- us counties: http://bl.ocks.org/4122298

modifications
=============
- Renamed Bouhaira to Le Kram in  Tunis governorate
- On Manouba Governorate merge Manouba delegation with Douar Hicher delegation (false positions)
  Then moved Mnouba delegation back to Manouba governorate(instead of Tunis governorate)
- Add Jarzouna delegation to Bizerte governorate. (by hand replicating images found in the web like: http://www.mdci.gov.tn/tn/Gov/Bizerte.html and http://www.zonu.com/imapa/africa/Carte_Gouvernorat_Bizerte_Tunisie.jpg)
- Add Zaouia Ksiba Thraya delegation to Sousse governorate. (needs to check that split is OK, can't find a reliable up to date map containing the delegation)
- Add Thyna delegation to Sfax governorate (as described in http://www.gouvernorat-sfax.gov.tn/thyna.htm)
- Update metadata and ids to Kairouan Sud delegation in the Kairouan governorate.
- Update metadata and ids to Majel BelAbes delegation in Kasserine governorate.
- Update metadata and ids to Medenine Sud delegation in Medenine governorate.
- Update metadata and ids to Tataouine Sud delegation in Tataouine governorate.
- Split Douz in 2 delegations: Douz Nord et Douz Sud in Kebili governorate (as in page 116 of http://www.ins.nat.tn/publication/rgph2004_volume35.pdf)

TODO
====
- check Zaouia Ksiba Thraya delegation. (Sousse governorate)
- find out tou which delegation the 2 islands in front of Monastir governorate are attached.



