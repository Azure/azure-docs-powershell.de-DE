---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471060"
---
# <span data-ttu-id="3d420-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="3d420-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="3d420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d420-102">SYNOPSIS</span></span>
<span data-ttu-id="3d420-103">Listet die SKU des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="3d420-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="3d420-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d420-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3d420-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d420-105">DESCRIPTION</span></span>
<span data-ttu-id="3d420-106">Listet die SKU des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="3d420-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="3d420-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d420-107">EXAMPLES</span></span>

### <span data-ttu-id="3d420-108">Beispiel 1: Auflisten der SKU für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d420-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="3d420-109">Mit diesem Befehl wird die SKU für ein Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d420-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="3d420-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d420-110">PARAMETERS</span></span>

### <span data-ttu-id="3d420-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d420-111">-DefaultProfile</span></span>
<span data-ttu-id="3d420-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d420-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d420-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d420-113">-SubscriptionId</span></span>
<span data-ttu-id="3d420-114">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3d420-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d420-115">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="3d420-115">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d420-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d420-116">CommonParameters</span></span>
<span data-ttu-id="3d420-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d420-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d420-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d420-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d420-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d420-119">INPUTS</span></span>

## <span data-ttu-id="3d420-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d420-120">OUTPUTS</span></span>

### <span data-ttu-id="3d420-121">Microsoft.Azure.PowerShell.Cmdlets.Element.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="3d420-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="3d420-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d420-122">NOTES</span></span>

<span data-ttu-id="3d420-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3d420-123">ALIASES</span></span>

## <span data-ttu-id="3d420-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d420-124">RELATED LINKS</span></span>

