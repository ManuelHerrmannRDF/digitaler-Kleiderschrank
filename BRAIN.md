# BRAIN — Gemeinsames Team-Gedächtnis

Lebendes Dokument für alles, was zwischen den Sessions und Teammitgliedern nicht verloren gehen soll. Wird von Menschen **und** von Claude gepflegt.

**Regeln für alle (Menschen wie Claudes):**
- Vor der Arbeit lesen, nach der Arbeit Änderungen eintragen — mit Datum und Namen. KI-Sitzungen dokumentieren dabei **jede** Aktion, siehe „📌 Protokollpflicht für alle KI-Sitzungen" unten.
- Einträge kurz halten; Details gehören in die Fachdokumente (ROADMAP.md, AVATAR-3D-KONZEPT.md), hier stehen Stand, Entscheidungen und Übergaben.
- Erledigtes aus „Offene Fragen" und „Nächste Schritte" entfernen statt anzusammeln — das Log unten ist das Archiv.
- Über Git synchronisieren: vor dem Lesen pullen, nach dem Eintragen committen und pushen.

---

## 📌 Protokollpflicht für alle KI-Sitzungen (dauerhaft — nicht löschen)

**Gilt für jede KI-Sitzung, die für dieses Projekt arbeitet** — egal für welches Teammitglied (Christian, Katha, Manuel) und egal mit welchem Werkzeug (Claude Code, Claude Cowork, Chat auf claude.ai, andere KIs).

1. **Vor der Arbeit:** Diese Datei komplett lesen (mit Git-Zugriff vorher pullen) und deine Sitzungskennung bestimmen — siehe „🪪 Deine Sitzungskennung" direkt hierunter.
2. **Alles, was du für das Projekt tust, wird hier dokumentiert** — Code- und Doku-Änderungen, getroffene Entscheidungen und übernommene Vorschläge, Recherchen und Experimente samt Ergebnis, Änderungen an Setup, Tools oder Repo-Struktur. Lieber ein kurzer Eintrag zu viel als eine Aktion, die niemand nachvollziehen kann.
3. **Wie:** Eintrag ins Log unten (neueste oben) im Format `**TT.MM.JJJJ · Sitzungskennung:** Kurzbeschreibung`. Zusätzlich die betroffenen Abschnitte nachziehen: Aktueller Stand, Offene Fragen, Wer macht gerade was, Wissensspeicher.
4. **Wann:** Nach jedem abgeschlossenen Arbeitsschritt, spätestens vor Ende der Sitzung — danach committen und pushen, damit alle anderen Sitzungen den Stand sofort sehen.
5. **Ohne Schreibzugriff:** Zuerst prüfen lassen, ob dein Claude-Werkzeug mit GitHub verknüpft ist — das war beim ersten Team-Test die Ursache (siehe Wissensspeicher); die Verknüpfung richtet dein Mensch einmal ein. Geht es danach immer noch nicht (z. B. Chat, der das Repo nur lesen kann): Am Ende der Antwort einen fertigen Log-Eintrag ausgeben und deinen Menschen bitten, ihn hier einzutragen und zu pushen.
6. **Nie ins Log:** Passwörter, API-Keys, Tokens oder andere Geheimnisse.

### 🪪 Deine Sitzungskennung

Jeder Log-Eintrag trägt die Kennung der Sitzung, die ihn geschrieben hat: **`Mensch/KI(Gerät.Anwendung)`**. Der Mensch bleibt die Konstante, Gerät und Anwendung machen die Sitzung eindeutig.

- **Mensch:** der Name, den sich dein Mensch selbst gibt — steht in „Wer ist wer", nicht der Git-Name
- **KI:** `Claude`; andere KIs mit ihrem eigenen Namen
- **Gerät:** kurzer, fester Name für den Rechner, z. B. `Laptop`, `PC`, `HomeOffice` — einmal festlegen, danach immer gleich schreiben
- **Anwendung:** `Code` = Claude Code · `Cowork` = Claude Cowork · `Chat` = Chat auf claude.ai

Beispiel: Katha arbeitet am Laptop mit Claude Code → `Katha/Claude(Laptop.Code)`.

**So bestimmst du deine Kennung — zu Beginn jeder Sitzung, nicht raten und nicht das Beispiel abschreiben:**

1. `git config user.name` ausführen und in „Wer ist wer" den Teamnamen nachschlagen.
2. `hostname` ausführen und in „Vergebene Kennungen" die Zeile mit diesem Rechnernamen und deiner Anwendung suchen. Genau ein Treffer → diese Kennung verwenden.
3. Kein eindeutiger Treffer oder kein Shell-Zugriff: deinen Menschen nach dem gewünschten Namen und Gerätenamen fragen — die Namen legen die Teammitglieder selbst fest. Dann die Tabellen ergänzen oder anpassen (neue Zeile anlegen, Namen ändern oder fehlenden Rechnernamen nachtragen), committen und pushen.
4. Deinem Menschen die ermittelte Kennung einmal nennen, damit sie bestätigt oder geändert werden kann.

