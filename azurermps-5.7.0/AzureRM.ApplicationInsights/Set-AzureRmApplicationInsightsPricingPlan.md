---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502638"
---
# <span data-ttu-id="47a9a-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="47a9a-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="47a9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="47a9a-103">Einrichten von Preisplänen und täglichen Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="47a9a-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47a9a-104">SYNTAX</span></span>

### <span data-ttu-id="47a9a-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="47a9a-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a9a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a9a-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a9a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a9a-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47a9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47a9a-108">DESCRIPTION</span></span>
<span data-ttu-id="47a9a-109">Einrichten von Preisplänen und täglichen Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="47a9a-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="47a9a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47a9a-110">EXAMPLES</span></span>

### <span data-ttu-id="47a9a-111">Beispiel 1 Satz Preisplan und tägliche Datenvolumen Informationen für eine Ressource für Anwendungs Einblicke</span><span class="sxs-lookup"><span data-stu-id="47a9a-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="47a9a-112">Legen Sie den Preisplan auf "Standard" fest, legen Sie die tägliche Datenmenge auf 400GB pro Tag fest, und beenden Sie die Benachrichtigung beim Drücken der Zugriffs Grenze für die Ressource "Test" in der Ressourcengruppe "Testgruppe".</span><span class="sxs-lookup"><span data-stu-id="47a9a-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="47a9a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a9a-113">PARAMETERS</span></span>

### <span data-ttu-id="47a9a-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="47a9a-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="47a9a-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="47a9a-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47a9a-116">-Confirm</span></span>
<span data-ttu-id="47a9a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47a9a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a9a-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="47a9a-118">-DailyCapGB</span></span>
<span data-ttu-id="47a9a-119">Tages-Cap.</span><span class="sxs-lookup"><span data-stu-id="47a9a-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a9a-120">-DefaultProfile</span></span>
<span data-ttu-id="47a9a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47a9a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a9a-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="47a9a-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="47a9a-123">Beenden der Benachrichtigung beim Drücken der Zugriffs Grenze</span><span class="sxs-lookup"><span data-stu-id="47a9a-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="47a9a-124">-Name</span></span>
<span data-ttu-id="47a9a-125">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="47a9a-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="47a9a-126">-PricingPlan</span></span>
<span data-ttu-id="47a9a-127">Name des Preisplans</span><span class="sxs-lookup"><span data-stu-id="47a9a-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="47a9a-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47a9a-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="47a9a-130">-ResourceId</span></span>
<span data-ttu-id="47a9a-131">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="47a9a-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a9a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a9a-132">-WhatIf</span></span>
<span data-ttu-id="47a9a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47a9a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47a9a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47a9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a9a-135">CommonParameters</span></span>
<span data-ttu-id="47a9a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a9a-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a9a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a9a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47a9a-138">INPUTS</span></span>

### <span data-ttu-id="47a9a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="47a9a-139">System.String</span></span>
<span data-ttu-id="47a9a-140">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47a9a-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="47a9a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47a9a-141">OUTPUTS</span></span>

### <span data-ttu-id="47a9a-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="47a9a-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="47a9a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="47a9a-143">NOTES</span></span>

## <span data-ttu-id="47a9a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47a9a-144">RELATED LINKS</span></span>

