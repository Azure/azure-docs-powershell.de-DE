---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378956"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Dieser Befehl ermöglicht es den Benutzern, das Vpn-Ipsec-Richtlinienobjekt zu erstellen, das einen oder alle Werte wie "IpsecEncryption", "IpsecIntegrity", "IkeEncryption", "IkeIntegrity", "DhGroup", "PfsGroup" anfordert, die auf dem VPN-Gateway festgelegt werden. Mit diesem Befehl wird das Ausgabeobjekt verwendet, um die Vpn-IPSec-Richtlinie für das neue/vorhandene Gateway zu festlegen.

## SYNTAX

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Dieser Befehl ermöglicht es den Benutzern, das Vpn-Ipsec-Richtlinienobjekt zu erstellen, das einen oder alle Werte wie "IpsecEncryption", "IpsecIntegrity", "IkeEncryption", "IkeIntegrity", "DhGroup", "PfsGroup" anfordert, die auf dem VPN-Gateway festgelegt werden. Mit diesem Befehl wird das Ausgabeobjekt verwendet, um die Vpn-IPSec-Richtlinie für das neue/vorhandene Gateway zu festlegen.

## BEISPIELE

### Beispiel 1: Definieren des Vpn-Ipsec-Richtlinienobjekts:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Dieses Cmdlet wird verwendet, um das Vpn-IPSEC-Richtlinienobjekt mit den übergebenen Werten eines oder aller Parameter zu erstellen, die der Benutzer an "param:VpnClientIpsecPolicy" des Befehls "PS" übergeben kann: New-AzVirtualNetworkGateway (Erstellung eines neuen VPN-Gateways) / Set-AzVirtualNetworkGateway (vorhandenes VPN-Gatewayupdate) in ResourceGroup:

### Beispiel 2: Erstellen eines neuen virtuellen Netzwerkgateways mit dem Festlegen einer benutzerdefinierten Vpn-Ipsec-Richtlinie:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt nach der Erstellung ein objekt des virtuellen Netzwerkgateways zurück. 

### Beispiel 3: Festlegen einer benutzerdefinierten Vpn-Ipsec-Richtlinie für ein vorhandenes virtuelles Netzwerkgateway:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt nach dem Festlegen der benutzerdefinierten Vpn-Ipsec-Richtlinie ein virtuelles Netzwerkgatewayobjekt zurück.

### Beispiel 4: Holen Sie sich das virtuelle Netzwerkgateway, um zu sehen, ob die benutzerdefinierte Vpn-Richtlinie korrekt festgelegt ist:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Dieses Cmdlet gibt ein Objekt des virtuellen Netzwerkgateways zurück.

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

### -DhGroup
Die vpnClient -DH-Gruppen, die in IKE Phase 1 für den anfänglichen SA verwendet wurden

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
Der VpnClient-IKE-Verschlüsselungsalgorithmus (IKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
Der VpnClient-IKE-Integritätsalgorithmus (IKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
Der VpnClient-IPSec-Verschlüsselungsalgorithmus (IKE Phase 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
Der VpnClient-IPSec-Integritätsalgorithmus (IKE Phase 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
Die vpnClient-PFS-Gruppen, die in IKE Phase 2 für das neue untergeordnete SA verwendet werden

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
Die Nutzlastgröße der VPNClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in KB

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
Die Lebensdauer der VPNClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in Sekunden

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
