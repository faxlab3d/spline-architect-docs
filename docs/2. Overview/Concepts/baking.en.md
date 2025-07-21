# Baking

Baking is one of the core features of the Spline Architect plugin. Before packaging the game, all `SplineArchitectWall` actors must be baked. This means all procedurally generated details become StaticMesh or InstancedStaticMesh components, the dynamically generated meshes are saved as StaticMesh assets, and the `SplineArchitectWall` no longer executes any logic when the Level loads (no Construction Script runs).

![img](assets/baking.gif)

![img](assets/baking-buttons.jpg){ align=right }

In the `SplineArchitectWall` "Details" panel, there are buttons responsible for baking. You can also choose how the components will be baked: either as `Instanced` or `Components`.

- The `Instanced` bake method creates `InstancedStaticMeshComponent`s, which are more performant to render but harder to edit position, rotation, or other parameters after baking.
- The `Components` bake method creates individual `StaticMeshComponent`s, which are easier to edit but require more draw calls.

---

Once a `SplineArchitectWall` is baked, its WallPreset can no longer be edited. If the preset appears grayed out, it means the actor is baked. The bake status can also be seen by checking the "Baked" boolean.

![img](assets/baked-bool.jpg)

---

![img](assets/baking-menu.jpg){ align=right }

You don’t need to bake each `SplineArchitectWall` individually. The Utility Widget has buttons in the "Bake" section that allow you to bake or unbake all, selected, or connected `SplineArchitectWall` actors.

More details about these buttons can be found [here](../../Components/5.Widgets/#bake).

---

# Automatic Baking

In the Spline Architect Project Settings, you can enable automatic baking of walls when the Level is saved. More information can be found in the [Project Settings](../../Components/6.Project-Settings/#on-level-save-action) section.
