---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663521"
---
# Remove-AzureRmSiteRecoveryStorageClassificationMapping

## Synopsis
Entfernt eine Speicher Klassifikations Zuordnung aus der Websitewiederherstellung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** entfernt eine Speicher Klassifikations Zuordnung aus Azure Site Recovery.

## Beispiele

## Parameter

### -StorageClassificationMapping
Gibt eine Speicher Klassifikations Zuordnung an, die von diesem Cmdlet entfernt wird.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
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

### ASRStorageClassificationMapping
Der Parameter "StorageClassificationMapping" akzeptiert den Wert vom Typ "ASRStorageClassificationMapping" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

[Get-AzureRmSiteRecoveryStorageClassificationMapping](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[Neu – AzureRmSiteRecoveryStorageClassificationMapping](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
