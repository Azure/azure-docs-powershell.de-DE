---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660451"
---
# New-AzVpnClientIpsecPolicy

## Synopsis
Mit diesem Befehl können die Benutzer das VPN-IPSec-Richtlinienobjekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die auf dem VPN-Gateway festgelegt werden sollen. Dieser Befehl Let Output-Objekt wird verwendet, um die VPN-IPSec-Richtlinie für das neue/exisitng-Gateway einzurichten.

## Syntax

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit diesem Befehl können die Benutzer das VPN-IPSec-Richtlinienobjekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die auf dem VPN-Gateway festgelegt werden sollen. Dieser Befehl Let Output-Objekt wird verwendet, um die VPN-IPSec-Richtlinie für das neue/exisitng-Gateway einzurichten.

## Beispiele

### Definieren Sie das VPN-IPSec-Richtlinienobjekt:
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Dieses Cmdlet wird verwendet, um das VPN-IPSec-Richtlinienobjekt zu erstellen, wobei die Werte für einen oder alle Parameter übergeben werden, die der Benutzer an param: VpnClientIpsecPolicy des PS-Befehls Let: New-AzVirtualNetworkGateway (neue VPN-Gateway-Erstellung)/Set-AzVirtualNetworkGateway (vorhandenes VPN-Gateway-Update) in ResourceGroup übergeben kann:

### Erstellen eines neuen virtuellen Netzwerkgateways mit dem Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie:
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt nach der Erstellung ein virtuelles Netzwerkgateway-Objekt zurück. 

### Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie auf einem vorhandenen virtuellen Netzwerkgateway:
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Dieses Cmdlet gibt nach dem Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie virtuelles Netzwerkgateway-Objekt zurück.

### Abrufen des virtuellen Netzwerkgateways, um zu sehen, ob die benutzerdefinierte VPN-Richtlinie richtig festgesetzt ist:
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Dieses Cmdlet gibt virtuelles Netzwerkgateway-Objekt zurück.

## Parameter

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

### -DhGroup
Die vpnclient-DH-Gruppen, die in der IKE-Phase 1 für Initial SA verwendet werden

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
Der vpnclient-IKE-Verschlüsselungsalgorithmus (IKE-Phase 2)

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
Der vpnclient-IKE-Integritätsalgorithmus (IKE-Phase 2)

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
Der vpnclient IPSec-Verschlüsselungsalgorithmus (IKE-Phase 1)

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
Der vpnclient-IPSec-Integritätsalgorithmus (IKE-Phase 1)

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
Die vpnclient-PFS-Gruppen, die in IKE Phase 2 für neue untergeordnete SA verwendet werden

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
Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Nutzlast-Größe in KB

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
Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Lebensdauer in Sekunden

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy

## Notizen

## Verwandte Links
