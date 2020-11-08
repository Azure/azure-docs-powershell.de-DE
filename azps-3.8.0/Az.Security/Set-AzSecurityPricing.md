---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003961"
---
# <span data-ttu-id="122b6-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="122b6-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="122b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="122b6-102">SYNOPSIS</span></span>
<span data-ttu-id="122b6-103">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="122b6-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="122b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="122b6-104">SYNTAX</span></span>

### <span data-ttu-id="122b6-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="122b6-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="122b6-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122b6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="122b6-107">DESCRIPTION</span></span>
<span data-ttu-id="122b6-108">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="122b6-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="122b6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="122b6-109">EXAMPLES</span></span>

### <span data-ttu-id="122b6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="122b6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="122b6-111">Legt die Preisstufe für das Abonnement Azure Security Center auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="122b6-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="122b6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="122b6-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="122b6-113">Legt die "myService1"-Ressourcengruppe Azure Security Center-Preisstufe auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="122b6-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="122b6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="122b6-114">PARAMETERS</span></span>

### <span data-ttu-id="122b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122b6-115">-DefaultProfile</span></span>
<span data-ttu-id="122b6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="122b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="122b6-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="122b6-117">-InputObject</span></span>
<span data-ttu-id="122b6-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="122b6-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="122b6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="122b6-119">-Name</span></span>
<span data-ttu-id="122b6-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="122b6-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122b6-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="122b6-121">-PricingTier</span></span>
<span data-ttu-id="122b6-122">Preisklasse.</span><span class="sxs-lookup"><span data-stu-id="122b6-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122b6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="122b6-123">-Confirm</span></span>
<span data-ttu-id="122b6-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="122b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122b6-125">-WhatIf</span></span>
<span data-ttu-id="122b6-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="122b6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="122b6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="122b6-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122b6-128">CommonParameters</span></span>
<span data-ttu-id="122b6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122b6-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122b6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122b6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="122b6-131">INPUTS</span></span>

### <span data-ttu-id="122b6-132">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="122b6-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="122b6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="122b6-133">OUTPUTS</span></span>

### <span data-ttu-id="122b6-134">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="122b6-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="122b6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="122b6-135">NOTES</span></span>

## <span data-ttu-id="122b6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="122b6-136">RELATED LINKS</span></span>
