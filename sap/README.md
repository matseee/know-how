# SAP
- [Tabellenpflege mit se16n + debugger](#tabellenpflege)
- [Transaktionen](#transaktionen)
- [Transport](#transport-zum-kundensystem)

## Tabellenpflege mit se16n + debugger
1. `/h`
1. `F8`
1. Folgende Variablen setzen `GD-EDIT = X` und `GD-SAPEDIT = X`
1. `F8`

## Transaktionen

### für die Fehleranalye
| Transaktion | Beschreibung |
| --- | --- |
| st22 | Abap Dumps |
| stauthtrace | Auth-Trace |

### für die Entwicklung:
| Transaktion | Beschreibung |
| --- | --- |
| se80 | ABAP Entwicklungsumgebung |
| se16n | Allgemeine Tabellenanzeige |
| se37 | Funktionsbausteine ausführen |

### zum Transport von Entwicklungsumgebung
| Transaktion | Beschreibung |
| --- | --- |
| se10 | Transport Organizer |
| stms | Transport Manager |

### für die Netzwerk-Kommunikation
| Transaktion | Beschreibung |
| --- | --- |
| sicf | Pflege HTTP-Services |
| sm59 | RFC Pflege |

## Transport zum Kundensystem
Ursprungsystem:
1. `se10` um den Transport freizugeben
2. Mit filezilla oder `CG3Y` Cofiles und Data herunterladen

Kundensystem:
1. `al11` um den Upload-Folder auszulesen (`DIR_TRANS`)
2. `cg3z` um Datei hochzuladen (data = R*, cofiles = K*)
3. `stms` -> `Zusätze` -> `Weitere Aufträge` -> `Anhängen` -> Transport eingeben 
4. Auftrag auswählen -> `Auftrag` -> `Auftrag importieren`