**Wer ist wer**

| Teamname | Git-Name(n) |
|---|---|
| Christian | `Christian` |
| Katha | `Katharina`, `Kathamesser` |
| Manuel | `ManuelHerrmannRDF` |

*Die Namen legen die Teammitglieder selbst fest — „Katha" ist nur vorbelegt und darf geändert werden. Wer neu dazukommt, trägt beim ersten Kontakt eigenen Namen und Git-Namen ein.*

**Vergebene Kennungen**

| Kennung | Gerät | Anwendung | Rechnername (`hostname`) |
|---|---|---|---|
| `Christian/Claude(HomeOffice.Code)` | Hauptrechner (Gaming-PC) | Claude Code | — |
| `Christian/Claude(VMOffice.Cowork)` | VM „ClaudeOffice" auf dem Hauptrechner | Claude Cowork | — |
| `Christian/Claude(Laptop.Code)` | Schullaptop | Claude Code | `Deadsec` |
| `Christian/Claude(Laptop.Cowork)` | Schullaptop | Claude Cowork | — |
| `Manuel/Claude(Laptop.Cowork)` | Laptop | Claude Cowork | `laptop-manu` |

*„—" beim Rechnernamen = noch nicht erfasst; bei der nächsten Sitzung auf diesem Gerät nachtragen.*

*Ältere Log-Einträge tragen noch frühere Schreibweisen (`Christian/Claude`, `Christian/Claude Code`, `Christian/Claude (Cowork)`). Sie bleiben so stehen, sind aber kein Vorbild — neue Einträge nur mit einer Kennung aus dieser Tabelle.*

## 👋 An die anderen Claudes

Hallo Kollegen! Hier schreibt Christians Claude-Code-Session (17.07.2026). Schön, dass ihr da seid — ab jetzt arbeiten wir zu mehreren an diesem Projekt, und diese Datei ist unser gemeinsames Gedächtnis.

Kurz zur Orientierung, bevor ihr loslegt: Die Planungsphase ist weitgehend abgeschlossen — Roadmap und Avatar-Konzept liegen im Repo und sind mit dem Team abgestimmt. Bitte lest `CLAUDE.md` und die dort verlinkten Dokumente, bevor ihr größere Vorschläge macht; einige naheliegende Ideen (KI-Foto-Avatar, Unity, eigenes VTON-Modell hosten) wurden bereits bewusst verworfen, die Begründungen stehen in `AVATAR-3D-KONZEPT.md`. Der Flask-Code im Repo ist ein Experimentierstand aus der Testphase, nicht die Zielarchitektur — bitte nicht ungefragt umbauen, das Team entscheidet noch, was davon übernommen wird (siehe offene Fragen unten).

Was ihr für eure Menschen tun könnt: die offenen Entscheidungen unten vorantreiben, Einträge in „Wer macht gerade was" aktuell halten, und Erkenntnisse in den Wissensspeicher schreiben, statt sie in euren Sessions versickern zu lassen. Und tragt euch nach jeder Aktion ins Log ein — wie genau und mit welcher Kennung, steht oben unter „📌 Protokollpflicht für alle KI-Sitzungen".

Gute Zusammenarbeit! 🤝

*(Diesen Abschnitt gerne löschen, sobald alle drei Claudes einmal hier waren — dann hat er seinen Zweck erfüllt.)*

## Aktueller Stand (Kurzfassung)

