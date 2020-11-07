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
# <span data-ttu-id="50b87-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="50b87-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="50b87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50b87-102">SYNOPSIS</span></span>
<span data-ttu-id="50b87-103">Ruft PeerAsn-Objekt aus dem Arm ab.</span><span class="sxs-lookup"><span data-stu-id="50b87-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="50b87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50b87-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b87-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50b87-105">DESCRIPTION</span></span>
<span data-ttu-id="50b87-106">Ruft den PeerAsn für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="50b87-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="50b87-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50b87-107">EXAMPLES</span></span>

### <span data-ttu-id="50b87-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50b87-108">Example 1</span></span>
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

<span data-ttu-id="50b87-109">Ruft die PeerAsn</span><span class="sxs-lookup"><span data-stu-id="50b87-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="50b87-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50b87-110">PARAMETERS</span></span>

### <span data-ttu-id="50b87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b87-111">-DefaultProfile</span></span>
<span data-ttu-id="50b87-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50b87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50b87-113">-Name</span><span class="sxs-lookup"><span data-stu-id="50b87-113">-Name</span></span>
<span data-ttu-id="50b87-114">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="50b87-114">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="50b87-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b87-115">CommonParameters</span></span>
<span data-ttu-id="50b87-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b87-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b87-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50b87-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b87-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50b87-118">INPUTS</span></span>

### <span data-ttu-id="50b87-119">Keine</span><span class="sxs-lookup"><span data-stu-id="50b87-119">None</span></span>

## <span data-ttu-id="50b87-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50b87-120">OUTPUTS</span></span>

### <span data-ttu-id="50b87-121">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="50b87-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="50b87-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="50b87-122">NOTES</span></span>

## <span data-ttu-id="50b87-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50b87-123">RELATED LINKS</span></span>
