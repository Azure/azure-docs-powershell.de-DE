---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169608"
---
# Set-AzVpnClientIpsecParameter

## SYNOPSIS
Legt die Vpn-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.

## SYNTAX

### ByFactoryName (Standard)
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzVpnClientIpsecParameter"** legt die vpn-ipsec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.
Beim Erstellen des virtuellen Netzwerkgateways werden die Standardmäßigen Vpn-IPSec-Richtlinien für das Gateway festgelegt. Für den Fall, dass der Benutzer von "Verweisen auf" bestimmte benutzerdefinierte Ipsec-Richtlinien zum Herstellen einer Verbindung mit dem VPN-Gateway verwenden möchte, muss der Benutzer diese "ipsec"-Richtlinie zuerst auf dem VPN-Gateway festlegen. **Set-AzVpnClientIpsecParameter** bietet eine Möglichkeit dazu.

## BEISPIELE

### Beispiel 1: Legt eine benutzerdefinierte Vpn-Ipsec-Richtlinie auf ein vorhandenes virtuelles Netzwerkgateway fest.
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

In diesem Beispiel wird die benutzerdefinierte Vpn-Ipsec-Richtlinie aus der Ressourcengruppe "ContosoResourceGroup" auf das vorhandene virtuelle Netzwerkgateway namens "ContosoVirtualGateway" definiert.
New-AzVpnClientIpsecParameter cmdlet wird verwendet, um das Vpn-IPSec-Parameterobjekt zu erstellen, in dem die übergebenen Werte eines oder aller Parameter verwendet werden, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in ResourceGroup festlegen kann.
Dieses erstellte "VpnClientIPsecParameters"-Objekt wird an den Befehl Set-AzVpnClientIpsecParameter übergeben, um die angegebene benutzerdefinierte Vpn-Ipsec-Richtlinie für das virtuelle Netzwerkgateway wie im obigen Beispiel gezeigt zu festlegen. Dieser Befehl gibt das Objekt "VpnClientIPsecParameters" zurück, das die festgelegten Parameter angibt.

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

### -InputObject
Das Objekt des virtuellen Netzwerkgateways

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Die Azure-Ressourcen-ID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Der Name des virtuellen Netzwerkgateways.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VpnClientIPsecParameter
Ipsec-Parameter des Vpn-Clients. Dieser Parameterwert kann mithilfe des Befehls "PS" let:New-AzVpnClientIpsecParameter erstellt werden.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVpnClientIpsecParameter](./Get-AzVpnClientIpsecParameter.md)

[New-AzVpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)
