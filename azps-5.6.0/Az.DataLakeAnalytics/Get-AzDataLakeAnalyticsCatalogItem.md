---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 738820c4c06fd32862def36ec76983968e99efb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942819"
---
# Get-AzDataLakeAnalyticsCatalogItem

## SYNOPSIS
Ruft ein Data Lake Analytics-Katalogelement oder Elementtypen ab.

## SYNTAX

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Die **Get-AzDataLakeAnalyticsCatalogItem** ruft ein angegebenes Azure Data Lake Analytics-Katalogelement ab oder ruft Katalogelemente eines angegebenen Typs ab.

## BEISPIELE

### Beispiel 1: Erhalten einer angegebenen Datenbank
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Dieser Befehl ruft die angegebene Datenbank ab.

### Beispiel 2: Erhalten von Tabellen in einer angegebenen Datenbank und einem bestimmten Schema
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Dieser Befehl ruft eine Liste der Tabellen in der angegebenen Datenbank ab.

## PARAMETER

### -Konto
Gibt den Namen des Data Lake Analytics-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
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

### -ItemType
Gibt den Katalogelementtyp der Elemente an, die abgerufen oder aufgelistet werden.
Die zulässigen Werte für diesen Parameter sind:
- Datenbank
- Schema
- Assembly
- Tabelle
- TableValuedFunction
- TableStatistics
- ExternalDataSource
- Ansicht
- Verfahren
- Geheim
- Anmeldeinformationen
- Typen
- TablePartition

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den mehrteiligen Pfad zum abzurufenden Element oder zum übergeordneten Element der zu listenden Elemente an.
Die Teile des Pfads sollten durch einen Zeitraum (.) getrennt sein.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance

## AUSGABEN

### Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem

## NOTIZEN

## VERWANDTE LINKS

[Test-AzDataLakeAnalyticsCatalogItem](./Test-AzDataLakeAnalyticsCatalogItem.md)


