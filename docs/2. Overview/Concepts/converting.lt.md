# Konvertavimas

![img](assets/convert-buttons.jpg){ align=right }

Konvertavimas yra procesas, kurio metu Spline Architect aktoriai yra paverčiami į įprastus Unreal Engine aktorius. 

Tai leidžia naudoti Spline Architect sukurtus aktorius kituose projektuose, kurie neturi Spline Architect plugin'o. Pavyzdžiui pasidalinti sukurtu projektu su kitais žmonėmis, kurie neturi Spline Architect plugin'o, arba kelti sukurtus asset'us į FAB Marketplace ar panašiai.

## Kaip konvertuoti Spline Architect aktorius?

Konvertavimas yra labai paprastas. Tereikia pažymėti Spline Architect aktorius, kuriuos norite konvertuoti, ir naudotis "Convert" funkcijomis Utility Widget'e.

Konvertuoti aktoriai bus patalpinami į "Converted" folderį Outliner'yje. Orgianlūs aktoriai, jeigu nebuvo ištrinti bus patalpint "Original" folderyje

| **Mygtukas**     | **Paaiškinimas** |
|-----------------------------|------------------|
| `Actor per parent`          | Sukurs atskirą aktorių kiekvienam tėviniam `SplineArchitectWall`, su visais jo ir jo priattach'intų child'ų komponentais|
| `Actor per wall`            | Sukurs atskirą aktorių kiekvienam `SplineArchitectWall`, su visais jo komponentais – išlaiko tėvo/vaiko struktūrą. |
| `Actor per mesh`            | Sukurs atskirus `StaticMeshActor` kiekvienam naudojamam mesh’ui – patogu vėlesniam rankiniam koregavimui. |
| `Instanced`                 | Sukurs tik `HierarchicalInstancedStaticMesh` komponentus – geresnis našumas, sunkiau redaguoti. |
| `Components`                | Sukurs `StaticMeshComponent` – lengviau redaguoti, bet reikalauja daugiau draw call’ų. |
| **Convert Selected**        | Konvertuoja tik pažymėtus `SplineArchitectWall` (ir visus attach'intus aktorius) |
| **Convert All**             | Konvertuoja visus `SplineArchitectWall` aktorius Level'yje |
| `Delete original?`          | Ištrina originalius `SplineArchitectWall` aktorius palikdamas tik konvertuotus. |