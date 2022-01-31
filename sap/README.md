# SAP
- [Transactions](#transactions)

## Upload transport
Ursprungsystem:
1. `se10` um den Transport freizugeben
2. Mit filezilla oder `CG3Y` Cofiles und Data herunterladen

Kundensystem:
1. `al11` um den Upload-Folder auszulesen (`DIR_TRANS`)
2. `cg3z` um Datei hochzuladen (data = R*, cofiles = K*)
3. `stms` -> `Zusätze` -> `Weitere Aufträge` -> `Anhängen` -> Transport eingeben (`ABMK*`)
4. Auftrag auswählen -> `Auftrag` -> `Auftrag importieren`