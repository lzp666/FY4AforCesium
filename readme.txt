 
China Meteorological Satellite FY4A NatureColor ,layer 0-7

FY4A0-6.7z
FY4A7.7z
terrain.7z : Stereoscopic cloud map layer 

layer 0	156543.0339 km
layer 1	78271.51696 km
layer 2	39135.75848 km
layer 3	19567.87924 km
layer 4	9783.939621 km
layer 5	4891.96981  km
layer 6	2445.984905 km
layer 7	1222.992453 km


var FY4Amap = Cesium.createTileMapServiceImageryProvider({ 
	url: 'SampleData/imagery/FY4A',
	fileExtension: 'png'
        });

var viewer = new Cesium.Viewer('cesiumContainer', {
	shouldAnimate : true,
	animation: true,     
	timeline: true,    
	fullscreenButton: true, 
	infoBox: false,
	baseLayerPicker : false,
	navigationHelpButton: false, 
	baseLayerPicker: false, 
	geocoder: false,
	homeButton: true,
	sceneModePicker: true,
	imageryProvider: FY4Amap
	});
var terrainProvider = new Cesium.CesiumTerrainProvider({ 
	url: "terrain" ,
	requestVertexNormals : true
	}); 		
	viewer.terrainExaggeration=20.0,
	viewer.terrainProvider=terrainProvider;
