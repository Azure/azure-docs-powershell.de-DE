---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006071"
---
# Set-AzureSqlDatabase

## Synopsis
Legt Eigenschaften für eine Azure SQL-Datenbank fest.

## Syntax

### ByNameWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureSqlDatabase** " legt Eigenschaften für eine Azure SQL-Datenbank fest.
Sie können die Datenbank nach Namen angeben oder ein Azure SQL-Datenbankobjekt über die Pipeline übergeben.
Sie können den Server nach Namen angeben oder einen Azure SQL-Datenbankserver-Verbindungskontext übergeben.
Erstellen Sie einen Verbindungskontext, indem Sie das Cmdlet **New-AzureSqlDatabaseServerContext** ausführen.
Wenn Sie den Server nach Namen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung zu authentifizieren.

## Beispiele

### Beispiel 1: Ändern der Größe einer Datenbank mithilfe eines Verbindungskontexts
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

In diesem Beispiel wird die Größe der Datenbank mit dem Namen Database01 auf 20 GB im Azure SQL-Datenbankserver-Verbindungskontext $Context geändert.

### Beispiel 2: Ändern der Größe einer Datenbank mit einem Servernamen
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

In diesem Beispiel wird die Größe der Datenbank mit dem Namen Database01 auf 20 GB auf dem Server mit dem Namen lpqd0zbr8y geändert.

## Parameter

### -ConnectionContext
Gibt den Verbindungskontext eines Servers an.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datenbank
Gibt ein Objekt an, das die Azure SQL-Datenbank darstellt, die von diesem Cmdlet geändert wird.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Gibt die neue Edition für die Azure SQL-Datenbank an.
Gültige Werte sind: 

- Keine
- Web
- Business
- Grundlegende
- Standard
-  Premium

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
Ermöglicht die Ausführung der Aktion, ohne dass Sie zur Bestätigung aufgefordert werden.

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
Gibt die neue maximale Größe für die Datenbank in Bytes an.
Sie können entweder diesen Parameter oder den *MaxSizeGB* -Parameter angeben.
Sehen Sie sich den *MaxSizeGB* -Parameter für akzeptable Werte auf der Grundlage der Edition an.

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
Gibt die neue maximale Größe für die Datenbank in Gigabyte an.
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

### -Datenbankname
Gibt den neuen Namen der Datenbank an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt die aktualisierte Azure SQL-Datenbank zurück.

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
Gibt den Namen des Servers an, der die Datenbank enthält, die von diesem Cmdlet geändert wird.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjective
Gibt ein Objekt an, das das neue Dienst Ziel (Leistungsstufe) für diese Datenbank darstellt.
Gültige Werte sind: 

- Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

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

### -Sync
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Datenbank aktualisieren](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Neu – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


