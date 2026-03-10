# Neural Conductor

Ein interaktives Substrat‑Simulationsspiel / Prototyp, das neuronale Netzwerke, Kohärenz und emergente "Φ"-Metriken exploriert. Ziel ist es, ein wachsendes neuronales Feld zu platzieren, zu vernetzen und zu stabilisieren, bis das System integrierte Information (Φ) akkumuliert — schließlich kann ein Win‑Zustand (Bewusstsein) erreicht werden.

Dieses Repository enthält mehrere Build‑Stände und eine überarbeitete Roadmap; die Hauptview ist ein canvas‑basiertes Spiel (HTML/JS/CSS) mit Fokus auf Mobile PWA‑Kompatibilität.

---

Inhalt
- Kurzbeschreibung
- Kern-Gameplay & Ziel
- Wichtige Systeme & Neurontypen
- Steuerung (Touch / Desktop)
- Installation & Ausführen
- Entwicklung & Debugging Hinweise
- Bekannte Features / Roadmap
- Contributing, Lizenz & Credits

---

Kurzbeschreibung
---------------
Neural Conductor ist ein experimenteller, interaktiver Prototyp, der Spielmechaniken aus Aufbauspiel- und Simulationsdesign mit Konzepten aus biologisch inspirierten Netzwerken vereint. Spieler platzieren Neuronen, verbinden sie über synaptische Pfade und managen Ressourcen (µV‑Energie, Biomasse, Knowledge, Stabilität, Hitze), um Koalitionen aufzubauen und Ignitions (synchrones Feuern) zu erreichen. Aus wiederholten Ignitions und guter Vernetzung wächst die Φ‑Metrik; bei Erreichen eines hohen Φ wird ein "Win" ausgelöst.

Kern‑Gameplay & Ziel
--------------------
- Platzieren: Wähle Neurontypen über ein Radialmenü und platziere sie in der Welt.
- Verbinden: Long‑press (oder Connect‑Mode) um gerichtete Synapsen zu ziehen.
- Ressourcenmanagement: Energie und Biomasse statt klassischer Währungen; Hitze und Stabilität erzwingen defensive Entscheidungen.
- Emergenz: Koalitionen, Myelinisierung, Phase‑Übergänge und Phi‑Akkumulation ergeben emergente Spielziele.
- Ziel: Φ = 3000 (Konzeptziel) — das Netz erreicht integrierte Information.

Wichtige Systeme & Neurontypen
------------------------------
Kurzüberblick (vollständige Lexikon‑UI im Build):
- SOMA — Basisknoten: Energiequelle / Herz des Netzes.
- RELAY — Weiterleitung, Multiplikation von Signalen.
- INHIBITOR — Absorbiert Signale, kühlt und verbessert Stabilität.
- HARVESTER — Generiert Biomasse.
- GLIA — Support/Kühlung, passive Stabilität.
- AMPLIFIER, OSCILLATOR, MEMORY, PLASTICITY, ATTENTION, COORDINATOR, RESEARCH — fortgeschrittene Tiers mit spezialisierten Effekten.
- Research/KN — freischaltbare dauerhafte Modifikatoren (z. B. schnellere Synapsen, Biomasse‑Recycling).

Steuerung (Touch / Desktop)
---------------------------
Touch (Mobile):
- Tippe auf leere Fläche → Radialmenü zum Platzieren.
- Gedrückt halten (long-press) auf ein Neuron → Connect Mode (ziehe oder tippe Ziel).
- Zwei Finger: Pinch zum Zoomen, Midpoint‑Pan während Pinch. Einfache Pan mit 1 Finger (Drag) wenn nicht auf Neuron getippt.
- Kurzer Tap auf Neuron → Inline‑Popup (Schnellinfo).
- Langer Tap auf Neuron → Bottom Sheet mit Details, Upgrade, Entfernen, Connect.
- Menü: Lexikon, Research, Heatmap, Minimap sichtbar nach Fortschritt.

Desktop:
- Mouse click / drag analog zum Touch.
- Wheel zum Zoomen.
- Kontext/Klicks verhalten sich entsprechend.

