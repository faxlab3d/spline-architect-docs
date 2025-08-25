# Aligning Spline Points to Landscape

Several users have asked about snapping `SplineArchitectWall` to a landscape. Unreal Engine 5 already provides the necessary tools. Below are two recommended workflows.

---

## 1. Draw Spline Tool (Modeling Tools)

UE5’s **Draw Spline** tool can directly create a spline inside an existing `SplineArchitectWall` and project it onto the landscape.

**Steps:**

1. Select your `SplineArchitectWall` actor in the viewport.
2. Go to **Modeling Tools** → **Draw Spline**.
3. In the tool settings, set **Output Mode** → **Existing Actor**.
4. The spline points will be added directly onto the landscape, inside the selected `SplineArchitectWall`.

![type:video](assets/draw-spline.mp4){ .off-glb }

---

## 2. Snapping selected Spline Points

If you already have a spline but want to quickly snap all spline points to the terrain (or any underlying geometry), use this method:

**Steps:**

1. In the **Outliner**, select your `SplineArchitectWall` actor. Move it slightly above the landscape.
2. In the **Details Panel**, under the **Spline Component**, press **Select All Spline Points**.
3. In the **Viewport**, right-click on the spline and choose **Snap To Floor**.

This snaps all points at once, instead of snapping them one by one with the `END` key.
   
![type:video](assets/snap-to-floor.mp4){ .off-glb }
