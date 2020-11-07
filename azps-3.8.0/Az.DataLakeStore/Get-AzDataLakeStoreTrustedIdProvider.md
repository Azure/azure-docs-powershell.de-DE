---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846131"
---
# Get-AzDataLakeStoreTrustedIdProvider

## Synopsis
Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.
Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.

## Syntax

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDataLakeStoreTrustedIdProvider** " Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.
Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgelistet.

## Beispiele

### Beispiel 1: Abrufen eines bestimmten vertrauenswürdigen Identitätsanbieters
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

Gibt den Anbieter mit dem Namen "MyProvider" aus dem Konto "ContosoADL" zurück.

### Beispiel 2: Auflisten aller Anbieter in einem Konto
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

Listet alle Anbieter unter dem Konto "ContosoADL" auf.

## Parameter

### -Konto
Das Data Lake Store-Konto zum Abrufen des vertrauenswürdigen Identitätsanbieters aus

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

### -Name
Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider

## Notizen

## Verwandte Links
