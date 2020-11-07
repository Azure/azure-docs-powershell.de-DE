---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: a52ae3b59cc7cbf99bf7f4751a36f271bc9610de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823300"
---
# <span data-ttu-id="9de42-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9de42-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="9de42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9de42-102">SYNOPSIS</span></span>
<span data-ttu-id="9de42-103">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="9de42-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9de42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de42-104">SYNTAX</span></span>

### <span data-ttu-id="9de42-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9de42-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de42-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9de42-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de42-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9de42-107">DESCRIPTION</span></span>
<span data-ttu-id="9de42-108">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="9de42-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9de42-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9de42-109">EXAMPLES</span></span>

### <span data-ttu-id="9de42-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9de42-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="9de42-111">Legt die Preisstufe für das Abonnement Azure Security Center auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="9de42-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="9de42-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9de42-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="9de42-113">Legt die "myService1"-Ressourcengruppe Azure Security Center-Preisstufe auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="9de42-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="9de42-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de42-114">PARAMETERS</span></span>

### <span data-ttu-id="9de42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de42-115">-DefaultProfile</span></span>
<span data-ttu-id="9de42-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9de42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de42-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9de42-117">-InputObject</span></span>
<span data-ttu-id="9de42-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="9de42-118">Input Object.</span></span>

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

### <span data-ttu-id="9de42-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9de42-119">-Name</span></span>
<span data-ttu-id="9de42-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="9de42-120">Resource name.</span></span>

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

### <span data-ttu-id="9de42-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="9de42-121">-PricingTier</span></span>
<span data-ttu-id="9de42-122">Preisklasse.</span><span class="sxs-lookup"><span data-stu-id="9de42-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="9de42-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9de42-123">-Confirm</span></span>
<span data-ttu-id="9de42-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9de42-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de42-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de42-125">-WhatIf</span></span>
<span data-ttu-id="9de42-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9de42-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9de42-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9de42-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de42-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de42-128">CommonParameters</span></span>
<span data-ttu-id="9de42-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de42-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de42-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de42-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de42-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9de42-131">INPUTS</span></span>

### <span data-ttu-id="9de42-132">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9de42-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9de42-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9de42-133">OUTPUTS</span></span>

### <span data-ttu-id="9de42-134">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9de42-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9de42-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9de42-135">NOTES</span></span>

## <span data-ttu-id="9de42-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9de42-136">RELATED LINKS</span></span>
