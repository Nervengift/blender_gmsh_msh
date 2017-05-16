# What is this?

This is an addon script for [Blender](https://blender.org) to allow importing [gmsh](http://gmsh.info)'s [native file format](http://gmsh.info/doc/texinfo/gmsh.html#MSH-ASCII-file-format) (".msh").

2D regions (`$PhysicalNames`) will get mapped to Blender materials, i.e. there are materials for all regions and all faces in such a region will use the corresponding material.

# How do I use this?

Just go to *File* -> *User Preferences* -> *Addons*, click *Install from file...* and find the `import_msh.py`. You should then find the *gmsh MSH import* in the *File* -> *Import* menu (else check if the addon is enabled)

# Limitations

* this only supports simple primitives (lines, triangles and quads), since I didn't need support for things like "125-node fourth order hexahedron" (yes, that's a thing in .msh)
* (tetrahedron support is included but commented out, you may try it at your own risk)
* no support for periodic elements (`$Periodic`) and additional element data (`$ElementData`, `$ElementNodeData`)
* no export
