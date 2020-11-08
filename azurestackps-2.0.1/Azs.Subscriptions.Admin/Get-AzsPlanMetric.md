---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005407"
---
# <span data-ttu-id="db216-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="db216-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="db216-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db216-102">SYNOPSIS</span></span>
<span data-ttu-id="db216-103">Abrufen der Metriken des angegebenen Plans</span><span class="sxs-lookup"><span data-stu-id="db216-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="db216-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db216-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="db216-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db216-105">DESCRIPTION</span></span>
<span data-ttu-id="db216-106">Abrufen der Metriken des angegebenen Plans</span><span class="sxs-lookup"><span data-stu-id="db216-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="db216-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db216-107">EXAMPLES</span></span>

### <span data-ttu-id="db216-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db216-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="db216-109">Besorgen Sie sich die Metriken eines Plans.</span><span class="sxs-lookup"><span data-stu-id="db216-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="db216-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db216-110">PARAMETERS</span></span>

### <span data-ttu-id="db216-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db216-111">-DefaultProfile</span></span>
<span data-ttu-id="db216-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db216-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db216-113">-Planname</span><span class="sxs-lookup"><span data-stu-id="db216-113">-PlanName</span></span>
<span data-ttu-id="db216-114">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="db216-114">Name of the plan.</span></span>

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

### <span data-ttu-id="db216-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db216-115">-ResourceGroupName</span></span>
<span data-ttu-id="db216-116">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="db216-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="db216-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="db216-117">-SubscriptionId</span></span>
<span data-ttu-id="db216-118">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="db216-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db216-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db216-119">CommonParameters</span></span>
<span data-ttu-id="db216-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db216-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db216-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db216-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db216-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db216-122">INPUTS</span></span>

## <span data-ttu-id="db216-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db216-123">OUTPUTS</span></span>

### <span data-ttu-id="db216-124">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="db216-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="db216-125">Aliase</span><span class="sxs-lookup"><span data-stu-id="db216-125">ALIASES</span></span>

## <span data-ttu-id="db216-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="db216-126">NOTES</span></span>

## <span data-ttu-id="db216-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db216-127">RELATED LINKS</span></span>

