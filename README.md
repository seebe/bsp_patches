# RZ BSP Patches

This is used to clone repositories and create branches at the same level as the BSP relesaes from Renesas.

Some additional patches are provided in the package on renesas.com that are not in github.
So they are included in this repo.

Here is an example.

<pre>
# Clone the build scripts
git clone https://github.com/renesas-rz/rzg2_bsp_scripts
cd rzg2_bsp_scripts/build_scripts

# Clone this repo
git clone https://github.com/seebe/bsp_patches

# Choose a BSP release and set PATCH_DIR to that sub-directory
PATCH_DIR=$(pwd)/bsp_patches/rzg2_vlp_v1.0.10

# Copy/paste the commands in info.txt in the directory (they are listed below)

source $PATCH_DIR/info.txt
eval $FLASH_WRITER_CMD
eval $TFA_CMD
eval $UBOOT_CMD
eval $KERNEL_CMD


# Now you can build usign the build scripts
./build.sh s
./build.sh f
./build.sh u
./build.sh t
./build.sh k

</pre>
