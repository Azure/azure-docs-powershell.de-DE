---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500254"
---
# <span data-ttu-id="02236-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="02236-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="02236-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02236-102">SYNOPSIS</span></span>
<span data-ttu-id="02236-103">Ruft die verfügbaren SKUs für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="02236-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02236-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02236-104">SYNTAX</span></span>

### <span data-ttu-id="02236-105">GetSkusWithAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="02236-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02236-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="02236-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02236-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02236-107">DESCRIPTION</span></span>
<span data-ttu-id="02236-108">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountSkus** " Ruft die verfügbaren SKUs für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="02236-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="02236-109">Die SKU ist der Stufenplan für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="02236-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="02236-110">Sie definiert den Preis, die Anruf Grenze und den Tarif für das Konto.</span><span class="sxs-lookup"><span data-stu-id="02236-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="02236-111">Die F0-SKU ist eine ﻿kostenlose Stufe.</span><span class="sxs-lookup"><span data-stu-id="02236-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="02236-112">Zu den bezahlten Ebenen gehören S0, S1, S2 usw.</span><span class="sxs-lookup"><span data-stu-id="02236-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="02236-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02236-113">EXAMPLES</span></span>

### <span data-ttu-id="02236-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02236-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="02236-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="02236-115">PARAMETERS</span></span>

### <span data-ttu-id="02236-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02236-116">-DefaultProfile</span></span>
<span data-ttu-id="02236-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="02236-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02236-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="02236-118">-Location</span></span>
<span data-ttu-id="02236-119">Standort des kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="02236-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02236-120">-Name</span><span class="sxs-lookup"><span data-stu-id="02236-120">-Name</span></span>
<span data-ttu-id="02236-121">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="02236-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02236-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02236-122">-ResourceGroupName</span></span>
<span data-ttu-id="02236-123">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02236-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02236-124">-Typ</span><span class="sxs-lookup"><span data-stu-id="02236-124">-Type</span></span>
<span data-ttu-id="02236-125">Typ des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="02236-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02236-126">CommonParameters</span></span>
<span data-ttu-id="02236-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02236-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02236-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02236-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02236-129">INPUTS</span></span>

### <span data-ttu-id="02236-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02236-130">System.String</span></span>

## <span data-ttu-id="02236-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02236-131">OUTPUTS</span></span>

### <span data-ttu-id="02236-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="02236-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="02236-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="02236-133">NOTES</span></span>

## <span data-ttu-id="02236-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02236-134">RELATED LINKS</span></span>
