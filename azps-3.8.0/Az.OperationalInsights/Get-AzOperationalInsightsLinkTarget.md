---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: 72841dc8ecc90c14bb41ae8f0f207d990afec9a8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007477"
---
# Get-AzOperationalInsightsLinkTarget

## Synopsis
Ruft Konten ab, die keinem Abonnement zugeordnet sind.

## Syntax

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzOperationalInsightsLinkTarget** " listet vorhandene Konten auf, die keinem Azure-Abonnement zugeordnet sind.
Wenn Sie einen neuen Arbeitsbereich mit einem vorhandenen Konto verknüpfen möchten, verwenden Sie eine Kunden-ID, die von diesem Vorgang in der Eigenschaft Kunden-ID eines neuen Arbeitsbereichs zurückgegeben wird.

## Beispiele

### Beispiel 1: Abrufen von unverknüpften Konten
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

Dieser Befehl ruft Konten mit unverknüpften Konten ab, die der ID des Anrufers gehören.

## Parameter

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount

## Notizen

## Verwandte Links

[Azure-Cmdlets für operationelle Einblicke](/powershell/module/az.operationalinsights)


