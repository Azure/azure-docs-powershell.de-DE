---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306739"
---
# <span data-ttu-id="ab71b-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="ab71b-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="ab71b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab71b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab71b-103">Festlegen des täglichen Datenvolumens für eine Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="ab71b-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="ab71b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab71b-104">SYNTAX</span></span>

### <span data-ttu-id="ab71b-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab71b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab71b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab71b-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab71b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab71b-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab71b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab71b-108">DESCRIPTION</span></span>
<span data-ttu-id="ab71b-109">Festlegen des täglichen Datenvolumens für eine Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="ab71b-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="ab71b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab71b-110">EXAMPLES</span></span>

### <span data-ttu-id="ab71b-111">Beispiel 1 Festlegen des täglichen Datenvolumens für eine Ressourcen für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="ab71b-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="ab71b-112">Legen Sie die tägliche Datenlautstärke auf 400 GB pro Tag und beenden Sie die Benachrichtigung zum Senden, wenn die Obergrenze für den "Test" der Ressource in der Ressourcengruppe "Testgruppe" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab71b-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ab71b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab71b-113">PARAMETERS</span></span>

### <span data-ttu-id="ab71b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ab71b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ab71b-115">Anwendungserkenntnisse-Komponentenobjekt.</span><span class="sxs-lookup"><span data-stu-id="ab71b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ab71b-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="ab71b-116">-DailyCapGB</span></span>
<span data-ttu-id="ab71b-117">Tageshöchstwert.</span><span class="sxs-lookup"><span data-stu-id="ab71b-117">Daily Cap.</span></span>

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

### <span data-ttu-id="ab71b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab71b-118">-DefaultProfile</span></span>
<span data-ttu-id="ab71b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab71b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab71b-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="ab71b-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="ab71b-121">Beenden Sie die Benachrichtigung beim Treffen der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="ab71b-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="ab71b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ab71b-122">-Name</span></span>
<span data-ttu-id="ab71b-123">Name der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="ab71b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ab71b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab71b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab71b-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ab71b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ab71b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab71b-126">-ResourceId</span></span>
<span data-ttu-id="ab71b-127">Ressourcen-ID der Komponente für Anwendungseinblicke.</span><span class="sxs-lookup"><span data-stu-id="ab71b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ab71b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab71b-128">-Confirm</span></span>
<span data-ttu-id="ab71b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab71b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab71b-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ab71b-130">-WhatIf</span></span>
<span data-ttu-id="ab71b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab71b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab71b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab71b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab71b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab71b-133">CommonParameters</span></span>
<span data-ttu-id="ab71b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab71b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab71b-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab71b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab71b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab71b-136">INPUTS</span></span>

### <span data-ttu-id="ab71b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ab71b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ab71b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ab71b-138">System.String</span></span>

## <span data-ttu-id="ab71b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab71b-139">OUTPUTS</span></span>

### <span data-ttu-id="ab71b-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="ab71b-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="ab71b-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab71b-141">NOTES</span></span>

## <span data-ttu-id="ab71b-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab71b-142">RELATED LINKS</span></span>
