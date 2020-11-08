---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009005"
---
# <span data-ttu-id="fe294-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fe294-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="fe294-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe294-102">SYNOPSIS</span></span>
<span data-ttu-id="fe294-103">Ruft PeerAsn-Objekt aus dem Arm ab.</span><span class="sxs-lookup"><span data-stu-id="fe294-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="fe294-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe294-104">SYNTAX</span></span>

### <span data-ttu-id="fe294-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe294-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe294-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe294-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe294-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe294-107">DESCRIPTION</span></span>
<span data-ttu-id="fe294-108">Ruft den PeerAsn für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fe294-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="fe294-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe294-109">EXAMPLES</span></span>

### <span data-ttu-id="fe294-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe294-110">Example 1</span></span>
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

<span data-ttu-id="fe294-111">Ruft die PeerAsn</span><span class="sxs-lookup"><span data-stu-id="fe294-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="fe294-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe294-112">PARAMETERS</span></span>

### <span data-ttu-id="fe294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe294-113">-DefaultProfile</span></span>
<span data-ttu-id="fe294-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe294-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe294-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fe294-115">-Name</span></span>
<span data-ttu-id="fe294-116">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fe294-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="fe294-117">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fe294-117">-ResourceId</span></span>
<span data-ttu-id="fe294-118">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fe294-118">The resource id string name.</span></span>

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

### <span data-ttu-id="fe294-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe294-119">CommonParameters</span></span>
<span data-ttu-id="fe294-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe294-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe294-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe294-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe294-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe294-122">INPUTS</span></span>

### <span data-ttu-id="fe294-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fe294-123">System.String</span></span>

## <span data-ttu-id="fe294-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe294-124">OUTPUTS</span></span>

### <span data-ttu-id="fe294-125">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fe294-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="fe294-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe294-126">NOTES</span></span>

## <span data-ttu-id="fe294-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe294-127">RELATED LINKS</span></span>
