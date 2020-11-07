---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 50d0345fea26d233147ad8373ab3daae785d6715
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663946"
---
# Get-AzureRmDtlAutoStartPolicy

## Synopsis
Ruft die Richtlinie für den automatischen Start einer Übungseinheit in DevTest Labs ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDtlAutoStartPolicy** " Ruft die Richtlinie für den automatischen Start einer Übungseinheit ab, die virtuelle Lab-Computer für den automatischen Start plant.
Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie sowie die Tage der Woche und Uhrzeit zurück, die Sie festgelegt haben, damit Lab-virtuelle Computer für den automatischen Start geplant werden können.

## Beispiele

## Parameter

### -LabName
Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für den automatischen Start erhält.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.

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

## Ausgaben

### Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule
Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit gestartet werden müssen.

## Notizen

## Verwandte Links

[Satz-AzureRmDtlAutoStartPolicy](./Set-AzureRmDtlAutoStartPolicy.md)


