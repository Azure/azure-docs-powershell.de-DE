---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381224"
---
# <span data-ttu-id="8eef7-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8eef7-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="8eef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eef7-102">SYNOPSIS</span></span>
<span data-ttu-id="8eef7-103">Festlegen des Preisplans und der täglichen Datenvolumeninformationen für eine Ressourcen für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="8eef7-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="8eef7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eef7-104">SYNTAX</span></span>

### <span data-ttu-id="8eef7-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8eef7-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eef7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eef7-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eef7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eef7-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8eef7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8eef7-108">DESCRIPTION</span></span>
<span data-ttu-id="8eef7-109">Festlegen des Preisplans und der täglichen Datenvolumeninformationen für eine Ressourcen für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="8eef7-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="8eef7-110">Der Preisplan für Anwendungserkenntnisse, der nach April 2018 erstellt wurde, kann von diesem Cmdlet nicht festgelegt werden: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="8eef7-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="8eef7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8eef7-111">EXAMPLES</span></span>

### <span data-ttu-id="8eef7-112">Beispiel 1 Festlegen des Preisplans und täglicher Datenvolumeninformationen für eine Ressourcen für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="8eef7-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="8eef7-113">Legen Sie den Preisplan auf "Standard" und das tägliche Datenvolumen auf 400 GB pro Tag und beenden Sie die Benachrichtigung zum Senden, wenn die Obergrenze für den Ressourcentest in der Ressourcengruppe "Testgruppe" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8eef7-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8eef7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eef7-114">PARAMETERS</span></span>

### <span data-ttu-id="8eef7-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eef7-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8eef7-116">Anwendungserkenntnisse-Komponentenobjekt.</span><span class="sxs-lookup"><span data-stu-id="8eef7-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="8eef7-117">-DailyCapGB</span></span>
<span data-ttu-id="8eef7-118">Tageshöchstwert.</span><span class="sxs-lookup"><span data-stu-id="8eef7-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eef7-119">-DefaultProfile</span></span>
<span data-ttu-id="8eef7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8eef7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eef7-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="8eef7-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="8eef7-122">Beenden Sie die Benachrichtigung beim Treffen der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8eef7-122">Stop send notification when hit cap.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8eef7-123">-Name</span></span>
<span data-ttu-id="8eef7-124">Name der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="8eef7-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="8eef7-125">-PricingPlan</span></span>
<span data-ttu-id="8eef7-126">Name des Preisplans.</span><span class="sxs-lookup"><span data-stu-id="8eef7-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eef7-127">-ResourceGroupName</span></span>
<span data-ttu-id="8eef7-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8eef7-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eef7-129">-ResourceId</span></span>
<span data-ttu-id="8eef7-130">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="8eef7-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eef7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8eef7-131">-Confirm</span></span>
<span data-ttu-id="8eef7-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8eef7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eef7-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8eef7-133">-WhatIf</span></span>
<span data-ttu-id="8eef7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8eef7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8eef7-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8eef7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eef7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eef7-136">CommonParameters</span></span>
<span data-ttu-id="8eef7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eef7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eef7-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eef7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eef7-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8eef7-139">INPUTS</span></span>

### <span data-ttu-id="8eef7-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8eef7-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8eef7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8eef7-141">System.String</span></span>

## <span data-ttu-id="8eef7-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8eef7-142">OUTPUTS</span></span>

### <span data-ttu-id="8eef7-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8eef7-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="8eef7-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8eef7-144">NOTES</span></span>

## <span data-ttu-id="8eef7-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8eef7-145">RELATED LINKS</span></span>
