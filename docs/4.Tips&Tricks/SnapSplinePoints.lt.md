# Spline Points pritaikymas prie Landscape

Keletas naudotojų klausė apie `SplineArchitectWall` prisnap'inimą prie landscape. Unreal Engine 5 jau turi tam reikalingus įrankius. Žemiau pateikti du rekomenduojami darbo metodai.

---

## 1. Draw Spline įrankis (Modeling Tools)

UE5 **Draw Spline** įrankis leidžia tiesiogiai sukurti spline esamame `SplineArchitectWall` ir pritaikyti jį prie landscape.

**Žingsniai:**

1. Viewport’e pasirinkite savo `SplineArchitectWall` aktorių.
2. Eikite į **Modeling Tools** → **Draw Spline**.
3. Įrankio nustatymuose nustatykite **Output Mode** → **Existing Actor**.
4. Spline points bus pridėti tiesiai and landscape, pasirinkto `SplineArchitectWall` viduje.

![type:video](assets/draw-spline.mp4){ .off-glb }

---

## 2. Snap'inti pasirinkuts Spline Points

Jeigu jau turite spline, bet norite greitai pritaikyti visus taškus prie reljefo (ar kitos geometrijos), naudokite šį metodą:

**Žingsniai:**

1. **Outliner** lange pasirinkite `SplineArchitectWall` aktorių. Pakelkite jį šiek tiek virš landscape.
2. **Details Panel** lange, prie **Spline Component**, paspauskite **Select All Spline Points**.
3. **Viewport’e** dešiniu pelės mygtuku spustelėkite ant spline ir pasirinkite **Snap To Floor**.  

Taip visi taškai bus pritaikyti iškart, užuot spaudus `END` klavišą kiekvienam atskirai.

![type:video](assets/snap-to-floor.mp4){ .off-glb }
