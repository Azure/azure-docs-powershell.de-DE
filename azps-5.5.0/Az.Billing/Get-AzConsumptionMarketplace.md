---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 0dfdec27fe53aaf40ebd46a2c623047381faa554
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171443"
---
# <span data-ttu-id="859e1-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="859e1-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="859e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="859e1-102">SYNOPSIS</span></span>
<span data-ttu-id="859e1-103">Holen Sie sich Marketplaces des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="859e1-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="859e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="859e1-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="859e1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="859e1-105">DESCRIPTION</span></span>
<span data-ttu-id="859e1-106">Das **Cmdlet "Get-AzConsumptionMarketplace"** ruft Marketplaces des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="859e1-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="859e1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="859e1-107">EXAMPLES</span></span>

### <span data-ttu-id="859e1-108">Beispiel 1: Nutzung von Marketplaces</span><span class="sxs-lookup"><span data-stu-id="859e1-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="859e1-109">Beispiel 2: Erhalten der Marketplace-Nutzung mit Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="859e1-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="859e1-110">Beispiel 3: Erhalten der Marketplace-Nutzung von BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="859e1-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="859e1-111">Beispiel 4: Get marketplace usage with InstanceName filter</span><span class="sxs-lookup"><span data-stu-id="859e1-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="859e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="859e1-112">PARAMETERS</span></span>

### <span data-ttu-id="859e1-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="859e1-113">-BillingPeriodName</span></span>
<span data-ttu-id="859e1-114">Name eines bestimmten Abrechnungszeitraums, um den Marketplace zu erhalten, der zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="859e1-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="859e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859e1-115">-DefaultProfile</span></span>
<span data-ttu-id="859e1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="859e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859e1-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="859e1-117">-EndDate</span></span>
<span data-ttu-id="859e1-118">Das Enddatum (in UTC) der zu filternden Marketplaces.</span><span class="sxs-lookup"><span data-stu-id="859e1-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="859e1-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="859e1-119">-InstanceId</span></span>
<span data-ttu-id="859e1-120">Die Instanz-ID der zu filternden Marketplaces.</span><span class="sxs-lookup"><span data-stu-id="859e1-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="859e1-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="859e1-121">-InstanceName</span></span>
<span data-ttu-id="859e1-122">Der Instanzname der zu filternden Marketplaces.</span><span class="sxs-lookup"><span data-stu-id="859e1-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="859e1-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="859e1-123">-ResourceGroup</span></span>
<span data-ttu-id="859e1-124">Die Ressourcengruppe der zu filternden Marketplaces.</span><span class="sxs-lookup"><span data-stu-id="859e1-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="859e1-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="859e1-125">-StartDate</span></span>
<span data-ttu-id="859e1-126">Das Startdatum (in UTC) der zu filternden Marketplaces.</span><span class="sxs-lookup"><span data-stu-id="859e1-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="859e1-127">-Top</span><span class="sxs-lookup"><span data-stu-id="859e1-127">-Top</span></span>
<span data-ttu-id="859e1-128">Ermitteln Sie die maximale Anzahl von Zurücksenddatensätzen.</span><span class="sxs-lookup"><span data-stu-id="859e1-128">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859e1-129">CommonParameters</span></span>
<span data-ttu-id="859e1-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859e1-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859e1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859e1-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="859e1-132">INPUTS</span></span>

### <span data-ttu-id="859e1-133">Keine</span><span class="sxs-lookup"><span data-stu-id="859e1-133">None</span></span>

## <span data-ttu-id="859e1-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="859e1-134">OUTPUTS</span></span>

### <span data-ttu-id="859e1-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="859e1-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="859e1-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="859e1-136">NOTES</span></span>

## <span data-ttu-id="859e1-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="859e1-137">RELATED LINKS</span></span>
