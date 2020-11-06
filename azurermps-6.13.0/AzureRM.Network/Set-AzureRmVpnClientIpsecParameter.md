---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498289"
---
# Set-AzureRmVpnClientIpsecParameter

## Synopsis
Legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmVpnClientIpsecParameter** " legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.
Wenn virtuelles Netzwerkgateway erstellt wird, legt es den Satz von Standard-VPN-IPSec-Richtlinien auf dem Gateway fest. Zeigen Sie auf Websitebenutzer möchte bestimmte benutzerdefinierte IPSec-Richtlinien zum Herstellen einer Verbindung mit dem VPN-Gateway verwenden, muss der Benutzer diese IPSec-Richtlinie zuerst auf dem VPN-Gateway festlegen. **AzureRmVpnClientIpsecParameter** bietet eine Möglichkeit, dies zu tun.

## Beispiele

### Beispiel 1: legt eine benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway fest.
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

In diesem Beispiel wird die benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway mit dem Namen ContosoVirtualGateway aus der Ressourcengruppe namens ContosoResourceGroup festgelegt.
New-AzureRmVpnClientIpsecParameter-Cmdlet wird zum Erstellen des VPN-IPSec-Parameters-Objekts verwendet, das die Werte der übergebenen oder aller Parameter verwendet, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in der ResourceGroup einrichten kann.
Dieses erstellte VpnClientIPsecParameters-Objekt wird an Set-AzureRmVpnClientIpsecParameter Befehl übergeben, um die angegebene VPN-IPSec-benutzerdefinierte Richtlinie auf dem virtuellen Netzwerkgateway festzulegen, wie in obigem Beispiel gezeigt. Dieser Befehl gibt das VpnClientIPsecParameters-Objekt zurück, das die Parameter für "Menge" anzeigt.

## Parameter

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

### -Inputobject
Das virtuelle Netzwerk-Gateaway-Objekt

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

### -Resourcen-Nr
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
IPSec-Parameter für VPN-Client. Dieser Parameterwert kann mithilfe von PS Befehl Let: neu-AzureRmVpnClientIpsecParameter erstellt werden.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters
Parameter: VpnClientIPsecParameter (ByValue)

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Parameter: Inputobject (ByValue)

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters

## Notizen

## Verwandte Links

[Neu – AzureRmVpnClientIpsecParameters](./New-AzureRmVpnClientIpsecParameters.md)
