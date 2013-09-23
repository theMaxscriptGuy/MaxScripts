
The very first script written is the one to export objects from 3ds Max to a ThreeJS compatible JSON format.

The script file is:
3ds_ThreeJS_Exporter.mse

How script looks:
Exporter_Script.jpg

Sample JSON Exported:
Character_gob.js
This is a character that I made in 3ds Max (reference from google).

HOW does it LOOK on THREEJS?
char.jpg
This is the mesh how it looks on ThreeJS(a very quick scene setup).

HOW TO USE IT?
Once downloaded, drag and drop it to the 3ds Max Viewport and it shall run.
To export the objects, select those needed to be exported and click on "Export" Button.

For now the only option you get is the change the scale of the object.

What Does It Export?
For now, the script only exports the object vertices, faces, normals and uvs.

Why so LESS?
This is just a quick script to export your objects from 3ds Max without getting into any hassels of export to obj/fbx and converting using a Python Script.
With one click your JSON/s are ready to be loaded on a ThreeJS platform.
Soon we shall be up with a complete scene export for WebGL and ThreeJS Lovers!

Sample 3JS Code:

loader.load( "objects/gob.js", function( geometry ) {
						var mat = new THREE.MeshLambertMaterial();
						var mesh = new THREE.Mesh( geometry, mat );
						geometry.computeVertexNormals();
						mesh.position.set(0, 0, 0);
						var s = 5000;
						mesh.scale.set(s, s, s);
						scene.add(mesh);
				});
				
Thanks,
Videep
