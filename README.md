# Assets

Repostiory for image assets.

## Converting Images

```
# Convert to maxWidth 2000px
sips --resampleWidth 2000 *.jpg # will overwrite original!
# or rename
mkdir -p resized && sips --resampleWidth 2000 *.[jJ][pP][gG] --out resized/

# Convert from JPG to HEIC
for f in *.[jJ][pP][gG]; do
    sips -s format heic "$f" --out "${f%.*}.heic"
done

```
