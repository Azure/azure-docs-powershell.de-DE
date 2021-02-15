---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145892"
---
# <span data-ttu-id="ed3fb-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="ed3fb-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="ed3fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3fb-103">Schließen der aggregierten Benachrichtigung "Iot"</span><span class="sxs-lookup"><span data-stu-id="ed3fb-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="ed3fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed3fb-104">SYNTAX</span></span>

### <span data-ttu-id="ed3fb-105">SolutionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed3fb-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3fb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3fb-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3fb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed3fb-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed3fb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed3fb-108">DESCRIPTION</span></span>
<span data-ttu-id="ed3fb-109">Das Disable-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet schließt eine bestimmte Benachrichtigung auf Geräten des iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="ed3fb-110">Der Name der aggregierten Warnungen ist eine Kombination aus dem Warnungstyp und dem Benachrichtigungsdatum, getrennt durch '/'.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="ed3fb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed3fb-111">EXAMPLES</span></span>

### <span data-ttu-id="ed3fb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed3fb-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="ed3fb-113">Schließen der aggregierten Warnung "IoT_SucessfulLocalLogin/2020-03-15" (Name kombiniert aus Warnungstyp und dem aggregierten Datum) aus der Sicherheitslösung "MySolutionName" des IoT in der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="ed3fb-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="ed3fb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed3fb-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="ed3fb-115">Schließen einer aggregierten Benachrichtigung mit der Ressourcen-ID "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="ed3fb-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="ed3fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed3fb-116">PARAMETERS</span></span>

### <span data-ttu-id="ed3fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3fb-117">-DefaultProfile</span></span>
<span data-ttu-id="ed3fb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3fb-119">-InputObject</span></span>
<span data-ttu-id="ed3fb-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3fb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ed3fb-121">-Name</span></span>
<span data-ttu-id="ed3fb-122">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed3fb-123">-PassThru</span></span>
<span data-ttu-id="ed3fb-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ed3fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed3fb-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3fb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed3fb-127">-ResourceId</span></span>
<span data-ttu-id="ed3fb-128">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3fb-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="ed3fb-129">-SolutionName</span></span>
<span data-ttu-id="ed3fb-130">Lösungsname</span><span class="sxs-lookup"><span data-stu-id="ed3fb-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3fb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed3fb-131">-Confirm</span></span>
<span data-ttu-id="ed3fb-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed3fb-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed3fb-133">-WhatIf</span></span>
<span data-ttu-id="ed3fb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed3fb-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed3fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3fb-136">CommonParameters</span></span>
<span data-ttu-id="ed3fb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3fb-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed3fb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3fb-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed3fb-139">INPUTS</span></span>

### <span data-ttu-id="ed3fb-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="ed3fb-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="ed3fb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ed3fb-141">System.String</span></span>

## <span data-ttu-id="ed3fb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed3fb-142">OUTPUTS</span></span>

### <span data-ttu-id="ed3fb-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed3fb-143">System.Boolean</span></span>

## <span data-ttu-id="ed3fb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed3fb-144">NOTES</span></span>

## <span data-ttu-id="ed3fb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed3fb-145">RELATED LINKS</span></span>
