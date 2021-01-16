---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295504"
---
# <span data-ttu-id="9b62d-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9b62d-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="9b62d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b62d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b62d-103">Erstellen oder Aktualisieren einer Sicherheitslösung für das Internet (IoT)</span><span class="sxs-lookup"><span data-stu-id="9b62d-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="9b62d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b62d-104">SYNTAX</span></span>

### <span data-ttu-id="9b62d-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b62d-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b62d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b62d-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b62d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b62d-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b62d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b62d-108">DESCRIPTION</span></span>
<span data-ttu-id="9b62d-109">Das Set-AzIotSecuritySolution erstellt oder aktualisiert eine bestimmte iot-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="9b62d-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="9b62d-110">Die Sicherheitslösung für das Internet (IoT) sammelt Sicherheitsdaten und Ereignisse von iot-Geräten und dem iot-Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="9b62d-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="9b62d-111">Der Name der iot-Sicherheitslösung sollte mit dem Namen des iot-Hubs identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9b62d-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="9b62d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b62d-112">EXAMPLES</span></span>

### <span data-ttu-id="9b62d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b62d-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="9b62d-114">Erstellen Sie die neue iot-Sicherheitslösung "MySample" für den IoT-Hub mit der Ressourcen-ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (der Name der Lösung sollte mit dem Namen des IoT-Hubs identisch sein)</span><span class="sxs-lookup"><span data-stu-id="9b62d-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="9b62d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b62d-115">PARAMETERS</span></span>

### <span data-ttu-id="9b62d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b62d-116">-DefaultProfile</span></span>
<span data-ttu-id="9b62d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b62d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b62d-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="9b62d-118">-DisabledDataSource</span></span>
<span data-ttu-id="9b62d-119">Deaktivierte Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="9b62d-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9b62d-120">-DisplayName</span></span>
<span data-ttu-id="9b62d-121">Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="9b62d-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9b62d-122">-Enabled</span></span>
<span data-ttu-id="9b62d-123">Status .</span><span class="sxs-lookup"><span data-stu-id="9b62d-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-124">-Export</span><span class="sxs-lookup"><span data-stu-id="9b62d-124">-Export</span></span>
<span data-ttu-id="9b62d-125">Exportieren sie Daten.</span><span class="sxs-lookup"><span data-stu-id="9b62d-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b62d-126">-InputObject</span></span>
<span data-ttu-id="9b62d-127">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="9b62d-127">Input Object.</span></span>

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

### <span data-ttu-id="9b62d-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9b62d-128">-IotHub</span></span>
<span data-ttu-id="9b62d-129">"Hubs" aus.</span><span class="sxs-lookup"><span data-stu-id="9b62d-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="9b62d-130">-Location</span></span>
<span data-ttu-id="9b62d-131">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="9b62d-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9b62d-132">-Name</span></span>
<span data-ttu-id="9b62d-133">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9b62d-133">Resource name.</span></span>

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

### <span data-ttu-id="9b62d-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b62d-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="9b62d-135">Konfiguration von Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9b62d-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="9b62d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b62d-136">-ResourceGroupName</span></span>
<span data-ttu-id="9b62d-137">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9b62d-137">Resource group name.</span></span>

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

### <span data-ttu-id="9b62d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b62d-138">-ResourceId</span></span>
<span data-ttu-id="9b62d-139">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b62d-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9b62d-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b62d-140">-Tag</span></span>
<span data-ttu-id="9b62d-141">Tags.</span><span class="sxs-lookup"><span data-stu-id="9b62d-141">Tags.</span></span>

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

### <span data-ttu-id="9b62d-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="9b62d-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="9b62d-143">Unmasked ip logging status.</span><span class="sxs-lookup"><span data-stu-id="9b62d-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="9b62d-144">-UserDefinedResource</span></span>
<span data-ttu-id="9b62d-145">Benutzerdefinierte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9b62d-145">User defined resources.</span></span>

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

### <span data-ttu-id="9b62d-146">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9b62d-146">-Workspace</span></span>
<span data-ttu-id="9b62d-147">Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="9b62d-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b62d-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b62d-148">-Confirm</span></span>
<span data-ttu-id="9b62d-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b62d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b62d-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9b62d-150">-WhatIf</span></span>
<span data-ttu-id="9b62d-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b62d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b62d-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b62d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b62d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b62d-153">CommonParameters</span></span>
<span data-ttu-id="9b62d-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b62d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b62d-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b62d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b62d-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b62d-156">INPUTS</span></span>

### <span data-ttu-id="9b62d-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9b62d-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="9b62d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9b62d-158">System.String</span></span>

### <span data-ttu-id="9b62d-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b62d-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9b62d-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9b62d-160">System.String[]</span></span>

### <span data-ttu-id="9b62d-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="9b62d-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="9b62d-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9b62d-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="9b62d-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b62d-163">OUTPUTS</span></span>

### <span data-ttu-id="9b62d-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9b62d-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="9b62d-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b62d-165">NOTES</span></span>

## <span data-ttu-id="9b62d-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b62d-166">RELATED LINKS</span></span>
