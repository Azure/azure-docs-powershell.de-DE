---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924672"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Mit diesem Befehl können die Benutzer das Vpn ipsec-Richtlinienobjekt erstellen, das einen oder alle Werte wie IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup für das VPN-Gateway anfordert. Mit diesem Befehl können Ausgabeobjekt verwendet werden, um die VPN-IPSec-Richtlinie für das neue /vorhandene Gateway zu legen.

## SYNTAX

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Mit diesem Befehl können die Benutzer das Vpn ipsec-Richtlinienobjekt erstellen, das einen oder alle Werte wie IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup für das VPN-Gateway anfordert. Mit diesem Befehl können Ausgabeobjekt verwendet werden, um die VPN-IPSec-Richtlinie für das neue /vorhandene Gateway zu legen.

## BEISPIELE

### Beispiel 1: Definieren des Vpn-Ipsec-Richtlinienobjekts:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Dieses Cmdlet wird verwendet, um das vpn ipsec-Richtlinienobjekt mit den übergebenen Werten eines oder aller Parameter zu erstellen, die der Benutzer an param:VpnClientIpsecPolicy of PS übergeben kann: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :

### Beispiel 2: Erstellen eines neuen virtuellen Netzwerkgateways mit dem Festlegen einer benutzerdefinierten Vpn-IPSec-Richtlinie:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt das Objekt des virtuellen Netzwerkgateways nach der Erstellung zurück. 

### Beispiel 3: Festlegen der benutzerdefinierten Vpn-IPSec-Richtlinie für vorhandenes Gateway für virtuelle Netzwerke:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt virtuelles Netzwerkgatewayobjekt zurück, nachdem eine benutzerdefinierte Vpn-IPSec-Richtlinie konfiguriert wurde.

### Beispiel 4: Holen Sie sich das Gateway für virtuelles Netzwerk, um zu sehen, ob die benutzerdefinierte Vpn-Richtlinie richtig festgelegt ist:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Dieses Cmdlet gibt virtuelles Netzwerkgatewayobjekt zurück.

## PARAMETER

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
Die vpnClient-DH-Gruppen, die in IKE Phase 1 für die erste SA verwendet werden

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
VpnClient-IKE-Verschlüsselungsalgorithmus (IKE Phase 2)

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
VpnClient-IPSec-Verschlüsselungsalgorithmus (IKE Phase 1)

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
Die vpnClient-PFS-Gruppen, die in IKE Phase 2 für neue untergeordnete SA verwendet werden

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
Die Nutzlastgröße der VpnClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in KB

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
Die Lebensdauer der VpnClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in Sekunden

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## NOTIZEN

## VERWANDTE LINKS
