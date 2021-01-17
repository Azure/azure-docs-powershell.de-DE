---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473269"
---
# <span data-ttu-id="29107-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="29107-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="29107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29107-102">SYNOPSIS</span></span>
<span data-ttu-id="29107-103">Erhalten Sie Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="29107-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="29107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29107-104">SYNTAX</span></span>

### <span data-ttu-id="29107-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="29107-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29107-106">Single</span><span class="sxs-lookup"><span data-stu-id="29107-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29107-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29107-107">DESCRIPTION</span></span>
<span data-ttu-id="29107-108">Das **Get-AzBillingPeriod-Cmdlet** ruft Abrechnungszeiträume des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="29107-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="29107-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29107-109">EXAMPLES</span></span>

### <span data-ttu-id="29107-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29107-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="29107-111">Erhalten Sie alle verfügbaren Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="29107-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="29107-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="29107-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="29107-113">Holen Sie sich den Abrechnungszeitraum des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="29107-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="29107-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="29107-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="29107-115">Sie erhalten mindestens zwei Abrechnungszeiträume des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="29107-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="29107-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29107-116">PARAMETERS</span></span>

### <span data-ttu-id="29107-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29107-117">-DefaultProfile</span></span>
<span data-ttu-id="29107-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="29107-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29107-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="29107-119">-MaxCount</span></span>
<span data-ttu-id="29107-120">Ermitteln Sie die maximale Anzahl von Zurücksenddatensätzen.</span><span class="sxs-lookup"><span data-stu-id="29107-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="29107-121">-Name</span><span class="sxs-lookup"><span data-stu-id="29107-121">-Name</span></span>
<span data-ttu-id="29107-122">Name eines bestimmten Abrechnungszeitraums.</span><span class="sxs-lookup"><span data-stu-id="29107-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="29107-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29107-123">CommonParameters</span></span>
<span data-ttu-id="29107-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29107-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29107-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29107-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29107-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29107-126">INPUTS</span></span>

### <span data-ttu-id="29107-127">Keine</span><span class="sxs-lookup"><span data-stu-id="29107-127">None</span></span>

## <span data-ttu-id="29107-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29107-128">OUTPUTS</span></span>

### <span data-ttu-id="29107-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="29107-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="29107-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29107-130">NOTES</span></span>

## <span data-ttu-id="29107-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29107-131">RELATED LINKS</span></span>
