---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: f55c42178daacdbf2be80982fb151514372d2d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936016"
---
# <span data-ttu-id="d9d34-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d9d34-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="d9d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d34-102">SYNOPSIS</span></span>

<span data-ttu-id="d9d34-103">Aktiviert oder deaktiviert Azure Defender-Pläne für ein Abonnement im Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="d9d34-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="d9d34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9d34-104">SYNTAX</span></span>

### <span data-ttu-id="d9d34-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9d34-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9d34-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9d34-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9d34-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9d34-107">DESCRIPTION</span></span>

<span data-ttu-id="d9d34-108">Aktivieren oder deaktivieren Sie einen der Azure Defender-Pläne für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9d34-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="d9d34-109">Details zu Azure Defender und den verfügbaren Plänen finden Sie unter [Einführung in Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="d9d34-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="d9d34-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9d34-110">EXAMPLES</span></span>

### <span data-ttu-id="d9d34-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9d34-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="d9d34-112">Aktiviert **Azure Defender für Server** für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9d34-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="d9d34-113">"Standard" bezieht sich auf den Status "Ein" für einen Azure Defender-Plan, wie im Preis- und Einstellungsbereich des Azure Security Centers im Azure-Portal dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d9d34-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="d9d34-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9d34-114">PARAMETERS</span></span>

### <span data-ttu-id="d9d34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d34-115">-DefaultProfile</span></span>

<span data-ttu-id="d9d34-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9d34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d34-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9d34-117">-InputObject</span></span>

<span data-ttu-id="d9d34-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9d34-118">Input Object.</span></span>

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

### <span data-ttu-id="d9d34-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d9d34-119">-Name</span></span>

<span data-ttu-id="d9d34-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d9d34-120">Resource name.</span></span>

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

### <span data-ttu-id="d9d34-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="d9d34-121">-PricingTier</span></span>

<span data-ttu-id="d9d34-122">Preisstufe.</span><span class="sxs-lookup"><span data-stu-id="d9d34-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="d9d34-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9d34-123">-Confirm</span></span>

<span data-ttu-id="d9d34-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9d34-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d34-125">-WhatIf</span></span>

<span data-ttu-id="d9d34-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9d34-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9d34-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9d34-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d34-128">CommonParameters</span></span>

<span data-ttu-id="d9d34-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d34-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9d34-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d34-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9d34-131">INPUTS</span></span>

### <span data-ttu-id="d9d34-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d9d34-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d9d34-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9d34-133">OUTPUTS</span></span>

### <span data-ttu-id="d9d34-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d9d34-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d9d34-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9d34-135">NOTES</span></span>

## <span data-ttu-id="d9d34-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9d34-136">RELATED LINKS</span></span>
