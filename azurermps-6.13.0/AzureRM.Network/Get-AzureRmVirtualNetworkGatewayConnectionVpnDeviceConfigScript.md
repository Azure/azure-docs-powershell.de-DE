---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: abaaaf7d9f430bd1b7850f3141b651ac02821257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479498"
---
# Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## Synopsis
Dieser Unifiedgroup übernimmt die Verbindungsressource, die Marke für das VPN-Gerät, das Modell, die Firmwareversion, und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf Ihren lokalen VPN-Geräten anwenden können. Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter wie öffentliche IP-Adressen des Azure-Gateways, virtuelle Netzwerk Adresspräfixe, VPN-Tunnel-vorinstallierter Schlüssel usw. ein, sodass Kunden einfach in Ihre VPN-Gerätekonfigurationen kopieren können.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Dieser Unifiedgroup übernimmt die Verbindungsressource, die Marke für das VPN-Gerät, das Modell, die Firmwareversion, und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf Ihren lokalen VPN-Geräten anwenden können. Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter wie öffentliche IP-Adressen des Azure-Gateways, virtuelle Netzwerk Adresspräfixe, VPN-Tunnel-vorinstallierter Schlüssel usw. ein, sodass Kunden einfach in Ihre VPN-Gerätekonfigurationen kopieren können.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

Im obigen Beispiel wird Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice verwendet, um die unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen abzurufen.
Verwendet dann eine der zurückgegebenen Modellinformationen, um ein VPN-Geräte Konfigurationsskript für das VirtualNetworkGatewayConnection "TestConnection" zu generieren. Das Gerät, das in diesem Beispiel verwendet wird, hat DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" und FirmwareVersion 20.

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

### -DeviceFamily
Name des VPN-Gerätemodells/-Familie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeviceVendor
Der Name des Anbieters für VPN-Geräte.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirmwareVersion
Firmware-Version des VPN-Geräts.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Ressourcenname der Verbindung, für die die Konfiguration generiert werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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

### System. String

## Ausgaben

### System. String

## Notizen

## Verwandte Links