- Projektphase: Planung abgeschlossen bis auf offene Punkte unten; Team experimentiert parallel mit Claude Pro und einem ersten Code-Stand (Flask-artige Webapp — gilt als Experimentierstand, nicht als Zielarchitektur).
- Tech-Stack entschieden: Python-Backend (Zielbild FastAPI), MongoDB, JavaScript/Three.js-Frontend. Details und Begründung: ROADMAP.md.
- Avatar-Ansatz entschieden: anpassbare 3D-Spielfigur (MakeHuman-Rohling + Three.js-Editor) statt KI-Foto-Generierung. Details: AVATAR-3D-KONZEPT.md.
- KI-Infrastruktur: GitHub = zentrale Quelle; Christians Obsidian-Vault ist ein synchronisierter Clone; CLAUDE.md gibt allen Claude-Sessions den Projektkontext. Seit 15.09.2026 gilt die Protokollpflicht: Alle KI-Sitzungen aller Teammitglieder dokumentieren jede Aktion in BRAIN.md, jeweils mit fester Sitzungskennung (Regeln und Kennungsliste im Abschnitt „📌 Protokollpflicht").

## Offene Fragen / anstehende Entscheidungen

- [ ] Frontend-Framework wählen (React oder Vue) — betrifft Phase 1
- [ ] KI-Anbieter für den Produktimport wählen — betrifft Phase 5
- [ ] Körpermaße: Regler mit internem cm-Mapping bestätigen (Empfehlung aus AVATAR-3D-KONZEPT.md)
- [ ] Umgang mit dem bestehenden Experimentier-Code klären: übernehmen, umbauen oder neu starten?
- [ ] Feature „Freunde" (existiert im Code, fehlt in der Planung): behalten und in die Roadmap aufnehmen — oder rausschneiden?
- [ ] Kleidungs-Kategorien für 3D-Vorlagen festlegen (Empfehlung: 5–6 zum Start)

## Wer macht gerade was

| Person | Aktuell dran an | Stand vom |
|---|---|---|
| Christian | Planung/KI-Infrastruktur mit Claude Code | 15.09.2026 |
| Katha | — (bitte selbst eintragen) | — |
| Manuel | Einstieg mit Claude Cowork: Repo verbunden, BRAIN.md gelesen, Sitzungskennung festgelegt | 06.10.2026 |

## Nächste Schritte (teamweit)

- [ ] Claude-Projekt auf claude.ai anlegen, GitHub-Connector verbinden, im Team teilen
- [ ] Jedes Teammitglied klont das Repo und arbeitet mit Claude Code darin
- [ ] Katha: maschinen-spezifische Permission aus `.claude/settings.json` in die lokale `settings.local.json` umziehen
- [ ] MakeHuman ausprobieren (jeder ~1 Stunde) und Eindruck hier festhalten
- [ ] Offene Entscheidungen (siehe oben) beim nächsten Team-Sync klären
- [ ] Katha und Manuel: GitHub mit dem eigenen Claude verknüpfen, einmal `git pull`, eine neue Claude-Code-Sitzung starten und fragen „Wie lautet deine Sitzungskennung für BRAIN.md?" — Ergebnis bestätigen (Test der Erstkontakt-Regel vom 15.09.2026)

## Wissensspeicher (Erkenntnisse, die nicht verloren gehen sollen)

- **Ready Player Me wurde 01/2026 abgeschaltet** (Netflix-Übernahme) — Lehre: keine Abhängigkeit von proprietären Plattformen; MakeHuman-Assets liegen als Dateien bei uns (CC0-Lizenz).
- **Werkstatt/Schaufenster-Prinzip:** MakeHuman ist Entwickler-Werkzeug zum Bau des Avatar-Rohlings (GLB mit Morph Targets); Nutzer sehen nur unseren eigenen Editor. Gespeichert wird pro Nutzer nur die Reglerstellung, nie das Modell.
- **Git-Falle auf Christians Rechner (erledigt 22.07.2026):** In `C:\Users\chris` lag ein versehentliches Git-Repo über das ganze Home-Verzeichnis (nur 1 Commit, kein Remote). Am 22.07.2026 entfernt (`.git` gelöscht) — es ging nichts Einzigartiges verloren. Lehre bleibt: in Home-/Desktop-Pfaden vor dem ersten Commit prüfen, ob nicht versehentlich ein zu weit gefasstes Repo offen ist; nur gezielt Projektpfade stagen.
- **KI-Sitzung kann nicht in BRAIN.md schreiben (15.09.2026):** Beim ersten Team-Test fehlte der KI-Sitzung einer Kollegin die Schreibberechtigung, sie konnte ihre Kennung nicht eintragen. Ursache: GitHub war noch nicht mit ihrem Claude verknüpft. Lösung: Verknüpfung einmal einrichten — Repo-Rechte oder `.claude/settings.json` mussten dafür nicht geändert werden.

---

## Log (neueste Einträge oben)

- **06.10.2026 · Manuel/Claude(Laptop.Cowork):** Erstkontakt Manuel (bisher „Teammitglied 3", Git-Name `ManuelHerrmannRDF`): Repo geklont, BRAIN.md und CLAUDE.md komplett gelesen. Sitzungskennung `Manuel/Claude(Laptop.Cowork)` von Manuel bestätigt; „Wer ist wer", „Vergebene Kennungen" und „Wer macht gerade was" ergänzt, Platzhalter „Teammitglied 3" in den aktuellen Abschnitten ersetzt (alte Log-Einträge unverändert). Hinweis: Die Sitzung hatte nur Lesezugriff, weil Manuels GitHub noch nicht mit Claude verknüpft war — Änderung wurde von Manuel eingetragen bzw. nach der Verknüpfung gepusht.
- **15.09.2026 · Christian/Claude(Laptop.Code):** Problem beim ersten Team-Test: Die KI-Sitzung einer Kollegin konnte ihre Kennung nicht in BRAIN.md eintragen (keine Schreibberechtigung). Ursache von Christian gefunden: GitHub war noch nicht mit ihrem Claude verknüpft. Keine Änderung an Repo-Rechten oder Claude-Freigaben nötig; Hinweis in Protokollpflicht (Punkt 5), Nächste Schritte und Wissensspeicher ergänzt.
- **15.09.2026 · Christian/Claude(Laptop.Code):** Entscheidung Christian: Die Teammitglieder legen ihre Namen für die Sitzungskennung selbst fest, verbindlich ist nur die Syntax `Mensch/KI(Gerät.Anwendung)`. Abschnitt „🪪 Deine Sitzungskennung" präzisiert: Name selbst gewählt, Vorbelegung „Katha" änderbar, ermittelte Kennung wird bestätigt oder geändert.
- **15.09.2026 · Christian/Claude(Laptop.Code):** Erstkontakt-Regel umgesetzt: neuer Abschnitt „🪪 Deine Sitzungskennung" in der Protokollpflicht (Aufbau der Kennung; Ablauf zu Sitzungsbeginn über `git config user.name` und `hostname`, sonst Menschen fragen; Tabellen „Wer ist wer" — Katharina/Kathamesser = Katha, per gemeinsamer Git-E-Mail geprüft — und „Vergebene Kennungen"; Hinweis auf alte Schreibweisen). Widerspruch in der Begrüßung beseitigt, CLAUDE.md angeglichen. Offene Frage aus der Prüfung erledigt; Test durch Katha und Teammitglied 3 unter „Nächste Schritte".
- **15.09.2026 · Christian/Claude(Laptop.Code):** Geprüft, ob eine neue KI-Sitzung eines Teammitglieds (Beispiel: Kathas Claude Code) über CLAUDE.md → BRAIN.md Zweck, Protokollpflicht und eigene Kennung erkennt. Ergebnis: Zweck und Protokollpflicht ja; Kennung nicht zuverlässig bestimmbar (Git-Name ≠ Teamname, Gerätenamen und Kennungsliste stehen nur in Christians Vault, Teammitglied 3 ohne Namen); zwei widersprüchliche Stellen (CLAUDE.md „nach relevanter Arbeit … Datum + Name", Begrüßung „Name eures Menschen genügt"). Korrektur vorgeschlagen, wartet auf Christians Freigabe.
- **15.09.2026 · Christian/Claude(Laptop.Code):** Abschnitt „📌 Protokollpflicht für alle KI-Sitzungen" angelegt: Jede KI-Sitzung jedes Teammitglieds (Claude Code, Cowork, claude.ai-Chat, andere KIs) dokumentiert ab sofort alle Aktionen fürs Projekt hier; Sitzungen ohne Schreibzugriff geben den Eintrag für ihren Menschen aus. „Regeln für alle" und „Aktueller Stand" angepasst, UNIBRAIN.md nachgezogen.
- **22.07.2026 · Christian/Claude Code:** Versehentliches Home-Git-Repo unter `C:\Users\chris` entfernt (siehe Wissensspeicher); StyleHUB-Repo unberührt. UNIBRAIN.md aktualisiert: StyleHUB-Kurzstand in die Projektübersicht hochgezogen + neue vault-weite Konvention „umgesetzte Änderungen immer im Brain nachziehen".
- **21.07.2026 · Christian/Claude (Cowork):** Cowork-Claude hat sich eingeklinkt und liest/schreibt ab jetzt ebenfalls in BRAIN.md.
- **17.07.2026 · Christian/Claude:** BRAIN.md angelegt. KI-Infrastruktur eingerichtet: Vault-Clone ↔ GitHub-Sync, CLAUDE.md gepusht. Planungsdokumente (ROADMAP, AVATAR-3D-KONZEPT, roadmap.html) liegen im Repo.
- **12.07.2026 · Christian/Claude:** Tech-Stack entschieden (Python/FastAPI, MongoDB, Three.js) und in ROADMAP.md dokumentiert.
- **~10.07.2026 · Christian/Claude:** Avatar-Konzept umgestellt: 3D-Spielfigur statt KI-Foto-Generierung; AVATAR-3D-KONZEPT.md ersetzt KI-AVATAR-KONZEPT.md.
- **09.07.2026 · Christian/Claude:** Erste Roadmap erstellt (8 Phasen, 26 Wochen).
