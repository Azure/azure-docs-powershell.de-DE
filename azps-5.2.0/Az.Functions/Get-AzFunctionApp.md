---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298016"
---
# <span data-ttu-id="3eb6c-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="3eb6c-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="3eb6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb6c-103">Ruft Funktions-Apps in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3eb6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eb6c-104">SYNTAX</span></span>

### <span data-ttu-id="3eb6c-105">GetAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="3eb6c-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3eb6c-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="3eb6c-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3eb6c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="3eb6c-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3eb6c-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb6c-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3eb6c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eb6c-109">DESCRIPTION</span></span>
<span data-ttu-id="3eb6c-110">Ruft Funktions-Apps in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="3eb6c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3eb6c-111">EXAMPLES</span></span>

### <span data-ttu-id="3eb6c-112">Beispiel 1: Alle Funktions-Apps herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3eb6c-113">Beispiel 2: Holen Sie sich Funktions-Apps nach Name.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3eb6c-114">Beispiel 3: "Funktions-Apps nach Ressourcengruppennamen herunterladen".</span><span class="sxs-lookup"><span data-stu-id="3eb6c-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3eb6c-115">Beispiel 4: Herunterladen von Funktions-Apps für die angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="3eb6c-116">Beispiel 5: Herunterladen von Funktions-Apps nach Standort.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="3eb6c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb6c-117">PARAMETERS</span></span>

### <span data-ttu-id="3eb6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb6c-118">-DefaultProfile</span></span>
<span data-ttu-id="3eb6c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb6c-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="3eb6c-120">-IncludeSlot</span></span>
<span data-ttu-id="3eb6c-121">Wird verwendet, um anzugeben, ob Bereitstellungsplätze in ergebnisse enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb6c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="3eb6c-122">-Location</span></span>
<span data-ttu-id="3eb6c-123">Die Position der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-123">The location of the function app.</span></span>

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

### <span data-ttu-id="3eb6c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3eb6c-124">-Name</span></span>
<span data-ttu-id="3eb6c-125">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-125">The name of the function app.</span></span>

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

### <span data-ttu-id="3eb6c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb6c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3eb6c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3eb6c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3eb6c-128">-SubscriptionId</span></span>
<span data-ttu-id="3eb6c-129">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3eb6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb6c-130">CommonParameters</span></span>
<span data-ttu-id="3eb6c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb6c-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eb6c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb6c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3eb6c-133">INPUTS</span></span>

## <span data-ttu-id="3eb6c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3eb6c-134">OUTPUTS</span></span>

### <span data-ttu-id="3eb6c-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="3eb6c-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="3eb6c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3eb6c-136">NOTES</span></span>

<span data-ttu-id="3eb6c-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3eb6c-137">ALIASES</span></span>

## <span data-ttu-id="3eb6c-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3eb6c-138">RELATED LINKS</span></span>

