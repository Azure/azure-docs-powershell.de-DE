---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005323"
---
# <span data-ttu-id="d97fa-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="d97fa-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="d97fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d97fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d97fa-103">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="d97fa-103">Get the offer metrics.</span></span>

## <span data-ttu-id="d97fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d97fa-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d97fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d97fa-105">DESCRIPTION</span></span>
<span data-ttu-id="d97fa-106">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="d97fa-106">Get the offer metrics.</span></span>

## <span data-ttu-id="d97fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d97fa-107">EXAMPLES</span></span>

### <span data-ttu-id="d97fa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d97fa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="d97fa-109">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="d97fa-109">Get the offer metrics.</span></span>

## <span data-ttu-id="d97fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d97fa-110">PARAMETERS</span></span>

### <span data-ttu-id="d97fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97fa-111">-DefaultProfile</span></span>
<span data-ttu-id="d97fa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d97fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97fa-113">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="d97fa-113">-OfferName</span></span>
<span data-ttu-id="d97fa-114">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="d97fa-114">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d97fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="d97fa-116">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d97fa-116">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d97fa-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d97fa-117">-SubscriptionId</span></span>
<span data-ttu-id="d97fa-118">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d97fa-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d97fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97fa-119">CommonParameters</span></span>
<span data-ttu-id="d97fa-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97fa-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d97fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97fa-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d97fa-122">INPUTS</span></span>

## <span data-ttu-id="d97fa-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d97fa-123">OUTPUTS</span></span>

### <span data-ttu-id="d97fa-124">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="d97fa-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="d97fa-125">Aliase</span><span class="sxs-lookup"><span data-stu-id="d97fa-125">ALIASES</span></span>

## <span data-ttu-id="d97fa-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d97fa-126">NOTES</span></span>

## <span data-ttu-id="d97fa-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d97fa-127">RELATED LINKS</span></span>

