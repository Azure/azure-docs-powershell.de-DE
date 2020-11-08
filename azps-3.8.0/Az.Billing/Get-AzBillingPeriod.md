---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997121"
---
# <span data-ttu-id="ad51c-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ad51c-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="ad51c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad51c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad51c-103">Besorgen Sie sich Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ad51c-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="ad51c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad51c-104">SYNTAX</span></span>

### <span data-ttu-id="ad51c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad51c-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad51c-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="ad51c-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad51c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad51c-107">DESCRIPTION</span></span>
<span data-ttu-id="ad51c-108">Das Cmdlet " **Get-AzBillingPeriod** " ruft Abrechnungsperioden des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="ad51c-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="ad51c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad51c-109">EXAMPLES</span></span>

### <span data-ttu-id="ad51c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad51c-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="ad51c-111">Abrufen aller verfügbaren Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ad51c-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="ad51c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad51c-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="ad51c-113">Abrufen des Abrechnungszeitraums des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="ad51c-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="ad51c-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ad51c-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="ad51c-115">Erhalten Sie höchstens zwei Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ad51c-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="ad51c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad51c-116">PARAMETERS</span></span>

### <span data-ttu-id="ad51c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad51c-117">-DefaultProfile</span></span>
<span data-ttu-id="ad51c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ad51c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad51c-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ad51c-119">-MaxCount</span></span>
<span data-ttu-id="ad51c-120">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad51c-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="ad51c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ad51c-121">-Name</span></span>
<span data-ttu-id="ad51c-122">Der Name eines bestimmten Abrechnungszeitraums, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad51c-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="ad51c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad51c-123">CommonParameters</span></span>
<span data-ttu-id="ad51c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad51c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad51c-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad51c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad51c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad51c-126">INPUTS</span></span>

### <span data-ttu-id="ad51c-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ad51c-127">None</span></span>

## <span data-ttu-id="ad51c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad51c-128">OUTPUTS</span></span>

### <span data-ttu-id="ad51c-129">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ad51c-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="ad51c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad51c-130">NOTES</span></span>

## <span data-ttu-id="ad51c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad51c-131">RELATED LINKS</span></span>
