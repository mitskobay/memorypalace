# How to Combine Multiple Photos Into a Single Image Using Photoshop

## Open all images together ([1])
- Go to `File > Scripts > Load Files into Stack`
- In the `Load Layers` dialog box, set `Use:` to `Files`
- Use `Browse...` to open each image
- Back in the `Load Layers` dialog box click `OK`
- Photoshop will load each image as a layer in a single document
- Alternatively, to add a photo to an existing document, use `File > Place Embedded...` ([5])

## Expand document bounds ([1])
- The images will be stacked on top of each other
- We will reposition the images and expand the canvas space
- Select the `Move` Tool
- In the `View` menu, make sure `Snap` is enabled, and under `Snap To`, make sure that `Document Bounds` is enabled
- Select a layer to move, then drag the image to the side until it snaps against another image (holding shift while dragging will limit the direction)
- To expand the canvas, go to `Image` and choose `Reveal All`
- Repeat with each image until none are overlapping


## Create guides on a standard reference ([2], [3])
- For example, to make faces the same size, create horizontal guides at the top and bottom of the face and at eye level
- Choose `View > Rulers`
- For a horizontal guide, drag from the horizontal ruler
- Choose a layer to transform, then hit `Command-T`
- Use `shift` key on corner to preserve aspect ratio

## Mask individual layers ([4])
- Select a layer
- Select `Rectangular Marquee Tool`
- Drag a selection outline around the part of the image you want to keep
- Select `Mask`

## Create border between photos ([6])
- Position the photos with space between them
- In Layers panel, at the bottom, click the `Create a New Fill or Adjustment Layer` (diagonal two-toned circle)
- Choose `Solid Color`
- In the dialog box, set the border color, then click `OK`
- In Layers panel, drag the new color fill layer below the image layers

[1]: https://www.photoshopessentials.com/photo-effects/place-two-images-side-by-side/

[2]: https://helpx.adobe.com/photoshop/using/grid-guides.html

[3]: https://clearps.com/photoshop-discussions/threads/19420-resize-two-face-images-to-same-size-in-ps/

[4]: https://www.photoshopessentials.com/basics/how-to-crop-a-single-layer-in-photoshop/

[5]: https://helpx.adobe.com/photoshop/how-to/ps-layers-basics.html?playlistPath=/services/playlist.helpx/set-header:ccx-designer/learn-path:get-started/products:SG_PHOTOSHOP_1_1/playlist:ccl-get-started-1/en_us.json

[6]: https://helpx.adobe.com/ph_fil/photoshop/how-to/add-border-frame-around-photo.html#