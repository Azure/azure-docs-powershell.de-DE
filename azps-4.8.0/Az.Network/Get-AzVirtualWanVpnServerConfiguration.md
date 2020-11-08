---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009123"
---
# Get-AzVirtualWanVpnServerConfiguration

## Synopsis
Ruft die Liste aller VpnServerConfigurations ab, die diesem VirtualWan zugeordnet sind.

## Syntax

### ByVirtualWanName (Standard)
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByVirtualWanObject
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByVirtualWanResourceId
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzVirtualWanVpnServerConfiguration** " gibt die Liste aller VpnServerConfigurations zurück, die diesem VirtualWan zugeordnet sind. dh alle VpnServerConfigurations, die mit einem P2SVpnGateways unter VirutalHubs dieser VirtualWan verbunden sind.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

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

### -Name
Der Ressourcenname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
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

### -Resourcen-Nr
Die Azure-Ressourcen-ID für das virtuelle WAN.

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualWanObject
Das virtuelle WAN-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
Microsoft. Azure. Commands. Network. Models. PSVirtualWan

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse

## Notizen

## Verwandte Links
