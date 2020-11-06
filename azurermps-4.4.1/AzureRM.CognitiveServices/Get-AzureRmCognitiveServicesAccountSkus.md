---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497825"
---
# <span data-ttu-id="58f08-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="58f08-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="58f08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58f08-102">SYNOPSIS</span></span>
<span data-ttu-id="58f08-103">Ruft die verfügbaren SKUs für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="58f08-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58f08-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f08-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58f08-105">DESCRIPTION</span></span>
<span data-ttu-id="58f08-106">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountSkus** " Ruft die verfügbaren SKUs für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="58f08-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="58f08-107">Die SKU ist der Stufenplan für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="58f08-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="58f08-108">Sie definiert den Preis, die Anruf Grenze und den Tarif für das Konto.</span><span class="sxs-lookup"><span data-stu-id="58f08-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="58f08-109">Die F0-SKU ist eine ﻿kostenlose Stufe.</span><span class="sxs-lookup"><span data-stu-id="58f08-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="58f08-110">Zu den bezahlten Ebenen gehören S0, S1, S2 usw.</span><span class="sxs-lookup"><span data-stu-id="58f08-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="58f08-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58f08-111">EXAMPLES</span></span>

## <span data-ttu-id="58f08-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="58f08-112">PARAMETERS</span></span>

### <span data-ttu-id="58f08-113">-Name</span><span class="sxs-lookup"><span data-stu-id="58f08-113">-Name</span></span>
<span data-ttu-id="58f08-114">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="58f08-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f08-115">-ResourceGroupName</span></span>
<span data-ttu-id="58f08-116">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58f08-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f08-117">-DefaultProfile</span></span>
<span data-ttu-id="58f08-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58f08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f08-119">CommonParameters</span></span>
<span data-ttu-id="58f08-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f08-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f08-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f08-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58f08-122">INPUTS</span></span>

## <span data-ttu-id="58f08-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58f08-123">OUTPUTS</span></span>

### <span data-ttu-id="58f08-124">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="58f08-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="58f08-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="58f08-125">NOTES</span></span>

## <span data-ttu-id="58f08-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58f08-126">RELATED LINKS</span></span>

