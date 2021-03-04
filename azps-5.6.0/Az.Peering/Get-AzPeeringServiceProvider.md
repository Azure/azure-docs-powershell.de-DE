---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937712"
---
# <span data-ttu-id="67429-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="67429-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="67429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67429-102">SYNOPSIS</span></span>
<span data-ttu-id="67429-103">Ruft eine Liste der Peeringdienstanbieter ab, die mit Microsoft zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="67429-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="67429-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67429-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67429-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67429-105">DESCRIPTION</span></span>
<span data-ttu-id="67429-106">Listen-Peering-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="67429-106">List peering service providers</span></span>

## <span data-ttu-id="67429-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67429-107">EXAMPLES</span></span>

### <span data-ttu-id="67429-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67429-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="67429-109">Ruft verfügbare Peeringdienstanbieter ab</span><span class="sxs-lookup"><span data-stu-id="67429-109">Gets available peering service providers</span></span>

## <span data-ttu-id="67429-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="67429-110">PARAMETERS</span></span>

### <span data-ttu-id="67429-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67429-111">-DefaultProfile</span></span>
<span data-ttu-id="67429-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67429-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67429-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67429-113">CommonParameters</span></span>
<span data-ttu-id="67429-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67429-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67429-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67429-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67429-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67429-116">INPUTS</span></span>

### <span data-ttu-id="67429-117">Keine</span><span class="sxs-lookup"><span data-stu-id="67429-117">None</span></span>

## <span data-ttu-id="67429-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67429-118">OUTPUTS</span></span>

### <span data-ttu-id="67429-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="67429-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="67429-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="67429-120">NOTES</span></span>

## <span data-ttu-id="67429-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="67429-121">RELATED LINKS</span></span>
