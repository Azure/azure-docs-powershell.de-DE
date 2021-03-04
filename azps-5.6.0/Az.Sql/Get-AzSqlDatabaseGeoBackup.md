---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922659"
---
# Get-AzSqlDatabaseGeoBackup

## SYNOPSIS
Ruft eine georedundant gesicherte Datenbank ab.

## SYNTAX

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzSqlDatabaseGeoBackup-Cmdlet** ruft eine angegebene georedundierte Sicherung einer SQL-Datenbank oder aller verfügbaren georedundierten Sicherungen auf einem angegebenen Server ab.
Eine georedundant gesicherte Ressource ist eine restorable Ressource, die Datendateien von einem separaten geografischen Speicherort verwendet.
Sie können Geo-Restore verwenden, um eine georedundant gesicherte Sicherung im Fall eines regionalen Ausfalls wiederherzustellen, um Ihre Datenbank in einer neuen Region wiederherzustellen.
Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Erhalten aller georedundanter Sicherungen auf einem Server
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Dieser Befehl ruft alle verfügbaren georedundanziellen Sicherungen auf einem angegebenen Server ab.

### Beispiel 2: Erhalten einer angegebenen georedundanzen Sicherung
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Dieser Befehl ruft die georedundierte Datenbanksicherung namens ContosoDatabase ab.

### Beispiel 3: Erhalten aller georedundanter Sicherungen auf einem Server mithilfe von Filtern
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Dieser Befehl ruft alle verfügbaren geo redundanten Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.

## PARAMETER

### -DatabaseName
Gibt den Namen der zu erhaltenden Datenbank an.

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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel

## NOTIZEN

## VERWANDTE LINKS

[Übersicht: Cloud business continuity and database disaster recovery with SQL Database](http://go.microsoft.com/fwlink/?LinkId=746881)

[Wiederherstellen einer Azure SQL-Datenbank nach einem Ausfall](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)
