---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933840"
---
# Add-AzNetworkInterfaceTapConfig

## SYNOPSIS
Erstellt eine TapConfiguration-Ressource, die einem NetworkInterface zugeordnet ist. Dadurch wird auf eine vorhandene VirtualNetworkTap-Ressource verwiesen.

## SYNTAX

### SetByResource (Standard)
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzNetworkInterfaceTapConfig-Cmdlet** erstellt eine TapConfiguration-Ressource, die einem NetworkInterface zugeordnet ist. Dadurch wird auf eine vorhandene VirtualNetworkTap-Ressource verwiesen.

## BEISPIELE

### Beispiel 1: Hinzufügen von TapConfiguration zu einem bestimmten NetworkInterface
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

Fügen Sie die TapConfiguration zu einer sourceNic hinzu. Der Datenverkehr von sourceNic VM wird an die Ziel-VM gespiegelt, auf die in der vVirtualNetworkTap-Ressource verwiesen wird.

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

### -Name
Name der Tippkonfiguration.

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

### -NetworkInterface
Der Verweis auf die Netzwerkschnittstellenressource.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkTap
Der Verweis auf die Ressource für das Tippen auf das virtuelle Netzwerk.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkTapId
Der Verweis auf die Ressource für das Tippen auf das virtuelle Netzwerk.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

### System.String

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNetworkInterfaceTapConfig](./Get-AzNetworkInterfaceTapConfig.md)

[Remove-AzNetworkInterfaceTapConfig](./Remove-AzNetworkInterfaceTapConfig.md)

[Set-AzNetworkInterfaceTapConfig](./Set-AzNetworkInterfaceTapConfig.md)
