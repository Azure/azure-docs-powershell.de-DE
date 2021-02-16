---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402421"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
Überprüft den Status von Kopierbeziehungen.

## SYNTAX

### ByServerNameOnly (Standard)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzureSqlDatabaseCopy"** überprüft den Status einer oder mehreren aktiven Kopierbeziehungen.
Führen Sie dieses Cmdlet aus, nachdem Sie das cmdlet Start-AzureSqlDatabaseCopy oder Stop-AzureSqlDatabaseCopy ausgeführt haben.
Sie können eine bestimmte Kopierbeziehung, alle Kopierbeziehungen oder eine gefilterte Liste von Kopierbeziehungen überprüfen, z. B. alle Kopien auf einem bestimmten Zielserver.
Sie können dieses Cmdlet auf dem Server ausführen, der die Quell- oder Zieldatenbank hostet.

Dieses Cmdlet ist synchron.
Das Cmdlet blockiert die Azure PowerShell-Konsole, bis ein Statusobjekt zurückgegeben wird.

Die *Parameter "PartnerServer"* *und "PartnerDatabase"* sind optional.
Wenn Sie keinen der Parameter angeben, gibt dieses Cmdlet eine Ergebnistabelle zurück.
Wenn Sie nur den Status einer bestimmten Datenbank anzeigen möchten, geben Sie beide Parameter an.

## BEISPIELE

### Beispiel 1: Anzeigen des Kopierstatus einer Datenbank
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Dieser Befehl ruft den Status der Datenbank mit dem Namen "Orders" auf dem Server namens lpqd0zbr8y ab.
Der *Parameter "PartnerServer"* schränkt diesen Befehl auf den Server bk0b8kf658 ein.

### Beispiel 2: Den Status aller Kopien auf einem Server erhalten: Anzeigen des Status aller Kopien auf einem Server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Dieser Befehl ruft den Status aller aktiven Kopien auf dem Server mit dem Namen lpqd0zbr8y ab.

## PARAMETERS

### -Database
Gibt ein Objekt an, das die Azure SQL darstellt.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Gibt ein Objekt an, das eine Datenbank darstellt.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.
Dieser Parameter akzeptiert die Pipelineeingabe.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Quelldatenbank an.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Gibt den Namen der sekundären Datenbank an.
Wenn diese Datenbank nicht in der dynamischen sys.dm_database_copies gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Gibt den Namen des Servers an, der die Zieldatenbank hostet.
Wenn dieser Server in der dynamischen sys.dm_database_copies nicht gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
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

### -ServerName
Gibt den Namen des Servers an, auf dem sich die Datenbankkopie befindet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## AUSGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## HINWEISE
* Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie im New-AzureSqlDatabaseServerContext-Cmdlet.

## LINKS ZU VERWANDTEN THEMEN

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


