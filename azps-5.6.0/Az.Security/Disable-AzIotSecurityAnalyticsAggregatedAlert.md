---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: c698c91f8b4115fb811ebcda41eaf43662f0bf08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936088"
---
# <span data-ttu-id="9ad44-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="9ad44-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="9ad44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad44-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad44-103">Schließen der aggregierten Benachrichtigung "Iot"</span><span class="sxs-lookup"><span data-stu-id="9ad44-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="9ad44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ad44-104">SYNTAX</span></span>

### <span data-ttu-id="9ad44-105">SolutionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ad44-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad44-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad44-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad44-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad44-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad44-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ad44-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad44-109">Das Disable-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet schließt eine bestimmte aggragated-Benachrichtigung auf Geräten des iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="9ad44-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="9ad44-110">Der Name der aggregierten Benachrichtigungen ist eine Kombination aus dem Warnungstyp und dem Benachrichtigungsaggragted-Datum, getrennt durch "/".</span><span class="sxs-lookup"><span data-stu-id="9ad44-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="9ad44-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ad44-111">EXAMPLES</span></span>

### <span data-ttu-id="9ad44-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ad44-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="9ad44-113">Schließen der aggregierten Benachrichtigung "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="9ad44-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="9ad44-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9ad44-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="9ad44-115">Schließen einer aggregierten Benachrichtigung mit der Ressourcen-ID "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="9ad44-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="9ad44-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ad44-116">PARAMETERS</span></span>

### <span data-ttu-id="9ad44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad44-117">-DefaultProfile</span></span>
<span data-ttu-id="9ad44-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ad44-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ad44-119">-InputObject</span></span>
<span data-ttu-id="9ad44-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="9ad44-120">Input Object.</span></span>

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

### <span data-ttu-id="9ad44-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9ad44-121">-Name</span></span>
<span data-ttu-id="9ad44-122">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9ad44-122">Resource name.</span></span>

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

### <span data-ttu-id="9ad44-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ad44-123">-PassThru</span></span>
<span data-ttu-id="9ad44-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9ad44-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9ad44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad44-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ad44-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ad44-126">Resource group name.</span></span>

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

### <span data-ttu-id="9ad44-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad44-127">-ResourceId</span></span>
<span data-ttu-id="9ad44-128">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ad44-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9ad44-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="9ad44-129">-SolutionName</span></span>
<span data-ttu-id="9ad44-130">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="9ad44-130">Solution name</span></span>

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

### <span data-ttu-id="9ad44-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ad44-131">-Confirm</span></span>
<span data-ttu-id="9ad44-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ad44-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad44-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad44-133">-WhatIf</span></span>
<span data-ttu-id="9ad44-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ad44-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ad44-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ad44-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad44-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad44-136">CommonParameters</span></span>
<span data-ttu-id="9ad44-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad44-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad44-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ad44-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad44-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad44-139">INPUTS</span></span>

### <span data-ttu-id="9ad44-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="9ad44-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="9ad44-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9ad44-141">System.String</span></span>

## <span data-ttu-id="9ad44-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad44-142">OUTPUTS</span></span>

### <span data-ttu-id="9ad44-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ad44-143">System.Boolean</span></span>

## <span data-ttu-id="9ad44-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ad44-144">NOTES</span></span>

## <span data-ttu-id="9ad44-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ad44-145">RELATED LINKS</span></span>
