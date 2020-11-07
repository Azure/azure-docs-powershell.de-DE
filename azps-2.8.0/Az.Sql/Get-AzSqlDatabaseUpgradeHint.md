---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825620"
---
# Get-AzSqlDatabaseUpgradeHint

## Synopsis
Ruft Preisstufen Hinweise für eine Datenbank ab.

## Syntax

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlDatabaseUpgradeHint** " ruft Preisstufen Hinweise für das Upgrade einer Azure SQL-Datenbank ab.
Datenbanken, die sich noch im Web-und Business-Preisniveau befinden, erhalten den Hinweis, dass Sie ein Upgrade auf die neuen Standard-, Standard-oder Premium-Preisstufen durchführen können.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Abrufen von Empfehlungen für alle Datenbanken auf einem Server
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken auf dem Server mit dem Namen "Server01" zurück.

### Beispiel 2: Abrufen von Empfehlungen für eine bestimmte Datenbank
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Dieser Befehl gibt Aktualisierungshinweise für eine bestimmte Datenbank zurück.

### Beispiel 3: Abrufen einer Empfehlung für alle Datenbanken, die sich nicht in einem elastischen datenbankpool befinden
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken zurück, die sich nicht in einem elastischen datenbankpool befinden.

### Beispiel 4: Abrufen von Empfehlungen für alle Datenbanken auf einem Server mithilfe von Filtern
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken auf dem Server mit dem Namen "Server01" zurück, die mit "Datenbank" beginnen.

## Parameter

### -DatabaseName
Gibt den Namen der SQL-Datenbank an, für die dieses Cmdlet einen Upgrade-Hinweis erhält.
Wenn Sie keine Datenbank angeben, erhält dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

### -ExcludeElasticPoolCandidates
Gibt an, ob Datenbanken in elastischen Daten Bank Pools von den zurückgegebenen Empfehlungen ausgeschlossen werden.

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
Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgrade-Hinweis erhält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Boolean

## Ausgaben

### Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties

## Notizen

## Verwandte Links

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


