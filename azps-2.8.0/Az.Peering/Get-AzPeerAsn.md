---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824051"
---
# Get-AzPeerAsn

## Synopsis
Ruft PeerAsn-Objekt aus dem Arm ab.

## Syntax

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft den PeerAsn für ein Abonnement ab.

## Beispiele

### Beispiel 1
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

Ruft die PeerAsn

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
Der eindeutige Name des PSPeering.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn

## Notizen

## Verwandte Links
