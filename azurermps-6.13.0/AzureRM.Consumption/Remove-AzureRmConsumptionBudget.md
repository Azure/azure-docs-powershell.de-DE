---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502169"
---
# <span data-ttu-id="580a0-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="580a0-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="580a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="580a0-102">SYNOPSIS</span></span>
<span data-ttu-id="580a0-103">Entfernen eines Budgets entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="580a0-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="580a0-104">SYNTAX</span></span>

### <span data-ttu-id="580a0-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="580a0-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="580a0-106">Rohrleitungs</span><span class="sxs-lookup"><span data-stu-id="580a0-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="580a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="580a0-107">DESCRIPTION</span></span>
<span data-ttu-id="580a0-108">Das Remove-AzureRmConsumptionBudget-Cmdlet entfernt ein Budget entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="580a0-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="580a0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="580a0-109">EXAMPLES</span></span>

### <span data-ttu-id="580a0-110">Beispiel 1: Entfernen eines Budgets mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="580a0-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="580a0-111">Beispiel 2: Entfernen eines Budgets mit einem Budgetnamen auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="580a0-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="580a0-112">Beispiel 3: Entfernen eines Budgets über die Rohrverlegung auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="580a0-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="580a0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="580a0-113">PARAMETERS</span></span>

### <span data-ttu-id="580a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580a0-114">-DefaultProfile</span></span>
<span data-ttu-id="580a0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="580a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580a0-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="580a0-116">-InputObject</span></span>
<span data-ttu-id="580a0-117">Budget Objekt.</span><span class="sxs-lookup"><span data-stu-id="580a0-117">Budget object.</span></span>

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

### <span data-ttu-id="580a0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="580a0-118">-Name</span></span>
<span data-ttu-id="580a0-119">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="580a0-119">Name of a budget.</span></span>

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

### <span data-ttu-id="580a0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="580a0-120">-PassThru</span></span>
<span data-ttu-id="580a0-121">Das Cmdlet gibt true zurück, wenn ein Budget erfolgreich entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="580a0-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="580a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="580a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="580a0-123">Ressourcengruppe eines Budgets</span><span class="sxs-lookup"><span data-stu-id="580a0-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="580a0-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="580a0-124">-Confirm</span></span>
<span data-ttu-id="580a0-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="580a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="580a0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="580a0-126">-WhatIf</span></span>
<span data-ttu-id="580a0-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="580a0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="580a0-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="580a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="580a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580a0-129">CommonParameters</span></span>
<span data-ttu-id="580a0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="580a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580a0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580a0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="580a0-132">INPUTS</span></span>

### <span data-ttu-id="580a0-133">Microsoft. Azure. Commands. Verbrauch. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="580a0-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="580a0-134">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="580a0-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="580a0-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="580a0-135">OUTPUTS</span></span>

### <span data-ttu-id="580a0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="580a0-136">System.Boolean</span></span>

## <span data-ttu-id="580a0-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="580a0-137">NOTES</span></span>

## <span data-ttu-id="580a0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="580a0-138">RELATED LINKS</span></span>
