---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154484"
---
# Get-AzApplicationGatewaySslCertificate

## SYNOPSIS
Ruft ein -SSL-Zertifikat für ein Anwendungsgateway ab.

## SYNTAX

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzApplicationGatewaySslCertificate"** ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.

## BEISPIELE

### Beispiel 1: Erhalten eines bestimmten Zertifikats
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.
Der zweite Befehl ruft das #A0 namens Cert01 vom Anwendungsgateway ab, das in der Variablen namens "$AppGW.
Der Befehl speichert das Zertifikat in der Variablen namens $Cert.

### Beispiel 2: Erhalten einer Liste von SSL-Zertifikaten
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.
Dieser zweite Befehl ruft eine Liste der SSL-Zertifikate vom Anwendungsgateway ab, das in der Variablen namens "$AppGW" gespeichert $AppGW.
Der Befehl speichert dann die Ergebnisse in der Variablen namens $Certs.

## PARAMETERS

### -ApplicationGateway
Gibt das Anwendungsgatewayobjekt an, das das SSL-Zertifikat enthält.

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
Gibt den Namen des SSL-Zertifikatpools an, den dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApplicationGatewaySslCertificate](./Add-AzApplicationGatewaySslCertificate.md)

[New-AzApplicationGatewaySslCertificate](./New-AzApplicationGatewaySslCertificate.md)

[Remove-AzApplicationGatewaySslCertificate](./Remove-AzApplicationGatewaySslCertificate.md)

[Set-AzApplicationGatewaySslCertificate](./Set-AzApplicationGatewaySslCertificate.md)


