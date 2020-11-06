---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503878"
---
# <span data-ttu-id="5a020-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5a020-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="5a020-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a020-102">SYNOPSIS</span></span>
<span data-ttu-id="5a020-103">Besorgen Sie sich Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5a020-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a020-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a020-104">SYNTAX</span></span>

### <span data-ttu-id="5a020-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a020-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a020-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="5a020-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a020-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a020-107">DESCRIPTION</span></span>
<span data-ttu-id="5a020-108">Das Cmdlet " **Get-AzureRmBillingPeriod** " ruft Abrechnungsperioden des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="5a020-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="5a020-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a020-109">EXAMPLES</span></span>

### <span data-ttu-id="5a020-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a020-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="5a020-111">Abrufen aller verfügbaren Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5a020-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="5a020-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a020-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="5a020-113">Abrufen des Abrechnungszeitraums des Abonnements mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="5a020-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="5a020-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5a020-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="5a020-115">Erhalten Sie höchstens zwei Abrechnungsperioden des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5a020-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="5a020-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a020-116">PARAMETERS</span></span>

### <span data-ttu-id="5a020-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a020-117">-DefaultProfile</span></span>
<span data-ttu-id="5a020-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5a020-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a020-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5a020-119">-MaxCount</span></span>
<span data-ttu-id="5a020-120">Ermitteln Sie die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a020-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a020-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a020-121">-Name</span></span>
<span data-ttu-id="5a020-122">Der Name eines bestimmten Abrechnungszeitraums, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a020-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="5a020-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a020-123">CommonParameters</span></span>
<span data-ttu-id="5a020-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a020-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a020-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a020-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a020-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a020-126">INPUTS</span></span>

### <span data-ttu-id="5a020-127">Keine</span><span class="sxs-lookup"><span data-stu-id="5a020-127">None</span></span>

## <span data-ttu-id="5a020-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a020-128">OUTPUTS</span></span>

### <span data-ttu-id="5a020-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Abrechnungs. Models. PSBillingPeriod; Microsoft. Azure. Commands. Billing; Version = 0.14.0.0; Kultur = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5a020-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5a020-130">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5a020-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5a020-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a020-131">NOTES</span></span>

## <span data-ttu-id="5a020-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a020-132">RELATED LINKS</span></span>

