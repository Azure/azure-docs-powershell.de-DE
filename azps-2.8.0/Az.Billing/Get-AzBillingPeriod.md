---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: b4e85f85d0e7b7724b2a09f3c78af03dfd489014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652377"
---
# <span data-ttu-id="90666-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="90666-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="90666-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90666-102">SYNOPSIS</span></span>
<span data-ttu-id="90666-103">Besorgen Sie sich Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="90666-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="90666-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90666-104">SYNTAX</span></span>

### <span data-ttu-id="90666-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="90666-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90666-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="90666-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90666-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90666-107">DESCRIPTION</span></span>
<span data-ttu-id="90666-108">Das Cmdlet " **Get-AzBillingPeriod** " ruft Abrechnungsperioden des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="90666-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="90666-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90666-109">EXAMPLES</span></span>

### <span data-ttu-id="90666-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90666-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="90666-111">Abrufen aller verfügbaren Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="90666-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="90666-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90666-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="90666-113">Abrufen des Abrechnungszeitraums des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="90666-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="90666-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="90666-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="90666-115">Erhalten Sie höchstens zwei Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="90666-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="90666-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="90666-116">PARAMETERS</span></span>

### <span data-ttu-id="90666-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90666-117">-DefaultProfile</span></span>
<span data-ttu-id="90666-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="90666-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90666-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="90666-119">-MaxCount</span></span>
<span data-ttu-id="90666-120">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="90666-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="90666-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90666-121">-Name</span></span>
<span data-ttu-id="90666-122">Der Name eines bestimmten Abrechnungszeitraums, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="90666-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="90666-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90666-123">CommonParameters</span></span>
<span data-ttu-id="90666-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90666-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90666-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90666-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90666-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90666-126">INPUTS</span></span>

### <span data-ttu-id="90666-127">Keine</span><span class="sxs-lookup"><span data-stu-id="90666-127">None</span></span>

## <span data-ttu-id="90666-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90666-128">OUTPUTS</span></span>

### <span data-ttu-id="90666-129">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="90666-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="90666-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="90666-130">NOTES</span></span>

## <span data-ttu-id="90666-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90666-131">RELATED LINKS</span></span>
