---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949952"
---
# Get-AzSqlDatabaseUpgradeHint

## SYNOPSIS
Ruft Preisstufenhinweise für eine Datenbank ab.

## SYNTAX

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzSqlDatabaseUpgradeHint-Cmdlet** erhält Preisstufenhinweise zum Upgrade einer Azure SQL Datenbank.
Datenbanken, die sich noch in web- und business-Preisstufen befinden, erhalten den Hinweis zum Upgrade auf die neuen Tarife Basic, Standard oder Premium.
Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Erhalten von Empfehlungen für alle Datenbanken auf einem Server
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server mit dem Namen Server01 zurück.

### Beispiel 2: Erhalten von Empfehlungen für eine bestimmte Datenbank
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Dieser Befehl gibt Upgradehinweise für eine bestimmte Datenbank zurück.

### Beispiel 3: Empfehlung für alle Datenbanken erhalten, die sich nicht in einem pool für flexible Datenbanken befinden
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Dieser Befehl gibt Upgradehinweise für alle Datenbanken zurück, die sich nicht in einem pool für flexible Datenbanken befinden.

### Beispiel 4: Erhalten von Empfehlungen für alle Datenbanken auf einem Server mithilfe von Filtern
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server mit dem Namen Server01 zurück, die mit "Datenbank" beginnen.

## PARAMETER

### -DatabaseName
Gibt den Namen der SQL an, für die dieses Cmdlet einen Upgradehinweis erhält.
Wenn Sie keine Datenbank angeben, ruft dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server ab.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -ExcludeElasticPoolCandidates
Gibt an, ob Datenbanken in flexiblen Datenbankpools von den zurückgegebenen Empfehlungen ausgeschlossen werden.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.

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
Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgradehinweis erhält.

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

### System.Boolean

## AUSGABEN

### Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties

## NOTIZEN

## VERWANDTE LINKS

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


