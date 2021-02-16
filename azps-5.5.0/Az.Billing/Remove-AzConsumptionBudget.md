---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168169"
---
# <span data-ttu-id="339fb-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="339fb-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="339fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339fb-102">SYNOPSIS</span></span>
<span data-ttu-id="339fb-103">Entfernen sie ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="339fb-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="339fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="339fb-104">SYNTAX</span></span>

### <span data-ttu-id="339fb-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="339fb-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339fb-106">Piping</span><span class="sxs-lookup"><span data-stu-id="339fb-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="339fb-107">DESCRIPTION</span></span>
<span data-ttu-id="339fb-108">Das Remove-AzConsumptionBudget-Cmdlet entfernt ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="339fb-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="339fb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="339fb-109">EXAMPLES</span></span>

### <span data-ttu-id="339fb-110">Beispiel 1: Entfernen eines Budgets mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="339fb-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="339fb-111">Beispiel 2: Entfernen eines Budgets mit einem Budgetnamen auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="339fb-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="339fb-112">Beispiel 3: Entfernen eines Budgets durch Piping auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="339fb-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="339fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="339fb-113">PARAMETERS</span></span>

### <span data-ttu-id="339fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339fb-114">-DefaultProfile</span></span>
<span data-ttu-id="339fb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="339fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339fb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="339fb-116">-InputObject</span></span>
<span data-ttu-id="339fb-117">Budgetobjekt.</span><span class="sxs-lookup"><span data-stu-id="339fb-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="339fb-118">-Name</span></span>
<span data-ttu-id="339fb-119">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="339fb-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339fb-120">-PassThru</span></span>
<span data-ttu-id="339fb-121">Das Cmdlet gibt "true" zurück, wenn ein Budget erfolgreich entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="339fb-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="339fb-123">Ressourcengruppe eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="339fb-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339fb-124">-Confirm</span></span>
<span data-ttu-id="339fb-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="339fb-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="339fb-126">-WhatIf</span></span>
<span data-ttu-id="339fb-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="339fb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339fb-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="339fb-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339fb-129">CommonParameters</span></span>
<span data-ttu-id="339fb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339fb-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339fb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339fb-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="339fb-132">INPUTS</span></span>

### <span data-ttu-id="339fb-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="339fb-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="339fb-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="339fb-134">OUTPUTS</span></span>

### <span data-ttu-id="339fb-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="339fb-135">System.Boolean</span></span>

## <span data-ttu-id="339fb-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="339fb-136">NOTES</span></span>

## <span data-ttu-id="339fb-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="339fb-137">RELATED LINKS</span></span>
