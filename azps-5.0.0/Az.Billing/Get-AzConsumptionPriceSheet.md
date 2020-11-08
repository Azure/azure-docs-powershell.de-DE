---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176322"
---
# <span data-ttu-id="4e87c-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="4e87c-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="4e87c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e87c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e87c-103">Rufen Sie die Preisblätter des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="4e87c-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="4e87c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e87c-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e87c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e87c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e87c-106">Das Cmdlet " **Get-AzConsumptionPriceSheet** " ruft Preisblätter des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="4e87c-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="4e87c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e87c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e87c-108">Beispiel 1: Abrufen von Preisblättern</span><span class="sxs-lookup"><span data-stu-id="4e87c-108">Example 1: Get price sheets</span></span>
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

### <span data-ttu-id="4e87c-109">Beispiel 2: Abrufen von Preisblättern mit Expand von MeterDetails</span><span class="sxs-lookup"><span data-stu-id="4e87c-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
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

### <span data-ttu-id="4e87c-110">Beispiel 3: Abrufen von Preisblättern von BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="4e87c-110">Example 3: Get price sheets of BillingPeriodName</span></span>
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

### <span data-ttu-id="4e87c-111">Beispiel 4: Abrufen der Top 5-Datensätze der Preisblätter</span><span class="sxs-lookup"><span data-stu-id="4e87c-111">Example 4: Get top 5 records of price sheets</span></span>
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

## <span data-ttu-id="4e87c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e87c-112">PARAMETERS</span></span>

### <span data-ttu-id="4e87c-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="4e87c-113">-BillingPeriodName</span></span>
<span data-ttu-id="4e87c-114">Name eines bestimmten Abrechnungszeitraums, um die Preisblätter abzurufen, die dem zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4e87c-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="4e87c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e87c-115">-DefaultProfile</span></span>
<span data-ttu-id="4e87c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e87c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e87c-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="4e87c-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="4e87c-118">Erweitern Sie die Preisblätter auf Grundlage von MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="4e87c-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="4e87c-119">-Top</span><span class="sxs-lookup"><span data-stu-id="4e87c-119">-Top</span></span>
<span data-ttu-id="4e87c-120">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e87c-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="4e87c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e87c-121">CommonParameters</span></span>
<span data-ttu-id="4e87c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e87c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e87c-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e87c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e87c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e87c-124">INPUTS</span></span>

### <span data-ttu-id="4e87c-125">Keine</span><span class="sxs-lookup"><span data-stu-id="4e87c-125">None</span></span>

## <span data-ttu-id="4e87c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e87c-126">OUTPUTS</span></span>

### <span data-ttu-id="4e87c-127">Microsoft. Azure. Commands. Verbrauch. Models. PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="4e87c-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="4e87c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e87c-128">NOTES</span></span>

## <span data-ttu-id="4e87c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e87c-129">RELATED LINKS</span></span>
