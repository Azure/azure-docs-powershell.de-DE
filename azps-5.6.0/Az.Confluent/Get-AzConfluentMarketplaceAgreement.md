---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948915"
---
# <span data-ttu-id="e8dbe-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="e8dbe-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="e8dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dbe-103">Listen Sie im Abonnement Confluent-Marketplace-Vereinbarungen auf.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="e8dbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8dbe-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8dbe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dbe-106">Listen Sie im Abonnement Confluent-Marketplace-Vereinbarungen auf.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="e8dbe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="e8dbe-108">Beispiel 1: Auflisten aller konfluenten Marketplace-Vereinbarung unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e8dbe-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="e8dbe-109">Mit diesem Befehl werden alle kongenenten Marketplace-Vereinbarung unter einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="e8dbe-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8dbe-110">PARAMETERS</span></span>

### <span data-ttu-id="e8dbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8dbe-111">-DefaultProfile</span></span>
<span data-ttu-id="e8dbe-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8dbe-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8dbe-113">-SubscriptionId</span></span>
<span data-ttu-id="e8dbe-114">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="e8dbe-114">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="e8dbe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dbe-115">CommonParameters</span></span>
<span data-ttu-id="e8dbe-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8dbe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dbe-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8dbe-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dbe-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8dbe-118">INPUTS</span></span>

## <span data-ttu-id="e8dbe-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8dbe-119">OUTPUTS</span></span>

### <span data-ttu-id="e8dbe-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="e8dbe-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="e8dbe-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8dbe-121">NOTES</span></span>

<span data-ttu-id="e8dbe-122">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e8dbe-122">ALIASES</span></span>

## <span data-ttu-id="e8dbe-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8dbe-123">RELATED LINKS</span></span>

