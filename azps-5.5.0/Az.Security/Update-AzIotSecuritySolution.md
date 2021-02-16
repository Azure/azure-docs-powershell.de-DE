---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169004"
---
# <span data-ttu-id="0b7fa-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0b7fa-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="0b7fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7fa-103">Aktualisieren Sie mindestens eine der folgenden Eigenschaften in der IoT-Sicherheitslösung: Tags, Empfehlungskonfiguration, benutzerdefinierte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b7fa-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="0b7fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b7fa-104">SYNTAX</span></span>

### <span data-ttu-id="0b7fa-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b7fa-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7fa-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b7fa-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7fa-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0b7fa-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b7fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b7fa-108">DESCRIPTION</span></span>
<span data-ttu-id="0b7fa-109">Das cmdlet Update-AzIotSecuritySolution eine oder mehrere der folgenden Eigenschaften in einer bestimmten IoT-Sicherheitslösung: Tags, Empfehlungskonfiguration, benutzerdefinierte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="0b7fa-110">Nur die angegebenen Eigenschaften werden innerhalb derot-Sicherheitslösung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="0b7fa-111">Die Sicherheitslösung für das Internet (IoT) sammelt Sicherheitsdaten und Ereignisse von iot-Geräten und dem iot-Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="0b7fa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b7fa-112">EXAMPLES</span></span>

### <span data-ttu-id="0b7fa-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b7fa-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="0b7fa-114">Aktualisieren der iot-Sicherheitslösung "MySample" aus der Ressourcengruppe "MyResourceGroup" mit Empfehlungskonfiguration und benutzerdefinierten Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b7fa-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="0b7fa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b7fa-115">PARAMETERS</span></span>

### <span data-ttu-id="0b7fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7fa-116">-DefaultProfile</span></span>
<span data-ttu-id="0b7fa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b7fa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b7fa-118">-InputObject</span></span>
<span data-ttu-id="0b7fa-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0b7fa-120">-Name</span></span>
<span data-ttu-id="0b7fa-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b7fa-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="0b7fa-123">Konfiguration von Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b7fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b7fa-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b7fa-126">-ResourceId</span></span>
<span data-ttu-id="0b7fa-127">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0b7fa-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b7fa-128">-Tag</span></span>
<span data-ttu-id="0b7fa-129">Tags.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="0b7fa-130">-UserDefinedResource</span></span>
<span data-ttu-id="0b7fa-131">Benutzerdefinierte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7fa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b7fa-132">-Confirm</span></span>
<span data-ttu-id="0b7fa-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b7fa-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0b7fa-134">-WhatIf</span></span>
<span data-ttu-id="0b7fa-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b7fa-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b7fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7fa-137">CommonParameters</span></span>
<span data-ttu-id="0b7fa-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7fa-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b7fa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7fa-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b7fa-140">INPUTS</span></span>

### <span data-ttu-id="0b7fa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0b7fa-141">System.String</span></span>

### <span data-ttu-id="0b7fa-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0b7fa-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="0b7fa-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b7fa-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b7fa-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="0b7fa-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="0b7fa-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0b7fa-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="0b7fa-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b7fa-146">OUTPUTS</span></span>

### <span data-ttu-id="0b7fa-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0b7fa-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="0b7fa-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b7fa-148">NOTES</span></span>

## <span data-ttu-id="0b7fa-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b7fa-149">RELATED LINKS</span></span>
