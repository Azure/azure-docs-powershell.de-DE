---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144212"
---
# Get-AzSqlDatabaseGeoBackup

## SYNOPSIS
Ruft eine geo redundante Sicherung einer Datenbank ab.

## SYNTAX

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzSqlDatabaseGeoBackup"** ruft eine angegebene georedundierte Sicherung einer SQL-Datenbank oder alle verfügbaren georedundierten Sicherungen auf einem angegebenen Server ab.
Eine georedundable Sicherung ist eine wiederversetzbare Ressource, die Datendateien von einem separaten geografischen Standort verwendet.
Sie können eine Geo-Restore für den Fall eines regionalen Ausfalls zum Wiederherstellen einer georedundanzen Sicherung verwenden, um die Datenbank in eine neue Region wiederherzustellen.
Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Alle georedundanzen Sicherungen auf einem Server erhalten
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Dieser Befehl ruft alle verfügbaren georedundanzen Sicherungen auf einem angegebenen Server ab.

### Beispiel 2: Erhalten einer angegebenen georedundanzen Sicherung
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Dieser Befehl ruft die georedundierte Datenbanksicherung namens "ContosoDatabase" ab.

### Beispiel 3: Erhalten aller georedundanzen Sicherungen auf einem Server mithilfe von Filtern
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Dieser Befehl ruft alle verfügbaren georedundanzen Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.

## PARAMETERS

### -DatabaseName
Gibt den Namen der datenbank an, die sie erhalten soll.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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
Gibt den Namen der Ressourcengruppe an, der der SQL Datenbankserver zugewiesen ist.

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

### -ServerName
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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Übersicht: Cloud-Geschäftskontinuität und Datenbank-Notfallwiederherstellung mit SQL Datenbank](http://go.microsoft.com/fwlink/?LinkId=746881)

[Wiederherstellen einer Azure SQL-Datenbank nach einem Ausfall](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)
