# ImageMagick
- resize
mogrify -resize 1024x1024! -quality 100 *.png
- remove border (1 pixel width. each side and 2 pixels height each side)
mogrify -shave 1x2 *.png

# Blender 
- Closing the turboVNC window after starting a render doesnot kill th ejob
- Closing the tunnel after starting a render also doesnot kill the job
- Logging out of cheyenne also doesnot kill the job

- Squeezing performance out of blender on supers
1. Enable GPU rendering in user preferences and in the render panel
2. Adjust the tile size. The default tile size might not be the fastest option.
3. Resources:
  - Speeding up cycles: https://www.youtube.com/watch?v=8gSyEpt4-60
  - Composition: BG
  - Color: BG
  - Lighting: BG
  - Photorealism: BG
  - Depth Of Field: ?

- To run a render from command line: 
1. Set up the project through an interactive session
2. Set an alias (have to do it only once); Ex: alias blender="<BLENDER_INSTALL_FOLDER>/blender"
3. Run from the folder containing the blend file; Ex: blender -b <.blend_file> -a -x 1 -o //render

# Shell
Rename files to seq. numbers
a=1
for i in *.png; do
  new=$(printf "%04d.jpg" "$a") #04 pad to length of 4
  mv -i -- "$i" "$new"
  let a=a+1
done


