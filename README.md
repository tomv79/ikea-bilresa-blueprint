# IKEA BILRESA – All-in-One Blueprint (Buttons + Scrollwheel)

Dieser Blueprint ermöglicht die vollständige Nutzung des **IKEA BILRESA Scroll Wheel Tasters**
in **Home Assistant** über **Matter / event.* Entities**.

Er kombiniert **alle Funktionen in einem einzigen Blueprint**:
- 3 Buttons (Button 2 & 3 optional)
- Scrollwheel rechts / links **pro Button**
- Mehrfachklicks
- Halten zum Dimmen
- Keine Cover-Funktionen (bewusst weggelassen)

---

## ✨ Funktionen

### Buttons (Taste 1–3)
- **1× Klick** (`multi_press_1`)
- **2× Klick** (`multi_press_2`)
- **3× Klick** (`multi_press_3`)
- **Halten / Loslassen**
  - `long_press` → Dimmen
  - `long_release` → Stop

Button **2 und 3 sind optional**.  
Wenn keine Event-Entity ausgewählt wird, werden sie einfach ignoriert.

---

### Scrollwheel (Drehrad)
Für **jeden Button separat** konfigurierbar:

- Rechtsdrehung → Helligkeit erhöhen oder reduzieren
- Linksdrehung → Helligkeit erhöhen oder reduzieren
- Berücksichtigt `totalNumberOfPressesCounted`
- Eigene Schrittweite pro Richtung
- Eigene Ziellampe pro Button möglich

Button 2 & 3 Scrollwheel-Entities sind ebenfalls **optional**.

---

## 🧩 Voraussetzungen

- **Home Assistant Core ≥ 2024.x**
- IKEA **BILRESA Scroll Wheel Taster**
- Integration, die **`event.*` Entities** erzeugt (z. B. Matter)
- Lampe mit Dimmfunktion (`light` Domain)

⚠️ Dieser Blueprint ist **nicht** für ZHA-/Zigbee-Action-Sensoren gedacht,  
sondern explizit für **event-basierte Matter-Entities**.

---

## 📥 Installation

### Direktimport (empfohlen)
Klicke auf diesen Link:

https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/tomv79/ikea-bilresa-blueprint/main/blueprints/automation/ikea_bilresa_all_in_one.yaml
