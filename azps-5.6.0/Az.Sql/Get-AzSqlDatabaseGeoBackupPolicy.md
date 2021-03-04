---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 132103e86f514bf5d7028ef4dc691225904396fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950027"
---
# Get-AzSqlDatabaseGeoBackupPolicy

## SYNOPSIS
Ruft eine Datenbank-Geosicherungsrichtlinie ab.

## SYNTAX

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzSqlDatabaseGeoBackupPolicy-Cmdlet** ruft die Geosicherungsrichtlinie ab, die für diese Datenbank registriert ist.
Dies ist eine Azure Backup-Ressource, die zum Definieren der Sicherungsspeicherrichtlinie verwendet wird.

## BEISPIELE

### Beispiel 1

Ruft eine Datenbank-Geosicherungsrichtlinie ab. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlDatabaseGeoBackupPolicy -DatabaseName db1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## PARAMETER

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet die Geosicherungsrichtlinie erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.

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
Gibt den Namen des Servers an, der die Datenbank hostet.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel

## NOTIZEN

## VERWANDTE LINKS

[Set-AzSqlDatabaseGeoBackupPolicy](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)
