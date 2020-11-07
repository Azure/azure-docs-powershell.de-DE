---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 33b55c70d88daf8493012945f49794c25e62b474
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661860"
---
# <span data-ttu-id="88618-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="88618-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="88618-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88618-102">SYNOPSIS</span></span>
<span data-ttu-id="88618-103">Einrichten von Preisplänen und täglichen Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="88618-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="88618-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88618-104">SYNTAX</span></span>

### <span data-ttu-id="88618-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="88618-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88618-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88618-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88618-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88618-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88618-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88618-108">DESCRIPTION</span></span>
<span data-ttu-id="88618-109">Einrichten von Preisplänen und täglichen Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="88618-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="88618-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88618-110">EXAMPLES</span></span>

### <span data-ttu-id="88618-111">Beispiel 1 Satz Preisplan und tägliche Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="88618-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="88618-112">Legen Sie den Preisplan auf "Standard" fest, legen Sie die tägliche Datenmenge auf 400GB pro Tag fest, und beenden Sie die Benachrichtigung beim Drücken der Zugriffs Grenze für die Ressource "Test" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="88618-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="88618-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="88618-113">PARAMETERS</span></span>

### <span data-ttu-id="88618-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="88618-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="88618-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="88618-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="88618-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="88618-116">-DailyCapGB</span></span>
<span data-ttu-id="88618-117">Tages-Cap.</span><span class="sxs-lookup"><span data-stu-id="88618-117">Daily Cap.</span></span>

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

### <span data-ttu-id="88618-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88618-118">-DefaultProfile</span></span>
<span data-ttu-id="88618-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88618-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88618-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="88618-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="88618-121">Beenden der Benachrichtigung beim Drücken der Zugriffs Grenze</span><span class="sxs-lookup"><span data-stu-id="88618-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="88618-122">-Name</span><span class="sxs-lookup"><span data-stu-id="88618-122">-Name</span></span>
<span data-ttu-id="88618-123">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="88618-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="88618-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="88618-124">-PricingPlan</span></span>
<span data-ttu-id="88618-125">Name des Preisplans</span><span class="sxs-lookup"><span data-stu-id="88618-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="88618-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88618-126">-ResourceGroupName</span></span>
<span data-ttu-id="88618-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88618-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="88618-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="88618-128">-ResourceId</span></span>
<span data-ttu-id="88618-129">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="88618-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="88618-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88618-130">-Confirm</span></span>
<span data-ttu-id="88618-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88618-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88618-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88618-132">-WhatIf</span></span>
<span data-ttu-id="88618-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88618-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88618-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88618-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88618-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88618-135">CommonParameters</span></span>
<span data-ttu-id="88618-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88618-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88618-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88618-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88618-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88618-138">INPUTS</span></span>

### <span data-ttu-id="88618-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="88618-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="88618-140">System. String</span><span class="sxs-lookup"><span data-stu-id="88618-140">System.String</span></span>

## <span data-ttu-id="88618-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88618-141">OUTPUTS</span></span>

### <span data-ttu-id="88618-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="88618-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="88618-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="88618-143">NOTES</span></span>

## <span data-ttu-id="88618-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88618-144">RELATED LINKS</span></span>
