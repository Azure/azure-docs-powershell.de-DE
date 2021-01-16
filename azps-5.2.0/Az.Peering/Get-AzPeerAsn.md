---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300144"
---
# <span data-ttu-id="d16ca-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d16ca-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="d16ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d16ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d16ca-103">Ruft das "PeerAsn"-Objekt aus ARM.</span><span class="sxs-lookup"><span data-stu-id="d16ca-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="d16ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d16ca-104">SYNTAX</span></span>

### <span data-ttu-id="d16ca-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d16ca-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d16ca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d16ca-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d16ca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d16ca-107">DESCRIPTION</span></span>
<span data-ttu-id="d16ca-108">Ruft den PeerAsn für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d16ca-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="d16ca-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d16ca-109">EXAMPLES</span></span>

### <span data-ttu-id="d16ca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d16ca-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="d16ca-111">Ruft peerAsn ab</span><span class="sxs-lookup"><span data-stu-id="d16ca-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="d16ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d16ca-112">PARAMETERS</span></span>

### <span data-ttu-id="d16ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16ca-113">-DefaultProfile</span></span>
<span data-ttu-id="d16ca-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d16ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d16ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d16ca-115">-Name</span></span>
<span data-ttu-id="d16ca-116">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d16ca-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16ca-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16ca-117">-ResourceId</span></span>
<span data-ttu-id="d16ca-118">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d16ca-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16ca-119">CommonParameters</span></span>
<span data-ttu-id="d16ca-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16ca-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d16ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16ca-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d16ca-122">INPUTS</span></span>

### <span data-ttu-id="d16ca-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d16ca-123">System.String</span></span>

## <span data-ttu-id="d16ca-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d16ca-124">OUTPUTS</span></span>

### <span data-ttu-id="d16ca-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d16ca-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="d16ca-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d16ca-126">NOTES</span></span>

## <span data-ttu-id="d16ca-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d16ca-127">RELATED LINKS</span></span>
