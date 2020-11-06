---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495657"
---
# <span data-ttu-id="40294-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="40294-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="40294-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40294-102">SYNOPSIS</span></span>
<span data-ttu-id="40294-103">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="40294-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40294-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40294-104">SYNTAX</span></span>

### <span data-ttu-id="40294-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="40294-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40294-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="40294-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40294-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="40294-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40294-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40294-108">DESCRIPTION</span></span>
<span data-ttu-id="40294-109">Legt die Preise für die Azure Security Center-Ebene für einen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="40294-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="40294-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40294-110">EXAMPLES</span></span>

### <span data-ttu-id="40294-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40294-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="40294-112">Legt die Preisstufe für das Abonnement Azure Security Center auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="40294-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="40294-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="40294-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="40294-114">Legt die "myService1"-Ressourcengruppe Azure Security Center-Preisstufe auf "Standard" fest</span><span class="sxs-lookup"><span data-stu-id="40294-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="40294-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="40294-115">PARAMETERS</span></span>

### <span data-ttu-id="40294-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40294-116">-DefaultProfile</span></span>
<span data-ttu-id="40294-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40294-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40294-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40294-118">-InputObject</span></span>
<span data-ttu-id="40294-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="40294-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40294-120">-Name</span><span class="sxs-lookup"><span data-stu-id="40294-120">-Name</span></span>
<span data-ttu-id="40294-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="40294-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40294-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="40294-122">-PricingTier</span></span>
<span data-ttu-id="40294-123">Preisklasse.</span><span class="sxs-lookup"><span data-stu-id="40294-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40294-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40294-124">-ResourceGroupName</span></span>
<span data-ttu-id="40294-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40294-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40294-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40294-126">-Confirm</span></span>
<span data-ttu-id="40294-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40294-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40294-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40294-128">-WhatIf</span></span>
<span data-ttu-id="40294-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40294-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40294-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40294-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40294-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40294-131">CommonParameters</span></span>
<span data-ttu-id="40294-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40294-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40294-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40294-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40294-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40294-134">INPUTS</span></span>

### <span data-ttu-id="40294-135">System. String</span><span class="sxs-lookup"><span data-stu-id="40294-135">System.String</span></span>
<span data-ttu-id="40294-136">Microsoft. Azure. Commands. Security. Cmdlets. Pricings. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="40294-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="40294-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40294-137">OUTPUTS</span></span>

### <span data-ttu-id="40294-138">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="40294-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="40294-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="40294-139">NOTES</span></span>

## <span data-ttu-id="40294-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40294-140">RELATED LINKS</span></span>
