---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 138d9d7510331a385246c99e57ce3f460899ad33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652359"
---
# <span data-ttu-id="8ec7e-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="8ec7e-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="8ec7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ec7e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec7e-103">Entfernen eines Budgets entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8ec7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ec7e-104">SYNTAX</span></span>

### <span data-ttu-id="8ec7e-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ec7e-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec7e-106">Rohrleitungs</span><span class="sxs-lookup"><span data-stu-id="8ec7e-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec7e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ec7e-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec7e-108">Das Remove-AzConsumptionBudget-Cmdlet entfernt ein Budget entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8ec7e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ec7e-109">EXAMPLES</span></span>

### <span data-ttu-id="8ec7e-110">Beispiel 1: Entfernen eines Budgets mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="8ec7e-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="8ec7e-111">Beispiel 2: Entfernen eines Budgets mit einem Budgetnamen auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="8ec7e-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="8ec7e-112">Beispiel 3: Entfernen eines Budgets über die Rohrverlegung auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="8ec7e-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="8ec7e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ec7e-113">PARAMETERS</span></span>

### <span data-ttu-id="8ec7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec7e-114">-DefaultProfile</span></span>
<span data-ttu-id="8ec7e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec7e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ec7e-116">-InputObject</span></span>
<span data-ttu-id="8ec7e-117">Budget Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-117">Budget object.</span></span>

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

### <span data-ttu-id="8ec7e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8ec7e-118">-Name</span></span>
<span data-ttu-id="8ec7e-119">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-119">Name of a budget.</span></span>

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

### <span data-ttu-id="8ec7e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ec7e-120">-PassThru</span></span>
<span data-ttu-id="8ec7e-121">Das Cmdlet gibt true zurück, wenn ein Budget erfolgreich entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="8ec7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ec7e-123">Ressourcengruppe eines Budgets</span><span class="sxs-lookup"><span data-stu-id="8ec7e-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="8ec7e-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ec7e-124">-Confirm</span></span>
<span data-ttu-id="8ec7e-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec7e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec7e-126">-WhatIf</span></span>
<span data-ttu-id="8ec7e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec7e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec7e-129">CommonParameters</span></span>
<span data-ttu-id="8ec7e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec7e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec7e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec7e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ec7e-132">INPUTS</span></span>

### <span data-ttu-id="8ec7e-133">Microsoft. Azure. Commands. Verbrauch. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="8ec7e-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="8ec7e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ec7e-134">OUTPUTS</span></span>

### <span data-ttu-id="8ec7e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec7e-135">System.Boolean</span></span>

## <span data-ttu-id="8ec7e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ec7e-136">NOTES</span></span>

## <span data-ttu-id="8ec7e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ec7e-137">RELATED LINKS</span></span>
