---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 871a06a2bbd3a844dd758dbc16189afdb261db2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004171"
---
# Remove-AzVirtualRouterPeer

## Synopsis
Entfernt einen Peer aus einem Azure VirtualRouter

## Syntax

### VirtualRouterPeerNameParameterSet (Standard)
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VirtualRouterPeerObjectParameterSet
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### VirtualRouterPeerResourceIdParameterSet
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Remove-AzVirtualRouterPeer** " entfernt einen VirtualRouter-Peer aus einem Azure-VirtualRouter

## Beispiele

### Beispiel 1
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### Beispiel 2
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### Beispiel 3
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Force
Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Das Peer Eingabeobjekt für einen virtuellen Router.

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PeerName
Der Name des virtuellen Router-Peers.

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe des virtuellen Routers/Peers.

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Peer Ressourcen-ID des virtuellen Routers.

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualRouterName
Der virtuelle Router, auf dem Peer vorhanden ist.

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualRouter

## Notizen

## Verwandte Links
