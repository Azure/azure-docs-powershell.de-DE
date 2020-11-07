---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662746"
---
# Get-AzureRmDataLakeAnalyticsCatalogItem

## Synopsis
Ruft ein Data Lake Analytics-Katalogelement oder eine Art von Elementen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Der **Get-AzureRmDataLakeAnalyticsCatalogItem** Ruft ein angegebenes Azure Data Lake Analytics-Katalogelement ab oder ruft Katalogelemente eines angegebenen Typs ab.

## Beispiele

### Beispiel 1: Abrufen einer angegebenen Datenbank
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Dieser Befehl ruft die angegebene Datenbank ab.

### Beispiel 2: Abrufen von Tabellen in einer bestimmten Datenbank und einem angegebenen Schema
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Mit diesem Befehl wird eine Liste der Tabellen in der angegebenen Datenbank abgerufen.

## Parameter

### -Konto
Gibt den Namen des Daten Lake Analytics-Kontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
Gibt den Katalog Elementtyp für die Elemente an, die abgerufen oder aufgelistet werden.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Datenbank
- Schema
- Assembly
- Tabelle
- TableValuedFunction
- Statistiken
- ExternalDataSource
- Ansicht
- Verfahren
- Geheimnis
- Credential
- Typen
- Partitions

```yaml
Type: CatalogItemType
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
Gibt den mehrteiligen Pfad zum abzurufenden Element oder das übergeordnete Element der Liste der Elemente an.
Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### CatalogItem
Das angegebene Katalogelement

### Liste<CatalogItem>
Die Liste der angegebenen Katalogelemente unterhalb des zugehörigen Containers.

## Notizen

## Verwandte Links

[Test-AzureRmDataLakeAnalyticsCatalogItem](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


