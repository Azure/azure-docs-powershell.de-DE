---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: 9f33eef5b9f0bd0b245c444cf869fa0ff7a0a064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928355"
---
# <span data-ttu-id="178e9-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="178e9-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="178e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178e9-102">SYNOPSIS</span></span>
<span data-ttu-id="178e9-103">Listet die Skus des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="178e9-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="178e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="178e9-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="178e9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178e9-105">DESCRIPTION</span></span>
<span data-ttu-id="178e9-106">Listet die Skus des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="178e9-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="178e9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="178e9-107">EXAMPLES</span></span>

### <span data-ttu-id="178e9-108">Beispiel 1: Listen-SKU für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="178e9-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="178e9-109">Mit diesem Befehl wird die SKU für ein Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="178e9-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="178e9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="178e9-110">PARAMETERS</span></span>

### <span data-ttu-id="178e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178e9-111">-DefaultProfile</span></span>
<span data-ttu-id="178e9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="178e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="178e9-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="178e9-113">-SubscriptionId</span></span>
<span data-ttu-id="178e9-114">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="178e9-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="178e9-115">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="178e9-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="178e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178e9-116">CommonParameters</span></span>
<span data-ttu-id="178e9-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178e9-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="178e9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178e9-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="178e9-119">INPUTS</span></span>

## <span data-ttu-id="178e9-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="178e9-120">OUTPUTS</span></span>

### <span data-ttu-id="178e9-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="178e9-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="178e9-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="178e9-122">NOTES</span></span>

<span data-ttu-id="178e9-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="178e9-123">ALIASES</span></span>

## <span data-ttu-id="178e9-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="178e9-124">RELATED LINKS</span></span>

