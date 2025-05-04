# AVD2-Task1
Skupinová práce na interaktivním dashboardu, zpracovávajícím data získaná na DOD

# 1. Krok 
#### Skupina
David Král (**@davidkral9**), Marie Kleckerová (**@majdakleckerova**)

#### Vybrané atributy
1. Čas dne, kdy byl dotazník vyplněn
2. 1. Jak jste se dozvěděli o DOD UJEP? (možnost více odpovědí)
3. Které sociální sítě UJEP znáte? (možnost více odpovědí)
4. 6. Je nabídka využívaných sociálních sítí UJEP dostačující?
12. Na jakou fakultu UJEP se hlásíte? (možnost více odpovědí)
13. 23. Jste:


#### Vybraný software
- PowerBI
- Apache Superset
- Metabase


#### SQL Query
```sql
SELECT 'Fakulta strojního inženýrství (FSI)' AS Fakulta, COUNT(*) AS Počet FROM dod_2025 WHERE fakulta_fsi = true
UNION ALL
SELECT 'Fakulta životního prostředí (FŽP)', COUNT(*) FROM dod_2025 WHERE fakulta_fzp = true
UNION ALL
SELECT 'Fakulta umění a designu (FUD)', COUNT(*) FROM dod_2025 WHERE fakulta_fud = true
UNION ALL
SELECT 'Filozofická fakulta (FF)', COUNT(*) FROM dod_2025 WHERE fakulta_ff = true
UNION ALL
SELECT 'Fakulta zdravotnických studií (FZS)', COUNT(*) FROM dod_2025 WHERE fakulta_fzs = true
UNION ALL
SELECT 'Přírodovědecká fakulta (PřF)', COUNT(*) FROM dod_2025 WHERE fakulta_prf = true
UNION ALL
SELECT 'Pedagogická fakulta (PF)', COUNT(*) FROM dod_2025 WHERE fakulta_pf = true
UNION ALL
SELECT 'Fakulta sociálně ekonomická (FSE)', COUNT(*) FROM dod_2025 WHERE fakulta_fse = true

```
