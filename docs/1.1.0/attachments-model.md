# Attachments models (.obj)

## Scopes/Sights attachments

You can place your attachment directly in your gun, so you wouldn't have to change the attachment position in the `.render.json` of your gun.
![!](https://modularmods.net/docs/images/attachment-2.png)


!!! info "How the zoom render works ?"
    The render of the zoomed world will be rendered on the plane object named `scopeModel`, it can be a circle or a square.

    ![!](https://modularmods.net/docs/images/attachment-4.png)

    Name your plane object `scopeModel` and place it where you want to render the zoomed world.
    ![!](https://modularmods.net/docs/images/attachment-5.png)

    UV Map of the `scopeModel`: Place the UV map in the center of the box, and size it in function of your wanted zoom.
    ![!](https://modularmods.net/docs/images/attachment-6.png)

    Now it's done:
    ![!](https://modularmods.net/docs/images/attachment-3.png)

!!! info "What is the overlay model ?"
    The overlay model allow to render a black texture in front of the scope model. You can copy the scopeModel, and place it just in front. No textures are required.
    ![!](https://modularmods.net/docs/images/attachment-7.png)

## Barrels attachments and others

Nothing really difficult here, place your `attachmentModel` in the correct position on Blender.

![!](https://modularmods.net/docs/images/attachment-9.png)

![!](https://modularmods.net/docs/images/attachment-8.png)

Export it in .obj using this parameters and that's it.
![!](https://modularmods.net/docs/images/texture4.png)