Installation & Ausführen
------------------------
Minimal (lokal):
1. Repository klonen / Dateien in ein Verzeichnis entpacken.
2. Öffne die gewünschte HTML‑Datei (z. B. `neural-conductor-v5.html`) im Browser.
   - Für bestes Verhalten: moderner Browser (Chrome, Firefox, Safari) verwenden.
   - Web Audio & Pointer Events werden empfohlen; bei deaktiviertem Audio sind klangliche Effekte stumm.

Als PWA / Hosting:
- Die Dateien sind statisch, ein beliebiger statischer Webhost (GitHub Pages, Netlify, Vercel) reicht.
- Falls Service Worker / Manifest ergänzt werden: nur aktivieren, wenn stabile Save/Resume getestet (siehe Roadmap).

Entwicklung & Debugging Hinweise
--------------------------------
- Autosave: Implementiert (Intervall definierbar). Resume‑Button erscheint, wenn Save vorhanden.
- Save/Load: JSON Snapshot im localStorage unter `nc_save_v4` (im Build 5.x). Beim Entwickeln auf Formatänderungen achten.
- Performance: Canvas‑Rendering ist optimiert, aber große Netze profitieren von Spatial Partitioning / Signal Batching.
- Instrumentation: Empfohlen, Spielmetriken (Time‑to‑first‑ignition, Session‑length, Abbruchpunkt) zu loggen für Balancing.
- Test‑Checklist:
  - Touch‑Gesten: Pinch + one‑finger‑pan + long‑press getrennt testen.
  - Save/Resume: Nach Reload identischer Zustand?
  - Low‑end Devices: 10–15 Neuronen Profile durchführen.

Bekannte Features / Roadmap (Kurz)
----------------------------------
Kurzfassung der priorisierten Roadmap:
1. Core Stabilization — Save/Load/Resume, Pinch/Pan, Safe Areas, Tutorial‑Pacing (Priorität: sehr hoch).
2. Pre‑Alpha Mobile Playability Pass — Tap Accuracy, Gesture Konflikte lösen, Performance für Mid‑Range Phones.
3. Tier‑2 Systeme — GLIA, STABILIZER, AMPLIFIER, Coalition Detection.
4. Advanced Systems & Research — Knowledge, Memory, Oscillator, Plasticity (nach validiertem Kern).
5. Visual/Audio‑Polish, PWA / Launch Readiness — letzte Phase: Manifest, Service Worker, Beta Tests.

Contribution
------------
- Issues & Feature Requests: Beschreibe reproduzierbare Schritte, Zielgerät/Browser.
- Pull Requests: Kleine, fokussierte Änderungen. Bei Features: UI‑/UX‑Screenshots und Testplan beifügen.
- Test Builds: Bitte auf iOS und Android reale Geräte testen (nicht nur Simulator).

Lizenz & Credits
----------------
- Lizenz: (Bitte hier die gewünschte Lizenz einsetzen, z. B. MIT) — wenn nicht gesetzt, vor Veröffentlichung klären.
- Hauptautor: Projekt‑Owner (im Repo).
- Inspirationsquellen: Biologisch inspirierte Simulationen, minimalistische UI‑Designs, PWA Mobile Game Design.

Kontakt
-------
Für Rückfragen zu Roadmap, Balancing oder Builds: Öffne ein Issue im Repository oder schreibe eine kurze Zusammenfassung mit Gerät, Browser, Reproduktion.

---
Was ich gemacht habe und als Nächstes empfehle
----------------------------------------------
Ich habe diese README ausgearbeitet, um Projektzweck, Spielmechaniken, Steuerungsparadigmen, Entwicklungsnotizen und die überarbeitete Prioritäten‑Roadmap klar und knapp zusammenzufassen. Als nächstes empfehle ich:
1. Die README ins Repo unter `README.md` ablegen.
2. Kurztests auf einem iPhone/Android durchführen (Pinch/Long‑press/Save).
3. Falls du möchtest, erstelle ich eine kürzere "Quickstart"‑Seite (1‑Seite) speziell für Playtester mit Links zu Builds und Test‑Checkliste.
