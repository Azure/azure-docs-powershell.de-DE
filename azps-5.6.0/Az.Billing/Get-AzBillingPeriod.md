---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938275"
---
# <span data-ttu-id="e2de3-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="e2de3-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="e2de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2de3-102">SYNOPSIS</span></span>
<span data-ttu-id="e2de3-103">Erhalten Sie Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e2de3-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="e2de3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2de3-104">SYNTAX</span></span>

### <span data-ttu-id="e2de3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2de3-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2de3-106">Single</span><span class="sxs-lookup"><span data-stu-id="e2de3-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2de3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2de3-107">DESCRIPTION</span></span>
<span data-ttu-id="e2de3-108">Das **Get-AzBillingPeriod-Cmdlet** erhält Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e2de3-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="e2de3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2de3-109">EXAMPLES</span></span>

### <span data-ttu-id="e2de3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2de3-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="e2de3-111">Alle verfügbaren Abrechnungszeiträume des Abonnements erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2de3-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="e2de3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2de3-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="e2de3-113">Holen Sie sich den Abrechnungszeitraum des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="e2de3-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="e2de3-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e2de3-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="e2de3-115">Erhalten Sie mindestens zwei Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e2de3-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="e2de3-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e2de3-116">PARAMETERS</span></span>

### <span data-ttu-id="e2de3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2de3-117">-DefaultProfile</span></span>
<span data-ttu-id="e2de3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e2de3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2de3-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e2de3-119">-MaxCount</span></span>
<span data-ttu-id="e2de3-120">Bestimmen Sie die maximale Anzahl von Datensätzen, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e2de3-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2de3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2de3-121">-Name</span></span>
<span data-ttu-id="e2de3-122">Name eines bestimmten Abrechnungszeitraums.</span><span class="sxs-lookup"><span data-stu-id="e2de3-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2de3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2de3-123">CommonParameters</span></span>
<span data-ttu-id="e2de3-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2de3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2de3-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2de3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2de3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2de3-126">INPUTS</span></span>

### <span data-ttu-id="e2de3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="e2de3-127">None</span></span>

## <span data-ttu-id="e2de3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2de3-128">OUTPUTS</span></span>

### <span data-ttu-id="e2de3-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="e2de3-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="e2de3-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e2de3-130">NOTES</span></span>

## <span data-ttu-id="e2de3-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e2de3-131">RELATED LINKS</span></span>
