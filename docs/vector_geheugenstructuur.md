# VECTORGEHEUGENSTRUCTUUR – hexENErgy

De hexBALanceMATrix is het structurele geheugen van het systeem. Het bestaat uit hexagonaal georganiseerde vectorvelden waarin gedrag, richting, fase en puls exact worden vastgelegd.

## 🔹 STRUCTURELE EIGENSCHAPPEN

- **Hexagonale ordening (6-richtingensymmetrie)**  
  Elk veld heeft precies 6 directe buren → essentieel voor:
  - pulsspreiding
  - fasebalans
  - spiegelidentificatie
  - foutcorrectie zonder redundantie

- **Gespiegeld geheugen (spiegel × .bin)**  
  Elke vectorcel heeft:
  - een originele waarde (`value`)
  - een spiegelwaarde (`value_mirror`)
  - hash_origineel en hash_spiegel
  - fasepositie (`Φ`) en pulshoogte (`P`)

- **Hash-verificatie (SHA256)**  
  Elke veldpositie bevat:
  - cryptografisch hash-ID
  - gedragsgebonden signatuur
  - timestamp van laatste activatie
  - directionele offset (`x, y, z`) voor 3D-herkenning

## 🔹 VOORBEELDSTRUCTUUR (JSON-stijl)

```json
{
  "id": "hex_012",
  "x": 5,
  "y": 3,
  "z": 0.0,
  "value": 0.886,
  "value_mirror": 0.114,
  "phase": 0.33,
  "pulse": 0.77,
  "hash_original": "7a32...e4a1",
  "hash_mirror": "3c4f...7b2e",
  "visible": false
}

---8cefe4fe505d972c1cee7503c0d3cf7e12944121713f7d3a3a24fa0b2397e3a9
