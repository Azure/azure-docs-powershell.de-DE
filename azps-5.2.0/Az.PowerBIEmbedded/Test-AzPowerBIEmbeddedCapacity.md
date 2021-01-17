---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363990"
---
# Test-AzPowerBIEmbeddedCapacity

## SYNOPSIS
Überprüft, ob es eine Instanz von eingebetteter PowerBI-Kapazität gibt.

## SYNTAX

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Test-AzPowerBIEmbeddedCapacity cmdlet testet das Vorhandensein einer Instanz der eingebetteten PowerBI-Kapazität.

## BEISPIELE

### Beispiel 1
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

Dieser Befehl testet, ob eine Kapazität mit dem Namen

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Name der eingebetteten PowerBI-Kapazität

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### System.Boolean

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPowerBIEmbedded1](./Get-AzPowerBIEmbeddedCapacity.md)

[Remove-AzPowerBIEmbedded1](./Remove-AzPowerBIEmbeddedCapacity.md)
