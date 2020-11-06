---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480625"
---
# <span data-ttu-id="47142-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="47142-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="47142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47142-102">SYNOPSIS</span></span>
<span data-ttu-id="47142-103">Einrichten der täglichen Datenvolumen Obergrenze für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="47142-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47142-104">SYNTAX</span></span>

### <span data-ttu-id="47142-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="47142-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47142-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47142-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47142-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47142-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47142-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47142-108">DESCRIPTION</span></span>
<span data-ttu-id="47142-109">Einrichten der täglichen Datenvolumen Obergrenze für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="47142-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="47142-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47142-110">EXAMPLES</span></span>

### <span data-ttu-id="47142-111">Beispiel 1 festgelegte tägliche Datenvolumen Obergrenze für eine Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="47142-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="47142-112">Setzen Sie das tägliche Datenvolumen Cap auf 400GB pro Tag, und beenden Sie die Benachrichtigung, wenn Sie auf Cap für Ressource "Test" in der Ressourcengruppe "Testgruppe" klicken.</span><span class="sxs-lookup"><span data-stu-id="47142-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="47142-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="47142-113">PARAMETERS</span></span>

### <span data-ttu-id="47142-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="47142-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="47142-115">Application Insights-Komponentenobjekt</span><span class="sxs-lookup"><span data-stu-id="47142-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="47142-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="47142-116">-DailyCapGB</span></span>
<span data-ttu-id="47142-117">Tages-Cap.</span><span class="sxs-lookup"><span data-stu-id="47142-117">Daily Cap.</span></span>

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

### <span data-ttu-id="47142-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47142-118">-DefaultProfile</span></span>
<span data-ttu-id="47142-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47142-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47142-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="47142-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="47142-121">Beenden der Benachrichtigung beim Drücken der Zugriffs Grenze</span><span class="sxs-lookup"><span data-stu-id="47142-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="47142-122">-Name</span><span class="sxs-lookup"><span data-stu-id="47142-122">-Name</span></span>
<span data-ttu-id="47142-123">Application Insights-Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="47142-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="47142-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47142-124">-ResourceGroupName</span></span>
<span data-ttu-id="47142-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47142-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="47142-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="47142-126">-ResourceId</span></span>
<span data-ttu-id="47142-127">Application Insights-Komponenten-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="47142-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="47142-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47142-128">-Confirm</span></span>
<span data-ttu-id="47142-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47142-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47142-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47142-130">-WhatIf</span></span>
<span data-ttu-id="47142-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47142-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47142-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47142-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47142-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47142-133">CommonParameters</span></span>
<span data-ttu-id="47142-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47142-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47142-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47142-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47142-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47142-136">INPUTS</span></span>

### <span data-ttu-id="47142-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="47142-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="47142-138">Parameter: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47142-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="47142-139">System. String</span><span class="sxs-lookup"><span data-stu-id="47142-139">System.String</span></span>

## <span data-ttu-id="47142-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47142-140">OUTPUTS</span></span>

### <span data-ttu-id="47142-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="47142-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="47142-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="47142-142">NOTES</span></span>

## <span data-ttu-id="47142-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47142-143">RELATED LINKS</span></span>
