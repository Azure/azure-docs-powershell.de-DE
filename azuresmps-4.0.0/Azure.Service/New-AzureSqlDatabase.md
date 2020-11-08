---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006179"
---
# New-AzureSqlDatabase

## Synopsis
Erstellt eine Azure SQL-Datenbank.

## Syntax

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureSqlDatabase** erstellt eine Azure SQL-Datenbank.
Sie können den Server angeben, indem Sie einen Azure SQL-Datenbankserver-Verbindungskontext verwenden, den Sie mit dem Cmdlet **New-AzureSqlDatabaseServerContext** erstellen.
Wenn Sie den Servernamen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.

Wenn Sie eine neue Datenbank erstellen, indem Sie einen Azure SQL-Datenbankserver angeben, erstellt das Cmdlet **New-AzureSqlDatabase** einen temporären Verbindungskontext mit dem angegebenen Servernamen und den aktuellen Azure-Abonnementinformationen, um den Vorgang auszuführen.

## Beispiele

### Beispiel 1: Erstellen einer Datenbank
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Dieser Befehl erstellt eine Azure SQL-Datenbank mit dem Namen "Database1" für den Azure SQL-Datenbankserver-Verbindungskontext $Context.

### Beispiel 2: Erstellen einer Datenbank im aktuellen Abonnement
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

In diesem Beispiel wird eine Datenbank mit dem Namen Database1 im angegebenen Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y erstellt.
Das Cmdlet verwendet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.

## Parameter

### -Sortierung
Gibt eine Sortierung für die neue Datenbank an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionContext
Gibt den Verbindungskontext eines Servers an, auf dem dieses Cmdlet eine Datenbank erstellt.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der neuen Datenbank an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Gibt die Edition für die neue Azure SQL-Datenbank an.
Gültige Werte sind: 

- Keine
- Web
- Business
- Grundlegende
- Standard
-  Premium

Der Standardwert ist Web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ermöglicht die Ausführung der Aktion, ohne dass der Benutzer zur Bestätigung aufgefordert wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeBytes
Gibt die maximale Größe der Datenbank in Bytes an.
Sie können entweder diesen Parameter oder den *MaxSizeGB* -Parameter angeben.
Lesen Sie die Beschreibung des *MaxSizeGB* -Parameters für akzeptable Werte auf der Grundlage der Edition.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Gibt die maximale Größe der Datenbank in Gigabyte an.
Sie können entweder diesen Parameter oder den *MaxSizeBytes* -Parameter angeben.
Die akzeptablen Werte unterscheiden sich je nach Edition.

Grundlegende Editions Werte: 1 oder 2

Standard Editions Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 oder 250

Premium Edition-Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 oder 500

Web Edition-Werte: 1 oder 5

Business Edition-Werte: 10, 20, 30, 40, 50, 100 oder 150

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Azure SQL-Datenbankservers an, der die neue Datenbank enthalten soll.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjective
Gibt ein Objekt an, das das neue Dienst Ziel (Leistungsstufe) für diese Datenbank darstellt.
Dieser Wert stellt die Ebene der Ressourcen dar, die dieser Datenbank zugewiesen sind.
Gültige Werte sind: 

Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c-Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b-Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928-Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) ist Teil des neuesten SQL-Datenbankupdates V12 (Preview).
Weitere Informationen finden Sie unter Neuerungen in der Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Notizen
* Verwenden Sie das Remove-AzureSqlDatabase-Cmdlet, um eine von **New-AzureSqlDatabase** erstellte Datenbank zu löschen.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Datenbank erstellen](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Satz-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


