---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008906"
---
# Get-AzSqlDatabaseGeoBackup

## Synopsis
Ruft eine Geo-redundante Sicherung einer Datenbank ab.

## Syntax

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlDatabaseGeoBackup** " Ruft eine angegebene Geo-redundante Sicherung einer SQL-Datenbank oder aller verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.
Bei einer Geo-redundanten Sicherung handelt es sich um eine wiederherstellbare Ressource, die Datendateien von einem separaten geografischen Standort verwendet.
Sie können Geo-Restore verwenden, um eine Geo-redundante Sicherung bei einem regionalen Ausfall wiederherzustellen, um Ihre Datenbank in einer neuen Region wiederherzustellen.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Abrufen aller Geo-redundanten Sicherungen auf einem Server
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Dieser Befehl ruft alle verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.

### Beispiel 2: Abrufen einer angegebenen Geo-redundanten Sicherung
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Mit diesem Befehl wird die Daten Bank Geo-redundante Sicherung mit dem Namen ContosoDatabase abgerufen.

### Beispiel 3: Abrufen aller Geo-redundanten Sicherungen auf einem Server mithilfe von Filtern
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Dieser Befehl ruft alle verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.

## Parameter

### -DatabaseName
Gibt den Namen der Datenbank an, die abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der SQL-Datenbankserver zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, der die wiederherzustellende Sicherung hostet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel

## Notizen

## Verwandte Links

[Übersicht: Cloud Business Continuity und Datenbank-Disaster Recovery mit SQL-Datenbank](http://go.microsoft.com/fwlink/?LinkId=746881)

[Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall](http://go.microsoft.com/fwlink/?LinkId=746882)

[Wiederherstellen – AzSqlDatabase](./Restore-AzSqlDatabase.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)
