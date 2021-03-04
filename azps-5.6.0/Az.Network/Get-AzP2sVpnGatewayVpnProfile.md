---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: e606f961cf54eb390e76e3f9bc8c00e556aff7fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919736"
---
# Get-AzP2sVpnGatewayVpnProfile

## SYNOPSIS
Generiert und gibt eine SAS-URL zurück, die der Kunde zum Herunterladen des Vpn-Profils für das Einrichten des Point-to-Websiteclients verwendet, um auf die Websitekonnektivität mit P2SVpnGateway verweisen zu können.

## SYNTAX

### ByP2SVpnGatewayName (Standard)
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByP2SVpnGatewayObject
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByP2SVpnGatewayResourceId
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzP2sVpnGatewayVpnProfile-Cmdlet** ermöglicht es Ihnen, eine SAS-URL für Kunden zu generieren und zu erhalten, um das Vpn-Profil für das Einrichten des Punkt-zu-Website-Clients herunterzuladen, um auf die Websitekonnektivität mit P2SVpnGateway zu verweisen. Verweisen Sie auf die Websiteclienteinrichtung, die dieses Vpn-Profil verwendet, um nur eine Verbindung mit diesem bestimmten P2SVpnGateway herzustellen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

Das **Get-AzP2sVpnGatewayVpnProfile-Cmdlet** ermöglicht es Ihnen, eine SAS-URL für Kunden zu generieren und zu erhalten, um das Vpn-Profil für das Einrichten des Punkt-zu-Website-Clients herunterzuladen, um auf die Websitekonnektivität mit P2SVpnGateway zu verweisen. ProfileUrl zeigt die SAS-URL an, von der der Kunde das Vpn-Profil für die Einrichtung von Punkt auf Websiteclient herunterladen kann.

## PARAMETER

### -AuthenticationMethod
Authentifizierungsmethode

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Das zu ändernde p2s-Vpn-Gatewayobjekt

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Ressourcenname.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateways.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String
Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse

## NOTIZEN

## VERWANDTE LINKS
