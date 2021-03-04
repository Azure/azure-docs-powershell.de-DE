---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: fa0b8ae9adaca5a187136f068dfd8797ed9e4b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923056"
---
# <span data-ttu-id="40cdb-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="40cdb-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="40cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="40cdb-103">Aktualisieren Sie ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40cdb-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="40cdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40cdb-104">SYNTAX</span></span>

### <span data-ttu-id="40cdb-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="40cdb-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40cdb-106">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="40cdb-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40cdb-107">Piping</span><span class="sxs-lookup"><span data-stu-id="40cdb-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40cdb-108">Piping and Notification</span><span class="sxs-lookup"><span data-stu-id="40cdb-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40cdb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40cdb-109">DESCRIPTION</span></span>
<span data-ttu-id="40cdb-110">Das Set-AzConsumptionBudget-Cmdlet aktualisiert ein Budget in einem Abonnement oder einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40cdb-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="40cdb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40cdb-111">EXAMPLES</span></span>

### <span data-ttu-id="40cdb-112">Beispiel 1: Aktualisieren eines Budgets um einen neuen Betrag mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="40cdb-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="40cdb-113">Beispiel 2: Aktualisieren eines Budgets mit einer Benachrichtigung, wenn Kosten oder Nutzung einen Schwellenwert von 90 Prozent des Betrags auf Abonnementebene erreichen</span><span class="sxs-lookup"><span data-stu-id="40cdb-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="40cdb-114">Beispiel 3: Aktualisieren eines Budgets um einen neuen Betrag mit einem Budgetnamen auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="40cdb-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="40cdb-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40cdb-115">PARAMETERS</span></span>

### <span data-ttu-id="40cdb-116">-Betrag</span><span class="sxs-lookup"><span data-stu-id="40cdb-116">-Amount</span></span>
<span data-ttu-id="40cdb-117">Betrag eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="40cdb-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-118">-Category</span><span class="sxs-lookup"><span data-stu-id="40cdb-118">-Category</span></span>
<span data-ttu-id="40cdb-119">Die Kategorie des Budgets kann Kosten oder Nutzung sein.</span><span class="sxs-lookup"><span data-stu-id="40cdb-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="40cdb-120">-ContactEmail</span></span>
<span data-ttu-id="40cdb-121">E-Mail-Adressen, an die die Budgetbenachrichtigung gesendet wird, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="40cdb-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="40cdb-122">-ContactGroup</span></span>
<span data-ttu-id="40cdb-123">Aktionsgruppen, an die die Budgetbenachrichtigung gesendet wird, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="40cdb-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="40cdb-124">-ContactRole</span></span>
<span data-ttu-id="40cdb-125">Kontaktrollen, an die die Budgetbenachrichtigung gesendet wird, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="40cdb-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cdb-126">-DefaultProfile</span></span>
<span data-ttu-id="40cdb-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40cdb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40cdb-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="40cdb-128">-EndDate</span></span>
<span data-ttu-id="40cdb-129">Enddatum (JJJJ-MM-TT in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="40cdb-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="40cdb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40cdb-130">-InputObject</span></span>
<span data-ttu-id="40cdb-131">Budgetobjekt.</span><span class="sxs-lookup"><span data-stu-id="40cdb-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="40cdb-132">-MeterFilter</span></span>
<span data-ttu-id="40cdb-133">Durch Kommas getrennte Liste der Meter, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40cdb-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="40cdb-134">Erforderlich, wenn Kategorie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40cdb-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="40cdb-135">-Name</span><span class="sxs-lookup"><span data-stu-id="40cdb-135">-Name</span></span>
<span data-ttu-id="40cdb-136">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="40cdb-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="40cdb-137">-NotificationEnabled</span></span>
<span data-ttu-id="40cdb-138">Die Benachrichtigung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="40cdb-138">The notification is enabled.</span></span>
<span data-ttu-id="40cdb-139">Wenn nicht angegeben, ist die Benachrichtigung standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40cdb-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="40cdb-140">-NotificationKey</span></span>
<span data-ttu-id="40cdb-141">Schlüssel einer Benachrichtigung, die einem Budget zugeordnet ist und zum Erstellen einer Benachrichtigung mit aktivierter Benachrichtigung, Benachrichtigungsschwellenwert, Kontakt-E-Mails, Kontaktgruppen oder Kontaktrollen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="40cdb-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="40cdb-142">-NotificationThreshold</span></span>
<span data-ttu-id="40cdb-143">Schwellenwert, der einer Benachrichtigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="40cdb-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="40cdb-144">Benachrichtigungen werden gesendet, wenn die Kosten oder die Nutzung den Schwellenwert überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="40cdb-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="40cdb-145">Er ist immer Prozent und muss zwischen 0 und 1000 liegen.</span><span class="sxs-lookup"><span data-stu-id="40cdb-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="40cdb-146">-ResourceFilter</span></span>
<span data-ttu-id="40cdb-147">Durch Kommas getrennte Liste der Ressourceninstanzen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40cdb-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="40cdb-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="40cdb-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="40cdb-149">Durch Kommas getrennte Liste der Ressourcengruppen, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40cdb-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="40cdb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cdb-150">-ResourceGroupName</span></span>
<span data-ttu-id="40cdb-151">Ressourcengruppe eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="40cdb-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="40cdb-152">-StartDate</span></span>
<span data-ttu-id="40cdb-153">Startdatum (JJJJ-MM-TT in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="40cdb-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="40cdb-154">Nicht vor dem aktuellen Monat für monatliche Zeitkörner.</span><span class="sxs-lookup"><span data-stu-id="40cdb-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="40cdb-155">Nicht vor drei Monaten für vierteljährliche Zeitkörner.</span><span class="sxs-lookup"><span data-stu-id="40cdb-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="40cdb-156">Nicht vor zwölf Monaten für Jahreszeitkörner.</span><span class="sxs-lookup"><span data-stu-id="40cdb-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="40cdb-157">Zukünftiges Startdatum nicht mehr als drei Monate.</span><span class="sxs-lookup"><span data-stu-id="40cdb-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="40cdb-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="40cdb-158">-TimeGrain</span></span>
<span data-ttu-id="40cdb-159">Das Zeitmass des Budgets kann monatlich, vierteljährlich oder jährlich sein.</span><span class="sxs-lookup"><span data-stu-id="40cdb-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cdb-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40cdb-160">-Confirm</span></span>
<span data-ttu-id="40cdb-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40cdb-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40cdb-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40cdb-162">-WhatIf</span></span>
<span data-ttu-id="40cdb-163">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40cdb-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40cdb-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40cdb-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40cdb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cdb-165">CommonParameters</span></span>
<span data-ttu-id="40cdb-166">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cdb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cdb-167">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40cdb-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cdb-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40cdb-168">INPUTS</span></span>

### <span data-ttu-id="40cdb-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="40cdb-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="40cdb-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40cdb-170">OUTPUTS</span></span>

### <span data-ttu-id="40cdb-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="40cdb-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="40cdb-172">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40cdb-172">NOTES</span></span>

## <span data-ttu-id="40cdb-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40cdb-173">RELATED LINKS</span></span>
