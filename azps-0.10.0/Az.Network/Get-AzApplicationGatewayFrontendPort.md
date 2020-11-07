---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841731"
---
# Get-AzApplicationGatewayFrontendPort

## Synopsis
Ruft den Front-End-Port eines Anwendungs Gateways ab.

## Syntax

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzApplicationGatewayFrontendPort** wird der Front-End-Port eines Anwendungs Gateways abgerufen.

## Beispiele

### Beispiel 1: Abrufen eines angegebenen Front-End-Ports
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.
Der zweite Befehl ruft den Front-End-Port mit dem Namen FrontEndPort01 aus $AppGw ab und speichert ihn in der $FrontEndPort-Variablen.

### Beispiel 2: Abrufen einer Liste der Front-End-Ports
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.
Der zweite Befehl ruft eine Liste der Front-End-Ports von $AppGw ab und speichert Sie in der $FrontEndPorts-Variablen.

## Parameter

### -ApplicationGateway
Gibt das Application Gateway-Objekt an, das den Front-End-Port enthält.

```yaml
Type: PSApplicationGateway
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des abzurufenden Front-End-Ports an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayFrontendPort](./Add-AzApplicationGatewayFrontendPort.md)

[Neu – AzApplicationGatewayFrontendPort](./New-AzApplicationGatewayFrontendPort.md)

[Remove-AzApplicationGatewayFrontendPort](./Remove-AzApplicationGatewayFrontendPort.md)

[Satz-AzApplicationGatewayFrontendPort](./Set-AzApplicationGatewayFrontendPort.md)


