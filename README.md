
# TrackScar imageJ macros

This repo contains toolsets to help with budscar counting for TrackScar.

# Installation


## Without git

Download the source for this repo. The folder should contain several `.txt` files, including two called `TrackScar segmentation.txt` and `TrackScar.txt`. There are also two files called: `makeCountList` and `mergeDV`. These files need to be installed into Fiji by copying them into its `toolsets` folder.

On a Mac, right click on the `Fiji.app` file in the `Applications` folder. Select `Show Contents`. Navigate to the folder `macros` and then to the folder `toolsets`. Copy the files `TrackScar segmentation.txt` and `TrackScar.txt` to the toolsets folder. Then restart Fiji.

Add the path to the macros folder to your .bash_profile. On my machine, the relevant line to add was:

`export PATH="/Applications/Fiji.app/macros/toolsets:$PATH"`

## With git

To install, delete the 'macros/toolsets' folder in Fiji and replace it with a clone of this repo.

`
cd path/to/macros
git clone https://bitbucket.org/csmaxwell/fiji-toolsets.git toolsets
`
Add the path to the macros folder to your .bash_profile. On my machine, the relevant line to add was:

`export PATH="/Applications/Fiji.app/macros/toolsets:$PATH"`


# Usage

## mergeDV

This is a python script that is designed to process images created by a DeltaVision microscope. It will not work for other file formats. The program expects

`exp052715_1514-D-for-age_02_160_R3D_D3D_PRJ_w-50.tif
exp052715_1514-D-for-age_02_160_R3D_D3D_PRJ_w525.tif
exp052715_1514-D-for-age_02_160_R3D_D3D_PRJ_w594.tif
exp052715_1514-D-for-age_02_160_R3D_D3D_PRJ_w676.tif`

`mergeDV --channels "w525 w676 w594 w-50" examples examples/stacks`



