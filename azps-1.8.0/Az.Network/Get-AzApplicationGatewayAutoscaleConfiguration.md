---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 723d1aaab342673f16d37cfaa15406f3ab99566d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660881"
---
# Get-AzApplicationGatewayAutoscaleConfiguration

## Synopsis
Ruft die AutoScale-Konfiguration des Anwendungs Gateways ab.

## Syntax

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzApplicationGatewayAutoscaleConfiguration** " Ruft die Konfiguration des Anwendungs Gateways mit einer AutoScale-Konfiguration ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $GW Variablen.
Der zweite Befehl extrahiert die AutoScale-Konfiguration vom applicationg-Gateway.

## Parameter

### -ApplicationGateway
Die applicationGateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration

## Notizen

## Verwandte Links

[Neu – AzApplicationGatewayAutoscaleConfiguration](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[Remove-AzApplicationGatewayAutoscaleConfiguration](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[Satz-AzApplicationGatewayAutoscaleConfiguration](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
