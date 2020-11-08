---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166467"
---
# <span data-ttu-id="d13e7-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="d13e7-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="d13e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d13e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d13e7-103">Ruft die verfügbaren SKUs für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d13e7-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="d13e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d13e7-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d13e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d13e7-105">DESCRIPTION</span></span>
<span data-ttu-id="d13e7-106">Das Cmdlet " **Get-AzCognitiveServicesAccountSku** " Ruft die verfügbaren SKUs für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d13e7-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="d13e7-107">Die SKU ist der Stufenplan für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="d13e7-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="d13e7-108">Sie definiert den Preis, die Anruf Grenze und den Tarif für das Konto.</span><span class="sxs-lookup"><span data-stu-id="d13e7-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="d13e7-109">Die F0-SKU ist eine ﻿kostenlose Stufe.</span><span class="sxs-lookup"><span data-stu-id="d13e7-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="d13e7-110">Zu den bezahlten Ebenen gehören S0, S1, S2 usw.</span><span class="sxs-lookup"><span data-stu-id="d13e7-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="d13e7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d13e7-111">EXAMPLES</span></span>

### <span data-ttu-id="d13e7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d13e7-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="d13e7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d13e7-113">PARAMETERS</span></span>

### <span data-ttu-id="d13e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13e7-114">-DefaultProfile</span></span>
<span data-ttu-id="d13e7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d13e7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d13e7-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="d13e7-116">-Location</span></span>
<span data-ttu-id="d13e7-117">Standort des kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="d13e7-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e7-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="d13e7-118">-Type</span></span>
<span data-ttu-id="d13e7-119">Typ des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="d13e7-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13e7-120">CommonParameters</span></span>
<span data-ttu-id="d13e7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d13e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13e7-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d13e7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13e7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d13e7-123">INPUTS</span></span>

### <span data-ttu-id="d13e7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d13e7-124">System.String</span></span>

## <span data-ttu-id="d13e7-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d13e7-125">OUTPUTS</span></span>

### <span data-ttu-id="d13e7-126">Microsoft. Azure. Management. CognitiveServices. Models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="d13e7-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="d13e7-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d13e7-127">NOTES</span></span>

## <span data-ttu-id="d13e7-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d13e7-128">RELATED LINKS</span></span>
