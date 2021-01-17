---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473262"
---
# <span data-ttu-id="1d8ee-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="1d8ee-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="1d8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8ee-103">Sie erhalten eine Liste der Budgets in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1d8ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d8ee-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d8ee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d8ee-105">DESCRIPTION</span></span>
<span data-ttu-id="1d8ee-106">Das Get-AzConsumptionBudget-Cmdlet ruft eine Liste der Budgets in einem Abonnement oder einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1d8ee-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d8ee-107">EXAMPLES</span></span>

### <span data-ttu-id="1d8ee-108">Beispiel 1: Erhalten einer Liste der Budgets auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="1d8ee-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1d8ee-109">Beispiel 2: Erhalten einer Liste der Budgets auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="1d8ee-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1d8ee-110">Beispiel 3: Erhalten eines Budgets mit dem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="1d8ee-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1d8ee-111">Beispiel 4: Erhalten eines Budgets mit dem Budgetnamen auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="1d8ee-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="1d8ee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d8ee-112">PARAMETERS</span></span>

### <span data-ttu-id="1d8ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8ee-113">-DefaultProfile</span></span>
<span data-ttu-id="1d8ee-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d8ee-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1d8ee-115">-Name</span></span>
<span data-ttu-id="1d8ee-116">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d8ee-118">Ressourcengruppe eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8ee-119">CommonParameters</span></span>
<span data-ttu-id="1d8ee-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8ee-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8ee-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8ee-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d8ee-122">INPUTS</span></span>

### <span data-ttu-id="1d8ee-123">Keine</span><span class="sxs-lookup"><span data-stu-id="1d8ee-123">None</span></span>

## <span data-ttu-id="1d8ee-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d8ee-124">OUTPUTS</span></span>

### <span data-ttu-id="1d8ee-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="1d8ee-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1d8ee-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d8ee-126">NOTES</span></span>

## <span data-ttu-id="1d8ee-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d8ee-127">RELATED LINKS</span></span>
