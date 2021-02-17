---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169513"
---
# <span data-ttu-id="3a261-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3a261-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="3a261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a261-102">SYNOPSIS</span></span>
<span data-ttu-id="3a261-103">Ruft eine Liste der Peeringdienstanbieter ab, die mit Microsoft zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a261-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="3a261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a261-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a261-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a261-105">DESCRIPTION</span></span>
<span data-ttu-id="3a261-106">Listen-Peering-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3a261-106">List peering service providers</span></span>

## <span data-ttu-id="3a261-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a261-107">EXAMPLES</span></span>

### <span data-ttu-id="3a261-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a261-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="3a261-109">Ruft verfügbare Peeringdienstanbieter ab</span><span class="sxs-lookup"><span data-stu-id="3a261-109">Gets available peering service providers</span></span>

## <span data-ttu-id="3a261-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a261-110">PARAMETERS</span></span>

### <span data-ttu-id="3a261-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a261-111">-DefaultProfile</span></span>
<span data-ttu-id="3a261-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a261-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a261-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a261-113">CommonParameters</span></span>
<span data-ttu-id="3a261-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a261-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a261-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a261-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a261-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a261-116">INPUTS</span></span>

### <span data-ttu-id="3a261-117">Keine</span><span class="sxs-lookup"><span data-stu-id="3a261-117">None</span></span>

## <span data-ttu-id="3a261-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a261-118">OUTPUTS</span></span>

### <span data-ttu-id="3a261-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3a261-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="3a261-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a261-120">NOTES</span></span>

## <span data-ttu-id="3a261-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a261-121">RELATED LINKS</span></span>
