---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503878"
---
# Get-AzureRmBillingPeriod

## Synopsis
Besorgen Sie sich Abrechnungsperioden des Abonnements.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Liste (Standard)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Einzel
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBillingPeriod** " ruft Abrechnungsperioden des Abonnements ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Abrufen aller verfügbaren Abrechnungsperioden des Abonnements.

### Beispiel 2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

Abrufen des Abrechnungszeitraums des Abonnements mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Erhalten Sie höchstens zwei Abrechnungsperioden des Abonnements.

## Parameter

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

### -MaxCount
Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name eines bestimmten Abrechnungszeitraums, der abgerufen werden soll.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Abrechnungs. Models. PSBillingPeriod; Microsoft. Azure. Commands. Billing; Version = 0.14.0.0; Kultur = neutral; PublicKeyToken = null]]
Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod

## Notizen

## Verwandte Links

