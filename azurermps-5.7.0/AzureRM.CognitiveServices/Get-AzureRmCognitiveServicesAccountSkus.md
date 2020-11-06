---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478646"
---
# <span data-ttu-id="e2205-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e2205-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="e2205-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2205-102">SYNOPSIS</span></span>
<span data-ttu-id="e2205-103">Ruft die verfügbaren SKUs für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="e2205-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2205-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2205-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2205-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2205-105">DESCRIPTION</span></span>
<span data-ttu-id="e2205-106">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountSkus** " Ruft die verfügbaren SKUs für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="e2205-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="e2205-107">Die SKU ist der Stufenplan für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="e2205-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="e2205-108">Sie definiert den Preis, die Anruf Grenze und den Tarif für das Konto.</span><span class="sxs-lookup"><span data-stu-id="e2205-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="e2205-109">Die F0-SKU ist eine ﻿kostenlose Stufe.</span><span class="sxs-lookup"><span data-stu-id="e2205-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="e2205-110">Zu den bezahlten Ebenen gehören S0, S1, S2 usw.</span><span class="sxs-lookup"><span data-stu-id="e2205-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="e2205-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2205-111">EXAMPLES</span></span>

## <span data-ttu-id="e2205-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2205-112">PARAMETERS</span></span>

### <span data-ttu-id="e2205-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2205-113">-DefaultProfile</span></span>
<span data-ttu-id="e2205-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e2205-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2205-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e2205-115">-Name</span></span>
<span data-ttu-id="e2205-116">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e2205-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2205-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2205-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2205-118">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e2205-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2205-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2205-119">CommonParameters</span></span>
<span data-ttu-id="e2205-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2205-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2205-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2205-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2205-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2205-122">INPUTS</span></span>

### <span data-ttu-id="e2205-123">Keine</span><span class="sxs-lookup"><span data-stu-id="e2205-123">None</span></span>
<span data-ttu-id="e2205-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e2205-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2205-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2205-125">OUTPUTS</span></span>

### <span data-ttu-id="e2205-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="e2205-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="e2205-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2205-127">NOTES</span></span>

## <span data-ttu-id="e2205-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2205-128">RELATED LINKS</span></span>

