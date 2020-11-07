---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4717fa187a8bd8234cd786ff5c6ad6d1678696b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663948"
---
# Get-AzureRmDtlAutoShutdownPolicy

## Synopsis
Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit in DevTest Labs ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDtlAutoShutdownPolicy** " Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit ab, mit der Sie alle virtuellen Computer in einer Übungseinheit automatisch zu einer bestimmten Tageszeit Herunterfahren können.
Das Cmdlet gibt zurück, ob der Status der Richtlinie aktiviert ist, und die Tageszeit, die Sie festgelegt haben, um die virtuellen Lab-Computer automatisch herunterzufahren.

## Beispiele

## Parameter

### -LabName
Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für das automatische Herunterfahren erhält.

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
Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit heruntergefahren werden müssen.

## Notizen

## Verwandte Links

[Satz-AzureRmDtlAutoShutdownPolicy](./Set-AzureRmDtlAutoShutdownPolicy.md)


