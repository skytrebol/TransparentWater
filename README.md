# TransparentWater

This is a lightweight Water module for three.js.


example:

    water = new TransparentWater(
	waterGeometry, {
	    textureWidth: 512,
	    textureHeight: 512,
	    waterNormals: new THREE.TextureLoader().load(
		'../js-module/textures/water/waternormals.jpg',
		function ( texture ) {
		    texture.wrapS = texture.wrapT = THREE.RepeatWrapping;
		} ),
	    eye: new THREE.Vector3( 0, -1, 0 ),
            intensity: 1.0,
	    alpha: 0.7,
	    sunDirection: new THREE.Vector3( 10, 400, 10 ),
            side: THREE.DoubleSide,
	    distortionScale: 3.7,
	    sunColor: 0x131818, //green-blue
	    baseColor: 0x232f2f, //blue-gray-cyan
	    waterColor: 0x85888d, //blue-gray-cyan
	    fog: scene.fog !== undefined
	}
    );
    scene.add( water );


    water.update({sunColor:0x131818,baseColor:0x232f2f,waterColor:0x85888d,alpha:0.85});
    water.update({time:(1.0 / 90.0),intensity:(_intensity/2+0.5)});
