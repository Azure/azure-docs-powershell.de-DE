---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: c159ab71befb52e8131ade0b90e69c4ba8158885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661643"
---
# <span data-ttu-id="e8b13-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="e8b13-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="e8b13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8b13-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b13-103">Aktualisieren eines Budgets entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8b13-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="e8b13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8b13-104">SYNTAX</span></span>

### <span data-ttu-id="e8b13-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8b13-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b13-106">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e8b13-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b13-107">Rohrleitungs</span><span class="sxs-lookup"><span data-stu-id="e8b13-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8b13-108">Rohrleitungs-und Benachrichtigungs-</span><span class="sxs-lookup"><span data-stu-id="e8b13-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b13-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8b13-109">DESCRIPTION</span></span>
<span data-ttu-id="e8b13-110">Das Set-AzConsumptionBudget-Cmdlet aktualisiert ein Budget entweder in einem Abonnement oder in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8b13-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="e8b13-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8b13-111">EXAMPLES</span></span>

### <span data-ttu-id="e8b13-112">Beispiel 1: Aktualisieren eines Budgets um einen neuen Betrag mit einem Budgetnamen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="e8b13-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
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

### <span data-ttu-id="e8b13-113">Beispiel 2: Aktualisieren eines Budgets mit einer Benachrichtigung, wenn die Kosten oder Verwendung einen Schwellenwert von 90 Prozent des Betrags auf Abonnementebene erreicht</span><span class="sxs-lookup"><span data-stu-id="e8b13-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
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

### <span data-ttu-id="e8b13-114">Beispiel 3: Aktualisieren eines Budgets um einen neuen Betrag mit einem Budgetnamen auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="e8b13-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
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

## <span data-ttu-id="e8b13-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8b13-115">PARAMETERS</span></span>

