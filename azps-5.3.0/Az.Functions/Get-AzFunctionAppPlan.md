---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458592"
---
# <span data-ttu-id="25afa-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="25afa-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="25afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25afa-102">SYNOPSIS</span></span>
<span data-ttu-id="25afa-103">Holen Sie sich Funktions-Apps-Pläne in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25afa-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="25afa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25afa-104">SYNTAX</span></span>

### <span data-ttu-id="25afa-105">GetAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="25afa-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="25afa-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="25afa-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="25afa-107">ByName</span><span class="sxs-lookup"><span data-stu-id="25afa-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="25afa-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25afa-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="25afa-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25afa-109">DESCRIPTION</span></span>
<span data-ttu-id="25afa-110">Holen Sie sich Funktions-Apps-Pläne in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25afa-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="25afa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25afa-111">EXAMPLES</span></span>

### <span data-ttu-id="25afa-112">Beispiel 1: Alle Funktions-App-Pläne erhalten.</span><span class="sxs-lookup"><span data-stu-id="25afa-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="25afa-113">Dieser Befehl ruft alle Funktions-App-Pläne ab.</span><span class="sxs-lookup"><span data-stu-id="25afa-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="25afa-114">Beispiel 2: Erhalten von Funktions-App-Plänen nach dem Namen der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25afa-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="25afa-115">Mit diesem Befehl werden Funktions-App-Pläne nach Dem Namen der Ressourcengruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25afa-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="25afa-116">Beispiel 3: Erhalten von Funktions-App-Plänen für die angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="25afa-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="25afa-117">Dieser Befehl ruft Funktions-App-Pläne für die angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="25afa-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="25afa-118">Beispiel 4: Erhalten von Funktions-App-Plänen nach Ort.</span><span class="sxs-lookup"><span data-stu-id="25afa-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="25afa-119">Dieser Befehl ruft Funktions-App-Pläne nach Ort ab.</span><span class="sxs-lookup"><span data-stu-id="25afa-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="25afa-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25afa-120">PARAMETERS</span></span>

### <span data-ttu-id="25afa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25afa-121">-DefaultProfile</span></span>
<span data-ttu-id="25afa-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25afa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25afa-123">-Location</span><span class="sxs-lookup"><span data-stu-id="25afa-123">-Location</span></span>
<span data-ttu-id="25afa-124">Die Position des Funktions-App-Plans.</span><span class="sxs-lookup"><span data-stu-id="25afa-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="25afa-125">-Name</span></span>
<span data-ttu-id="25afa-126">Der Name des Serviceplans.</span><span class="sxs-lookup"><span data-stu-id="25afa-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25afa-127">-ResourceGroupName</span></span>
<span data-ttu-id="25afa-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25afa-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25afa-129">-SubscriptionId</span></span>
<span data-ttu-id="25afa-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="25afa-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="25afa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25afa-131">CommonParameters</span></span>
<span data-ttu-id="25afa-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25afa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25afa-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25afa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25afa-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25afa-134">INPUTS</span></span>

## <span data-ttu-id="25afa-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25afa-135">OUTPUTS</span></span>

### <span data-ttu-id="25afa-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25afa-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="25afa-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25afa-137">NOTES</span></span>

<span data-ttu-id="25afa-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="25afa-138">ALIASES</span></span>

## <span data-ttu-id="25afa-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25afa-139">RELATED LINKS</span></span>

