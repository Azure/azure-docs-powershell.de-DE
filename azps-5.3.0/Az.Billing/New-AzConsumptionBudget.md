---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471064"
---
# <span data-ttu-id="74448-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="74448-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="74448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74448-102">SYNOPSIS</span></span>
<span data-ttu-id="74448-103">Erstellen Sie ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74448-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="74448-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74448-104">SYNTAX</span></span>

### <span data-ttu-id="74448-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="74448-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74448-106">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="74448-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74448-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74448-107">DESCRIPTION</span></span>
<span data-ttu-id="74448-108">Das New-AzConsumptionBudget erstellt ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74448-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="74448-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74448-109">EXAMPLES</span></span>

### <span data-ttu-id="74448-110">Beispiel 1: Erstellen eines Kostenbudgets mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="74448-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="74448-111">Beispiel 2: Erstellen eines Kostenbudgets mit einem Budgetnamen auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="74448-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="74448-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74448-112">PARAMETERS</span></span>

### <span data-ttu-id="74448-113">-Amount</span><span class="sxs-lookup"><span data-stu-id="74448-113">-Amount</span></span>
<span data-ttu-id="74448-114">Der Betrag eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="74448-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-115">-Category</span><span class="sxs-lookup"><span data-stu-id="74448-115">-Category</span></span>
<span data-ttu-id="74448-116">Die Kategorie des Budgets kann Kosten oder Nutzung sein.</span><span class="sxs-lookup"><span data-stu-id="74448-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="74448-117">-ContactEmail</span></span>
<span data-ttu-id="74448-118">E-Mail-Adressen, an die die Budgetbenachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="74448-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="74448-119">-ContactGroup</span></span>
<span data-ttu-id="74448-120">Aktionsgruppen, an die die Budgetbenachrichtigung gesendet wird, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="74448-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="74448-121">-ContactRole</span></span>
<span data-ttu-id="74448-122">Kontaktrollen, an die die Budgetbenachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="74448-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74448-123">-DefaultProfile</span></span>
<span data-ttu-id="74448-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74448-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74448-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="74448-125">-EndDate</span></span>
<span data-ttu-id="74448-126">Enddatum (JJJJ-MM-TT in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="74448-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="74448-127">-MeterFilter</span></span>
<span data-ttu-id="74448-128">Durch Kommas getrennte Liste von Metern, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74448-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="74448-129">Erforderlich, wenn es sich bei der Kategorie um eine Nutzung handelt.</span><span class="sxs-lookup"><span data-stu-id="74448-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-130">-Name</span><span class="sxs-lookup"><span data-stu-id="74448-130">-Name</span></span>
<span data-ttu-id="74448-131">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="74448-131">Name of a budget.</span></span>

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

### <span data-ttu-id="74448-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="74448-132">-NotificationEnabled</span></span>
<span data-ttu-id="74448-133">Die Benachrichtigung ist aktiviert oder nicht.</span><span class="sxs-lookup"><span data-stu-id="74448-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="74448-134">-NotificationKey</span></span>
<span data-ttu-id="74448-135">Schlüssel einer einem Budget zugeordneten Benachrichtigung, die erforderlich ist, um eine Benachrichtigung mit aktivierter Benachrichtigungsschalter, Benachrichtigungsschwellenwert, Kontakt-E-Mails, Kontaktgruppen oder Kontaktrollen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="74448-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="74448-136">-NotificationThreshold</span></span>
<span data-ttu-id="74448-137">Schwellenwert, der einer Benachrichtigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="74448-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="74448-138">Eine Benachrichtigung wird gesendet, wenn die Kosten oder die Nutzung den Schwellenwert überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="74448-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="74448-139">Er ist immer Prozent und muss zwischen 0 und 1000 liegen.</span><span class="sxs-lookup"><span data-stu-id="74448-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="74448-140">-ResourceFilter</span></span>
<span data-ttu-id="74448-141">Durch Kommas getrennte Liste der Ressourceninstanzen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74448-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="74448-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="74448-143">Durch Kommas getrennte Liste der Ressourcengruppen, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74448-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74448-144">-ResourceGroupName</span></span>
<span data-ttu-id="74448-145">Ressourcengruppe eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="74448-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="74448-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="74448-146">-StartDate</span></span>
<span data-ttu-id="74448-147">Startdatum (JJJJ-MM-TT in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="74448-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="74448-148">Nicht vor dem aktuellen Monat für monatliche Zeitkörner.</span><span class="sxs-lookup"><span data-stu-id="74448-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="74448-149">Für vierteljährliche Zeitkörner nicht vor drei Monaten.</span><span class="sxs-lookup"><span data-stu-id="74448-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="74448-150">Nicht vor zwölf Monaten für die Jahreszeit.</span><span class="sxs-lookup"><span data-stu-id="74448-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="74448-151">Zukünftiger Starttermin nicht mehr als drei Monate.</span><span class="sxs-lookup"><span data-stu-id="74448-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="74448-152">-TimeGrain</span></span>
<span data-ttu-id="74448-153">Das Zeitmass des Budgets kann monatlich, vierteljährlich oder jährlich sein.</span><span class="sxs-lookup"><span data-stu-id="74448-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74448-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74448-154">-Confirm</span></span>
<span data-ttu-id="74448-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74448-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74448-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74448-156">-WhatIf</span></span>
<span data-ttu-id="74448-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74448-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74448-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74448-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74448-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74448-159">CommonParameters</span></span>
<span data-ttu-id="74448-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74448-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74448-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74448-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74448-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74448-162">INPUTS</span></span>

### <span data-ttu-id="74448-163">Keine</span><span class="sxs-lookup"><span data-stu-id="74448-163">None</span></span>

## <span data-ttu-id="74448-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74448-164">OUTPUTS</span></span>

### <span data-ttu-id="74448-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="74448-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="74448-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74448-166">NOTES</span></span>

## <span data-ttu-id="74448-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74448-167">RELATED LINKS</span></span>
