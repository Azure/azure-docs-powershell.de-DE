---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665095"
---
# <span data-ttu-id="45ac7-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="45ac7-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="45ac7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="45ac7-103">Rufen Sie die Nutzungsdetails des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="45ac7-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45ac7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45ac7-104">SYNTAX</span></span>

### <span data-ttu-id="45ac7-105">Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="45ac7-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45ac7-106">Rechnung</span><span class="sxs-lookup"><span data-stu-id="45ac7-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45ac7-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="45ac7-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45ac7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45ac7-108">DESCRIPTION</span></span>
<span data-ttu-id="45ac7-109">Das Cmdlet " **Get-AzureRmConsumptionUsageDetail** " ruft Nutzungsdetails des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="45ac7-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="45ac7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45ac7-110">EXAMPLES</span></span>

### <span data-ttu-id="45ac7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45ac7-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="45ac7-112">Rufen Sie die Nutzungsdetails der Rechnung mit dem angegebenen Namen ab, und schließen Sie die MeterDetails-Eigenschaft in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="45ac7-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="45ac7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="45ac7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="45ac7-114">Rufen Sie die Nutzungsdetails des Abrechnungszeitraums mit dem angegebenen Namen ab, und schließen Sie die AdditionalProperties-Eigenschaft in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="45ac7-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="45ac7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="45ac7-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="45ac7-116">Rufen Sie die Nutzungsdetails des Abonnements ab, die zwischen 2017-01-17 und 2017-01-19 liegen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="45ac7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="45ac7-117">PARAMETERS</span></span>

### <span data-ttu-id="45ac7-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="45ac7-118">-BillingPeriodName</span></span>
<span data-ttu-id="45ac7-119">Name eines bestimmten Abrechnungszeitraums, um die Nutzungsdetails abzurufen, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ac7-120">-Enddate</span><span class="sxs-lookup"><span data-stu-id="45ac7-120">-EndDate</span></span>
<span data-ttu-id="45ac7-121">Das Enddatum (in UTC) der Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-121">The end date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="45ac7-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="45ac7-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="45ac7-123">Fügen Sie zusätzliche Eigenschaften in die Verwendungen ein.</span><span class="sxs-lookup"><span data-stu-id="45ac7-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="45ac7-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="45ac7-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="45ac7-125">Fügen Sie die Zähler Details in die Verwendung ein.</span><span class="sxs-lookup"><span data-stu-id="45ac7-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="45ac7-126">-Invoicename</span><span class="sxs-lookup"><span data-stu-id="45ac7-126">-InvoiceName</span></span>
<span data-ttu-id="45ac7-127">Der Name einer bestimmten Rechnung, um die Nutzungsdetails abzurufen, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ac7-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="45ac7-128">-MaxCount</span></span>
<span data-ttu-id="45ac7-129">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="45ac7-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="45ac7-130">-StartDate</span></span>
<span data-ttu-id="45ac7-131">Das Startdatum (in UTC) der Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="45ac7-131">The start date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="45ac7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ac7-132">-DefaultProfile</span></span>
<span data-ttu-id="45ac7-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45ac7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45ac7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ac7-134">CommonParameters</span></span>
<span data-ttu-id="45ac7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ac7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ac7-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ac7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ac7-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45ac7-137">INPUTS</span></span>

### <span data-ttu-id="45ac7-138">Keine</span><span class="sxs-lookup"><span data-stu-id="45ac7-138">None</span></span>

## <span data-ttu-id="45ac7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45ac7-139">OUTPUTS</span></span>

### <span data-ttu-id="45ac7-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Verbrauch. Models. PSUsageDetail, Microsoft. Azure. Commands. Verbrauch, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="45ac7-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="45ac7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="45ac7-141">NOTES</span></span>

## <span data-ttu-id="45ac7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45ac7-142">RELATED LINKS</span></span>

