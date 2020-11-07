---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 1390efccef67e6bfb626e9b31d1a58c72c9fb36e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663783"
---
# Get-AzureRmBatchLocationQuotas

## Synopsis
Ruft die Stapelverarbeitungs Dienst Kontingente für Ihr Abonnement an der angegebenen Position ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Ruft die Stapelverarbeitungs Dienst Kontingente für das angegebene Abonnement an der angegebenen Position ab.

## Beispiele

### Beispiel 1: Abrufen der Batch Dienst Kontingente für das Abonnement in der Region West Amerika
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der West US-Region ab.
Der Rückgabewert gibt an, dass dieses Abonnement nur ein Stapelverarbeitungs Konto in diesem Bereich erstellen kann.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Standort
Gibt den Bereich an, für den das Cmdlet die Kontingente überprüft.
Weitere Informationen finden Sie unter Azure-Bereiche ( https://azure.microsoft.com/regions) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas

## Notizen

## Verwandte Links

