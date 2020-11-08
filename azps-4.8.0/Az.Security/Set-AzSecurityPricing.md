---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165579"
---
# <span data-ttu-id="0254b-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0254b-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="0254b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0254b-102">SYNOPSIS</span></span>
<span data-ttu-id="0254b-103">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="0254b-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="0254b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0254b-104">SYNTAX</span></span>

### <span data-ttu-id="0254b-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0254b-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0254b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0254b-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0254b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0254b-107">DESCRIPTION</span></span>
<span data-ttu-id="0254b-108">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="0254b-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="0254b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0254b-109">EXAMPLES</span></span>

### <span data-ttu-id="0254b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0254b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="0254b-111">Legt die Preisstufe für das Abonnement Azure Security Center auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="0254b-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="0254b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0254b-112">PARAMETERS</span></span>

### <span data-ttu-id="0254b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0254b-113">-DefaultProfile</span></span>
<span data-ttu-id="0254b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0254b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0254b-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0254b-115">-InputObject</span></span>
<span data-ttu-id="0254b-116">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="0254b-116">Input Object.</span></span>

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

### <span data-ttu-id="0254b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0254b-117">-Name</span></span>
<span data-ttu-id="0254b-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="0254b-118">Resource name.</span></span>

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

### <span data-ttu-id="0254b-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="0254b-119">-PricingTier</span></span>
<span data-ttu-id="0254b-120">Preisklasse.</span><span class="sxs-lookup"><span data-stu-id="0254b-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="0254b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0254b-121">-Confirm</span></span>
<span data-ttu-id="0254b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0254b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0254b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0254b-123">-WhatIf</span></span>
<span data-ttu-id="0254b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0254b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0254b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0254b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0254b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0254b-126">CommonParameters</span></span>
<span data-ttu-id="0254b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0254b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0254b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0254b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0254b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0254b-129">INPUTS</span></span>

### <span data-ttu-id="0254b-130">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0254b-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="0254b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0254b-131">OUTPUTS</span></span>

### <span data-ttu-id="0254b-132">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0254b-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="0254b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0254b-133">NOTES</span></span>

## <span data-ttu-id="0254b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0254b-134">RELATED LINKS</span></span>
