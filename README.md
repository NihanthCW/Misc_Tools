# Misc_Tools
Misc

# Image Magick tips
- resize
mogrify -resize 1024x1024! -quality 100 *.png

- remove border (1 pixel width. each side and 2 pixels height each side)
mogrify -shave 1x2 *.png

# Other

Rename files to seq. numbers
a=1
for i in *.png; do
  new=$(printf "%04d.jpg" "$a") #04 pad to length of 4
  mv -i -- "$i" "$new"
  let a=a+1
done


