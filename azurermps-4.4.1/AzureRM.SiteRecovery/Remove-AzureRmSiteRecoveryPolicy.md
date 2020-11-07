---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662889"
---
# Remove-AzureRmSiteRecoveryPolicy

## Synopsis
Entfernt eine Replikationsrichtlinie für die Standortwiederherstellung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRMSiteRecoveryPolicy** entfernt eine Azure Site Recovery-Replikationsrichtlinie.

## Beispiele

## Parameter

### – Richtlinien
Gibt das Website Wiederherstellungsrichtlinien Objekt an.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### ASRPolicy
Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmSiteRecoveryPolicy](./Get-AzureRmSiteRecoveryPolicy.md)

[Neu – AzureRmSiteRecoveryPolicy](./New-AzureRmSiteRecoveryPolicy.md)
