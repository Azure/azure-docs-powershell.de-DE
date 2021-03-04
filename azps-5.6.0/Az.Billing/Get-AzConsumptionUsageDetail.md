---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 4c355565936a7aefc8d0adc9b9ee865a2414e880
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919032"
---
# <span data-ttu-id="eb031-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="eb031-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="eb031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb031-102">SYNOPSIS</span></span>
<span data-ttu-id="eb031-103">Hier erhalten Sie Nutzungsdetails des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="eb031-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="eb031-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb031-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb031-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb031-105">DESCRIPTION</span></span>
<span data-ttu-id="eb031-106">Das **Get-AzConsumptionUsageDetail-Cmdlet** ruft Nutzungsdetails des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="eb031-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="eb031-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb031-107">EXAMPLES</span></span>

### <span data-ttu-id="eb031-108">Beispiel 1: Anzeigen von Nutzungsdetails mit erweitern von MeterDetails</span><span class="sxs-lookup"><span data-stu-id="eb031-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="eb031-109">Beispiel 2: Anzeigen von Nutzungsdetails mit Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="eb031-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="eb031-110">Beispiel 3: Anzeigen von Nutzungsdetails von BillingPeriodName mit InstanceName-Filter</span><span class="sxs-lookup"><span data-stu-id="eb031-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="eb031-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb031-111">PARAMETERS</span></span>

### <span data-ttu-id="eb031-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="eb031-112">-BillingPeriodName</span></span>
<span data-ttu-id="eb031-113">Name eines bestimmten Abrechnungszeitraums, um die Nutzungsdetails zu erhalten, die zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eb031-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="eb031-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb031-114">-DefaultProfile</span></span>
<span data-ttu-id="eb031-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb031-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb031-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="eb031-116">-EndDate</span></span>
<span data-ttu-id="eb031-117">Das Enddatum (in UTC) der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-118">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="eb031-118">-Expand</span></span>
<span data-ttu-id="eb031-119">Erweitern Sie die Verwendungen basierend auf MeterDetails oder AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="eb031-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="eb031-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="eb031-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="eb031-121">Fügen Sie zusätzliche Eigenschaften in die Verwendungen ein.</span><span class="sxs-lookup"><span data-stu-id="eb031-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="eb031-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="eb031-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="eb031-123">Fügen Sie Zählerdetails in die Verwendungen ein.</span><span class="sxs-lookup"><span data-stu-id="eb031-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="eb031-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eb031-124">-InstanceId</span></span>
<span data-ttu-id="eb031-125">Die Instanz-ID der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eb031-126">-InstanceName</span></span>
<span data-ttu-id="eb031-127">Der Instanzname der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eb031-128">-MaxCount</span></span>
<span data-ttu-id="eb031-129">Bestimmen Sie die maximale Anzahl von Datensätzen, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb031-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eb031-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb031-130">-ResourceGroup</span></span>
<span data-ttu-id="eb031-131">Die Ressourcengruppe der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="eb031-132">-StartDate</span></span>
<span data-ttu-id="eb031-133">Das Startdatum (in UTC) der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb031-134">-Tag</span></span>
<span data-ttu-id="eb031-135">Das Tag der zu filternden Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb031-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="eb031-136">-Top</span><span class="sxs-lookup"><span data-stu-id="eb031-136">-Top</span></span>
<span data-ttu-id="eb031-137">Bestimmen Sie die maximale Anzahl von Datensätzen, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb031-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eb031-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb031-138">CommonParameters</span></span>
<span data-ttu-id="eb031-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb031-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb031-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb031-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb031-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb031-141">INPUTS</span></span>

### <span data-ttu-id="eb031-142">Keine</span><span class="sxs-lookup"><span data-stu-id="eb031-142">None</span></span>

## <span data-ttu-id="eb031-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb031-143">OUTPUTS</span></span>

### <span data-ttu-id="eb031-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="eb031-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="eb031-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb031-145">NOTES</span></span>

## <span data-ttu-id="eb031-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb031-146">RELATED LINKS</span></span>
