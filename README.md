# blender-vmt
Tools for importing Source Engine material (.vmt) files into Blender

## Features

### VTF Importer
`File -> Import -> Source Engine Image (.vtf)`

Allows importing a single .vtf file into Blender.
The file will be opened with the included VTFLib and packed into the .blend file as a png.

### VMT Importer
`File -> Import -> Source Engine Material (.vmt)`

Allows importing a single material from a .vmt file into Blender.

You need to have the extracted texture files in the original directory structure (`<game>/materials/[subfolder]/<textures>`).
These can be extracted from Source game files using [GCFScape](http://nemesis.thewavelength.net/index.php?p=25).
If your VMT files are in the same directory as your textures, then you don't need to specify the texture path seperately.
If you specify the texture path, the addon will look there for the texture files, instead of the folder the .vmt file is in.

If you have already converted your texture files, you can specify the texture file format.
By default it is the original .vtf format, and the textures will be imported by the addon.

You can also override the material name to whatever you want, otherwise it will use the file name.

By default, existing materials will not be overridden but this can be toggled.

## Installation
1. Clone the repository.
2. Run `install.sh`. (You can use Git Bash under Windows.)
3. Run `python pack_addon.py`
4. Install the addon .zip file in Blender
