---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473261"
---
# <span data-ttu-id="db6ab-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="db6ab-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="db6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="db6ab-103">Erhalten Sie Preisblätter des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="db6ab-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="db6ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db6ab-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="db6ab-106">Das **Cmdlet "Get-AzConsumptionPriceSheet"** ruft Preisblätter des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="db6ab-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="db6ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="db6ab-108">Beispiel 1: Preisblätter erhalten</span><span class="sxs-lookup"><span data-stu-id="db6ab-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="db6ab-109">Beispiel 2: Erhalten von Preisblättern mit der Erweiterung "MeterDetails"</span><span class="sxs-lookup"><span data-stu-id="db6ab-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="db6ab-110">Beispiel 3: Preisblätter von BillingPeriodName erhalten</span><span class="sxs-lookup"><span data-stu-id="db6ab-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="db6ab-111">Beispiel 4: Erhalten der ersten fünf Datensätze von Preisblättern</span><span class="sxs-lookup"><span data-stu-id="db6ab-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="db6ab-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6ab-112">PARAMETERS</span></span>

### <span data-ttu-id="db6ab-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="db6ab-113">-BillingPeriodName</span></span>
<span data-ttu-id="db6ab-114">Name eines bestimmten Abrechnungszeitraums, um die Preisblätter zu erhalten, die zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db6ab-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="db6ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6ab-115">-DefaultProfile</span></span>
<span data-ttu-id="db6ab-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db6ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db6ab-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="db6ab-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="db6ab-118">Erweitern Sie die Preisblätter basierend auf "MeterDetails".</span><span class="sxs-lookup"><span data-stu-id="db6ab-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="db6ab-119">-Top</span><span class="sxs-lookup"><span data-stu-id="db6ab-119">-Top</span></span>
<span data-ttu-id="db6ab-120">Ermitteln Sie die maximale Anzahl von Zurücksenddatensätzen.</span><span class="sxs-lookup"><span data-stu-id="db6ab-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="db6ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6ab-121">CommonParameters</span></span>
<span data-ttu-id="db6ab-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6ab-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6ab-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6ab-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db6ab-124">INPUTS</span></span>

### <span data-ttu-id="db6ab-125">Keine</span><span class="sxs-lookup"><span data-stu-id="db6ab-125">None</span></span>

## <span data-ttu-id="db6ab-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db6ab-126">OUTPUTS</span></span>

### <span data-ttu-id="db6ab-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="db6ab-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="db6ab-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db6ab-128">NOTES</span></span>

## <span data-ttu-id="db6ab-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db6ab-129">RELATED LINKS</span></span>
