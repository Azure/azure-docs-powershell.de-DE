---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173781"
---
# <span data-ttu-id="e9f1d-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="e9f1d-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="e9f1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f1d-103">Abrufen von Funktions-apps-Plänen in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="e9f1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9f1d-104">SYNTAX</span></span>

### <span data-ttu-id="e9f1d-105">GetAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9f1d-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9f1d-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="e9f1d-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f1d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e9f1d-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9f1d-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f1d-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f1d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9f1d-109">DESCRIPTION</span></span>
<span data-ttu-id="e9f1d-110">Abrufen von Funktions-apps-Plänen in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="e9f1d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9f1d-111">EXAMPLES</span></span>

### <span data-ttu-id="e9f1d-112">Beispiel 1: Abrufen aller Funktions-APP-Pläne.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="e9f1d-113">Dieser Befehl ruft alle Funktions-APP-Pläne ab.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="e9f1d-114">Beispiel 2: Abrufen von Funktions-APP-Plänen nach Ressourcengruppennamen.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="e9f1d-115">Dieser Befehl ruft Funktions-APP-Pläne nach dem Namen der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="e9f1d-116">Beispiel 3: Abrufen von Funktions-APP-Plänen für die angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="e9f1d-117">Dieser Befehl ruft Funktions-APP-Pläne für die angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="e9f1d-118">Beispiel 4: Abrufen von Funktions-APP-Plänen nach Standort.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="e9f1d-119">Dieser Befehl ruft Funktions-APP-Pläne nach Position ab.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="e9f1d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9f1d-120">PARAMETERS</span></span>

### <span data-ttu-id="e9f1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f1d-121">-DefaultProfile</span></span>
<span data-ttu-id="e9f1d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f1d-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="e9f1d-123">-Location</span></span>
<span data-ttu-id="e9f1d-124">Der Speicherort des Funktions-APP-Plans.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="e9f1d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9f1d-125">-Name</span></span>
<span data-ttu-id="e9f1d-126">Der Name des Service Planes.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-126">The service plan name.</span></span>

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

### <span data-ttu-id="e9f1d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f1d-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9f1d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9f1d-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e9f1d-129">-SubscriptionId</span></span>
<span data-ttu-id="e9f1d-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e9f1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f1d-131">CommonParameters</span></span>
<span data-ttu-id="e9f1d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f1d-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9f1d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f1d-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9f1d-134">INPUTS</span></span>

## <span data-ttu-id="e9f1d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9f1d-135">OUTPUTS</span></span>

### <span data-ttu-id="e9f1d-136">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9f1d-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="e9f1d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9f1d-137">NOTES</span></span>

<span data-ttu-id="e9f1d-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="e9f1d-138">ALIASES</span></span>

## <span data-ttu-id="e9f1d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9f1d-139">RELATED LINKS</span></span>

