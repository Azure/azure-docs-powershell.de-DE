---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997105"
---
# <span data-ttu-id="1cae1-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="1cae1-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="1cae1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cae1-102">SYNOPSIS</span></span>
<span data-ttu-id="1cae1-103">Sie können ein Budget entweder in einem Abonnement oder in einer Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="1cae1-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1cae1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cae1-104">SYNTAX</span></span>

### <span data-ttu-id="1cae1-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cae1-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cae1-106">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1cae1-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cae1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cae1-107">DESCRIPTION</span></span>
<span data-ttu-id="1cae1-108">Mit dem New-AzConsumptionBudget-Cmdlet wird ein Budget entweder in einem Abonnement oder in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1cae1-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1cae1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cae1-109">EXAMPLES</span></span>

### <span data-ttu-id="1cae1-110">Beispiel 1: Erstellen eines Kostenbudgets mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="1cae1-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="1cae1-111">Beispiel 2: Erstellen eines Kostenbudgets mit einem Budgetnamen auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="1cae1-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="1cae1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cae1-112">PARAMETERS</span></span>

### <span data-ttu-id="1cae1-113">-Betrag</span><span class="sxs-lookup"><span data-stu-id="1cae1-113">-Amount</span></span>
<span data-ttu-id="1cae1-114">Betrag eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1cae1-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="1cae1-115">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="1cae1-115">-Category</span></span>
<span data-ttu-id="1cae1-116">Die Kategorie des Budgets kann Kosten oder Verwendung sein.</span><span class="sxs-lookup"><span data-stu-id="1cae1-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="1cae1-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="1cae1-117">-ContactEmail</span></span>
<span data-ttu-id="1cae1-118">E-Mail-Adressen, an die die Budget Benachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="1cae1-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="1cae1-119">-Kontaktliste</span><span class="sxs-lookup"><span data-stu-id="1cae1-119">-ContactGroup</span></span>
<span data-ttu-id="1cae1-120">Aktionsgruppen, an die die Budget Benachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="1cae1-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="1cae1-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="1cae1-121">-ContactRole</span></span>
<span data-ttu-id="1cae1-122">Kontaktrollen, um die Budget Benachrichtigung an zu senden, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="1cae1-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="1cae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cae1-123">-DefaultProfile</span></span>
<span data-ttu-id="1cae1-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cae1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cae1-125">-Enddate</span><span class="sxs-lookup"><span data-stu-id="1cae1-125">-EndDate</span></span>
<span data-ttu-id="1cae1-126">Enddatum (yyyy-mm-tt in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1cae1-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="1cae1-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="1cae1-127">-MeterFilter</span></span>
<span data-ttu-id="1cae1-128">Durch trennzeichengetrennte Liste der Meter, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cae1-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="1cae1-129">Erforderlich, wenn Category die Verwendung ist.</span><span class="sxs-lookup"><span data-stu-id="1cae1-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="1cae1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="1cae1-130">-Name</span></span>
<span data-ttu-id="1cae1-131">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1cae1-131">Name of a budget.</span></span>

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

### <span data-ttu-id="1cae1-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="1cae1-132">-NotificationEnabled</span></span>
<span data-ttu-id="1cae1-133">Die Benachrichtigung ist aktiviert oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1cae1-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="1cae1-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="1cae1-134">-NotificationKey</span></span>
<span data-ttu-id="1cae1-135">Der Schlüssel einer mit einem Budget verknüpften Benachrichtigung, die zum Erstellen einer Benachrichtigung mit aktiviertem Benachrichtigungs Schalter, Benachrichtigungsschwellenwert, Kontakt-e-Mails, Kontaktgruppen oder Kontaktrollen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1cae1-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="1cae1-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="1cae1-136">-NotificationThreshold</span></span>
<span data-ttu-id="1cae1-137">Schwellenwert, der einer Benachrichtigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1cae1-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="1cae1-138">Benachrichtigung wird gesendet, wenn die Kosten oder die Verwendung den Schwellenwert überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="1cae1-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="1cae1-139">Es ist immer Prozent und muss zwischen 0 und 1000 sein.</span><span class="sxs-lookup"><span data-stu-id="1cae1-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="1cae1-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="1cae1-140">-ResourceFilter</span></span>
<span data-ttu-id="1cae1-141">Durch trennzeichengetrennte Liste der Ressourcen Instanzen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cae1-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="1cae1-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="1cae1-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="1cae1-143">Durch trennzeichengetrennte Liste der Ressourcengruppen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cae1-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="1cae1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cae1-144">-ResourceGroupName</span></span>
<span data-ttu-id="1cae1-145">Ressourcengruppe eines Budgets</span><span class="sxs-lookup"><span data-stu-id="1cae1-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="1cae1-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1cae1-146">-StartDate</span></span>
<span data-ttu-id="1cae1-147">Anfangstermin (yyyy-mm-tt in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="1cae1-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="1cae1-148">Nicht vor dem aktuellen Monat für monatliche Zeit Körnung.</span><span class="sxs-lookup"><span data-stu-id="1cae1-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="1cae1-149">Nicht vor drei Monaten für Quartals Zeit.</span><span class="sxs-lookup"><span data-stu-id="1cae1-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="1cae1-150">Nicht vor 12 Monaten für Jahreszeit Getreide.</span><span class="sxs-lookup"><span data-stu-id="1cae1-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="1cae1-151">Zukünftiger Anfangstermin nicht mehr als drei Monate.</span><span class="sxs-lookup"><span data-stu-id="1cae1-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="1cae1-152">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="1cae1-152">-TimeGrain</span></span>
<span data-ttu-id="1cae1-153">Die Zeitspanne des Budgets kann monatlich, quartalsweise oder jährlich sein.</span><span class="sxs-lookup"><span data-stu-id="1cae1-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="1cae1-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1cae1-154">-Confirm</span></span>
<span data-ttu-id="1cae1-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cae1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cae1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cae1-156">-WhatIf</span></span>
<span data-ttu-id="1cae1-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cae1-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cae1-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cae1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cae1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cae1-159">CommonParameters</span></span>
<span data-ttu-id="1cae1-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cae1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cae1-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cae1-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cae1-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cae1-162">INPUTS</span></span>

### <span data-ttu-id="1cae1-163">Keine</span><span class="sxs-lookup"><span data-stu-id="1cae1-163">None</span></span>

## <span data-ttu-id="1cae1-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cae1-164">OUTPUTS</span></span>

### <span data-ttu-id="1cae1-165">Microsoft. Azure. Commands. Verbrauch. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="1cae1-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1cae1-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cae1-166">NOTES</span></span>

## <span data-ttu-id="1cae1-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cae1-167">RELATED LINKS</span></span>
