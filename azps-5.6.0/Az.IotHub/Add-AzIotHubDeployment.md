---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 80494fd18216ce42883a962920ab78bbc2aa628b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942547"
---
# <span data-ttu-id="e5522-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="e5522-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="e5522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5522-102">SYNOPSIS</span></span>
<span data-ttu-id="e5522-103">Fügen Sie eine IoT Edge-Bereitstellung in einem Ziel-IoT Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5522-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="e5522-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5522-104">SYNTAX</span></span>

### <span data-ttu-id="e5522-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5522-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5522-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5522-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5522-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5522-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5522-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5522-108">DESCRIPTION</span></span>
<span data-ttu-id="e5522-109">Edgebereitstellungen können mit benutzerdefinierten Metriken für die On-Demand-Auswertung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5522-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="e5522-110">Weitere https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="e5522-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="e5522-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5522-111">EXAMPLES</span></span>

### <span data-ttu-id="e5522-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5522-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="e5522-113">Erstellen Sie eine Edgebereitstellung mit Standardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="e5522-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="e5522-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5522-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="e5522-115">Erstellen Sie eine Edgebereitstellung mit der Priorität 3, die unter der Bedingung gilt, dass ein Gerät in Gebäude 9 markiert ist und die Umgebung "Test" ist.</span><span class="sxs-lookup"><span data-stu-id="e5522-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="e5522-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5522-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="e5522-117">Erstellen Sie eine Edgebereitstellung mit Benutzermetriken.</span><span class="sxs-lookup"><span data-stu-id="e5522-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="e5522-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e5522-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="e5522-119">Erstellen Sie eine Edgebereitstellung mit Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="e5522-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="e5522-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e5522-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="e5522-121">Erstellen Sie eine Edgebereitstellung mit Inhalten.</span><span class="sxs-lookup"><span data-stu-id="e5522-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="e5522-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5522-122">PARAMETERS</span></span>

### <span data-ttu-id="e5522-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5522-123">-DefaultProfile</span></span>
<span data-ttu-id="e5522-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5522-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5522-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5522-125">-InputObject</span></span>
<span data-ttu-id="e5522-126">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e5522-126">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e5522-127">-IotHubName</span></span>
<span data-ttu-id="e5522-128">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="e5522-128">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-129">-Label</span><span class="sxs-lookup"><span data-stu-id="e5522-129">-Label</span></span>
<span data-ttu-id="e5522-130">Karte der Bezeichnungen, die auf die Zielbereitstellung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5522-130">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-131">-Metrisch</span><span class="sxs-lookup"><span data-stu-id="e5522-131">-Metric</span></span>
<span data-ttu-id="e5522-132">Abfragesammlung für die Definition von IoT Edge-Bereitstellungsmetriken.</span><span class="sxs-lookup"><span data-stu-id="e5522-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="e5522-133">-ModulesContent</span></span>
<span data-ttu-id="e5522-134">Bereitstellungsinhalt von Modulen für IoT Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="e5522-134">Deployment content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e5522-135">-Name</span></span>
<span data-ttu-id="e5522-136">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e5522-136">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-137">-Priorität</span><span class="sxs-lookup"><span data-stu-id="e5522-137">-Priority</span></span>
<span data-ttu-id="e5522-138">Gewicht der Bereitstellung im Falle konkurrierender Regeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="e5522-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5522-139">-ResourceGroupName</span></span>
<span data-ttu-id="e5522-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e5522-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5522-141">-ResourceId</span></span>
<span data-ttu-id="e5522-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e5522-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="e5522-143">-TargetCondition</span></span>
<span data-ttu-id="e5522-144">Zielbedingung, für die eine Edgebereitstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="e5522-144">Target condition in which an Edge deployment applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5522-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5522-145">-Confirm</span></span>
<span data-ttu-id="e5522-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5522-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5522-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5522-147">-WhatIf</span></span>
<span data-ttu-id="e5522-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5522-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5522-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5522-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5522-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5522-150">CommonParameters</span></span>
<span data-ttu-id="e5522-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5522-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5522-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5522-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5522-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5522-153">INPUTS</span></span>

### <span data-ttu-id="e5522-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5522-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5522-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e5522-155">System.String</span></span>

## <span data-ttu-id="e5522-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5522-156">OUTPUTS</span></span>

### <span data-ttu-id="e5522-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="e5522-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="e5522-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5522-158">NOTES</span></span>

## <span data-ttu-id="e5522-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5522-159">RELATED LINKS</span></span>
