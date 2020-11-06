---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionMarketplace.md
ms.openlocfilehash: 7ac3a179139a9e196b81d3ae323e665f793f4702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480410"
---
# <span data-ttu-id="534e7-101">Get-AzureRmConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="534e7-101">Get-AzureRmConsumptionMarketplace</span></span>

## <span data-ttu-id="534e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="534e7-102">SYNOPSIS</span></span>
<span data-ttu-id="534e7-103">Erhalten Sie Marktplätze des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="534e7-103">Get marketplaces of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="534e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="534e7-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="534e7-105">DESCRIPTION</span></span>
<span data-ttu-id="534e7-106">Das Cmdlet " **Get-AzureRmConsumptionMarketplace** " ruft Marktplätze des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="534e7-106">The **Get-AzureRmConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="534e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="534e7-107">EXAMPLES</span></span>

### <span data-ttu-id="534e7-108">Beispiel 1: Abrufen der Marktplatz Nutzung</span><span class="sxs-lookup"><span data-stu-id="534e7-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -Top 10
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

### <span data-ttu-id="534e7-109">Beispiel 2: Abrufen der Marketplace-Nutzung mit dem Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="534e7-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
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

### <span data-ttu-id="534e7-110">Beispiel 3: Abrufen der Marketplace-Nutzung von BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="534e7-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
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

### <span data-ttu-id="534e7-111">Beispiel 4: Abrufen der Marktplatz Nutzung mit instanceName-Filter</span><span class="sxs-lookup"><span data-stu-id="534e7-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -InstanceName TestVM -Top 10
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

## <span data-ttu-id="534e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="534e7-112">PARAMETERS</span></span>

### <span data-ttu-id="534e7-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="534e7-113">-BillingPeriodName</span></span>
<span data-ttu-id="534e7-114">Name eines bestimmten Abrechnungszeitraums, um den Marktplatz zu erhalten, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="534e7-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="534e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534e7-115">-DefaultProfile</span></span>
<span data-ttu-id="534e7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="534e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534e7-117">-Enddate</span><span class="sxs-lookup"><span data-stu-id="534e7-117">-EndDate</span></span>
<span data-ttu-id="534e7-118">Das Enddatum (in UTC) der zu filternden Marktplätze.</span><span class="sxs-lookup"><span data-stu-id="534e7-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="534e7-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="534e7-119">-InstanceId</span></span>
<span data-ttu-id="534e7-120">Die Instanz-ID der zu filternden Marktplätze.</span><span class="sxs-lookup"><span data-stu-id="534e7-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="534e7-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="534e7-121">-InstanceName</span></span>
<span data-ttu-id="534e7-122">Der Instanzname der zu filternden Marktplätze.</span><span class="sxs-lookup"><span data-stu-id="534e7-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="534e7-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="534e7-123">-ResourceGroup</span></span>
<span data-ttu-id="534e7-124">Die Ressourcengruppe der zu filternden Marktplätze.</span><span class="sxs-lookup"><span data-stu-id="534e7-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="534e7-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="534e7-125">-StartDate</span></span>
<span data-ttu-id="534e7-126">Das Startdatum (in UTC) der zu filternden Marktplätze.</span><span class="sxs-lookup"><span data-stu-id="534e7-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="534e7-127">-Top</span><span class="sxs-lookup"><span data-stu-id="534e7-127">-Top</span></span>
<span data-ttu-id="534e7-128">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="534e7-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="534e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534e7-129">CommonParameters</span></span>
<span data-ttu-id="534e7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534e7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534e7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="534e7-132">INPUTS</span></span>

### <span data-ttu-id="534e7-133">Keine</span><span class="sxs-lookup"><span data-stu-id="534e7-133">None</span></span>

## <span data-ttu-id="534e7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="534e7-134">OUTPUTS</span></span>

### <span data-ttu-id="534e7-135">Microsoft. Azure. Commands. Verbrauch. Models. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="534e7-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="534e7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="534e7-136">NOTES</span></span>

## <span data-ttu-id="534e7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="534e7-137">RELATED LINKS</span></span>
