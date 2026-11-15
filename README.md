# FacePipe

**A free, local tool for preparing face photographs for research.** FacePipe finds the face in each photo, removes the background, straightens and crops by margins you choose, adjusts brightness, contrast and colour in linear light (the same for every image, or matched to a target), and measures every image. Everything runs on your own computer: your photos are never uploaded.

Developed by **Dr. Gabriel (Naiqi) Xiao**, Principal Investigator of the **McMaster Baby Lab**, McMaster University, Canada.

## Download

**[Latest release →](../../releases/latest)**

| Your computer | File |
|---|---|
| Mac with Apple silicon (M1 or newer), macOS 11 or later | `FacePipe-macos-arm64.dmg` |
| Windows 10 or 11, 64-bit | `FacePipe-windows-x64.zip` |
| Linux, 64-bit | `FacePipe-linux-x64.tar.gz` |

The download is about 200 MB and needs about 550 MB of disk space once unpacked. `SHA256SUMS.txt` in each release lists a checksum for every file, if you want to check your download.

### Opening it the first time

The app is not signed with a paid developer certificate, so your computer will ask for confirmation once.

- **Mac:** open the `.dmg`, drag **FacePipe** to Applications. The first time, **right-click FacePipe, choose Open, then Open** again. (If macOS says the app is damaged, run `xattr -dr com.apple.quarantine /Applications/FacePipe.app` in Terminal.)
- **Windows:** unzip the folder and run `FacePipe.exe`. If SmartScreen appears, choose **More info, then Run anyway**.
- **Linux:** `tar -xzf FacePipe-linux-x64.tar.gz` and run `FacePipe/FacePipe`.

FacePipe opens in your web browser (the page is served by the app on your own computer, not from the internet). To stop it, use **Quit FacePipe** at the top right of the page, or ⌘Q on a Mac. Closing the browser tab alone does not stop it.

## How to use it

1. **Choose your photos.** Drop a folder of images (JPG, PNG, TIFF, or camera RAW files) or open a folder on your computer. One face per photo works best.
2. **Faces.** Press *Extract faces*. FacePipe finds every face; check them on the preview and set the background.
3. **Image editing** (optional). Change brightness, contrast and colour inside the face, the same for every photo or matched to one target (mean luminance and RMS contrast).
4. **Crop and align.** Choose the space around the face as fractions of the face height, drag the crop edges, and straighten tilted heads.
5. **Export.** Pick a folder and press *Process all images*. You get the pictures, a `results.csv` with one row per image (including the luminance and contrast actually achieved), and a `manifest.json` for your methods section. Save the recipe to repeat the same processing on a new batch.

A blue **?** next to every setting explains it in plain language. Your original photos are never changed.

## What it is built for

FacePipe follows common practice in vision science for preparing face stimuli: faces are placed with one similarity transform (rotation, uniform scale and shift, so shapes are never stretched); luminance and contrast are defined in linear light with Rec. 709 weights and reported before and after, so you can state the values you achieved; and the methods text for your paper can be generated from the recipe.

## Cite

> Xiao, N. G. (2026). *FacePipe* [Computer software]. McMaster Baby Lab, McMaster University, Canada.

Please also state the version number shown in the app (**About**).

## Questions and problems

Please open an [issue](../../issues) and include the FacePipe version, your operating system, and what you did. Do not attach photos of people unless you have permission to share them.

## Licence

See the [LICENSE](LICENSE) file.

---

*This repository holds the downloads and this page. The source code is maintained privately by the McMaster Baby Lab.*
