---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151820"
---
# Get-AzVirtualRouterPeerLearnedRoute

## SYNOPSIS
Liste der von einem bestimmten virtuellen Router peer erlernten Routen

## SYNTAX

### VirtualRouterPeerNameParameterSet (Standard)
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VirtualRouterPeerObjectParameterSet
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Aufzählen der von einem virtuellen Router peer aus anderen Quellen erlernten Routen.

## BEISPIELE

### Beispiel 1
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### Beispiel 2
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Das Eingabeobjekt des virtuellen Router-Peers.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PeerName
Name des Peers des virtuellen Routers

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Virtuellen Router-Peer-Ressourcengruppe

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualRouterName
Name des virtuellen Routers

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPeerRoute

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