### <span data-ttu-id="e8b13-116">-Betrag</span><span class="sxs-lookup"><span data-stu-id="e8b13-116">-Amount</span></span>
<span data-ttu-id="e8b13-117">Betrag eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="e8b13-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="e8b13-118">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="e8b13-118">-Category</span></span>
<span data-ttu-id="e8b13-119">Die Kategorie des Budgets kann Kosten oder Verwendung sein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="e8b13-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="e8b13-120">-ContactEmail</span></span>
<span data-ttu-id="e8b13-121">E-Mail-Adressen, an die die Budget Benachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="e8b13-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="e8b13-122">-Kontaktliste</span><span class="sxs-lookup"><span data-stu-id="e8b13-122">-ContactGroup</span></span>
<span data-ttu-id="e8b13-123">Aktionsgruppen, an die die Budget Benachrichtigung gesendet werden soll, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="e8b13-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="e8b13-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="e8b13-124">-ContactRole</span></span>
<span data-ttu-id="e8b13-125">Kontaktrollen, um die Budget Benachrichtigung an zu senden, wenn der Schwellenwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="e8b13-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="e8b13-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b13-126">-DefaultProfile</span></span>
<span data-ttu-id="e8b13-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8b13-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b13-128">-Enddate</span><span class="sxs-lookup"><span data-stu-id="e8b13-128">-EndDate</span></span>
<span data-ttu-id="e8b13-129">Enddatum (yyyy-mm-tt in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="e8b13-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="e8b13-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8b13-130">-InputObject</span></span>
<span data-ttu-id="e8b13-131">Budget Objekt.</span><span class="sxs-lookup"><span data-stu-id="e8b13-131">Budget object.</span></span>

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

### <span data-ttu-id="e8b13-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="e8b13-132">-MeterFilter</span></span>
<span data-ttu-id="e8b13-133">Durch trennzeichengetrennte Liste der Meter, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8b13-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="e8b13-134">Erforderlich, wenn Category die Verwendung ist.</span><span class="sxs-lookup"><span data-stu-id="e8b13-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="e8b13-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e8b13-135">-Name</span></span>
<span data-ttu-id="e8b13-136">Name eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="e8b13-136">Name of a budget.</span></span>

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

### <span data-ttu-id="e8b13-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="e8b13-137">-NotificationEnabled</span></span>
<span data-ttu-id="e8b13-138">Die Benachrichtigung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e8b13-138">The notification is enabled.</span></span>
<span data-ttu-id="e8b13-139">Wenn diese Option nicht angegeben ist, ist die Benachrichtigung standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e8b13-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="e8b13-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="e8b13-140">-NotificationKey</span></span>
<span data-ttu-id="e8b13-141">Der Schlüssel einer mit einem Budget verknüpften Benachrichtigung, die zum Erstellen einer Benachrichtigung mit aktiviertem Benachrichtigungs Schalter, Benachrichtigungsschwellenwert, Kontakt-e-Mails, Kontaktgruppen oder Kontaktrollen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e8b13-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="e8b13-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="e8b13-142">-NotificationThreshold</span></span>
<span data-ttu-id="e8b13-143">Schwellenwert, der einer Benachrichtigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8b13-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="e8b13-144">Benachrichtigung wird gesendet, wenn die Kosten oder die Verwendung den Schwellenwert überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="e8b13-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="e8b13-145">Es ist immer Prozent und muss zwischen 0 und 1000 sein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="e8b13-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="e8b13-146">-ResourceFilter</span></span>
<span data-ttu-id="e8b13-147">Durch trennzeichengetrennte Liste der Ressourcen Instanzen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8b13-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="e8b13-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="e8b13-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="e8b13-149">Durch trennzeichengetrennte Liste der Ressourcengruppen, nach denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8b13-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="e8b13-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b13-150">-ResourceGroupName</span></span>
<span data-ttu-id="e8b13-151">Ressourcengruppe eines Budgets</span><span class="sxs-lookup"><span data-stu-id="e8b13-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="e8b13-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e8b13-152">-StartDate</span></span>
<span data-ttu-id="e8b13-153">Anfangstermin (yyyy-mm-tt in UTC) des Zeitraums eines Budgets.</span><span class="sxs-lookup"><span data-stu-id="e8b13-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="e8b13-154">Nicht vor dem aktuellen Monat für monatliche Zeit Körnung.</span><span class="sxs-lookup"><span data-stu-id="e8b13-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="e8b13-155">Nicht vor drei Monaten für Quartals Zeit.</span><span class="sxs-lookup"><span data-stu-id="e8b13-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="e8b13-156">Nicht vor 12 Monaten für Jahreszeit Getreide.</span><span class="sxs-lookup"><span data-stu-id="e8b13-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="e8b13-157">Zukünftiger Anfangstermin nicht mehr als drei Monate.</span><span class="sxs-lookup"><span data-stu-id="e8b13-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="e8b13-158">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="e8b13-158">-TimeGrain</span></span>
<span data-ttu-id="e8b13-159">Die Zeitspanne des Budgets kann monatlich, quartalsweise oder jährlich sein.</span><span class="sxs-lookup"><span data-stu-id="e8b13-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="e8b13-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8b13-160">-Confirm</span></span>
<span data-ttu-id="e8b13-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8b13-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b13-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b13-162">-WhatIf</span></span>
<span data-ttu-id="e8b13-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8b13-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b13-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b13-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b13-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b13-165">CommonParameters</span></span>
<span data-ttu-id="e8b13-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b13-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b13-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b13-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b13-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8b13-168">INPUTS</span></span>

### <span data-ttu-id="e8b13-169">Microsoft. Azure. Commands. Verbrauch. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="e8b13-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="e8b13-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8b13-170">OUTPUTS</span></span>

### <span data-ttu-id="e8b13-171">Microsoft. Azure. Commands. Verbrauch. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="e8b13-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="e8b13-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8b13-172">NOTES</span></span>

## <span data-ttu-id="e8b13-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8b13-173">RELATED LINKS</span></span>
