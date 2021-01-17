---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386572"
---
# <span data-ttu-id="db783-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="db783-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="db783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db783-102">SYNOPSIS</span></span>
<span data-ttu-id="db783-103">Aktualisieren Sie die anpassbaren Felder der IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="db783-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="db783-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db783-104">SYNTAX</span></span>

### <span data-ttu-id="db783-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="db783-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db783-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="db783-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db783-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="db783-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db783-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db783-108">DESCRIPTION</span></span>
<span data-ttu-id="db783-109">Aktualisieren sie die angegebenen Eigenschaften einer IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="db783-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="db783-110">Hinweis: Der Konfigurationsinhalt kann nicht stumm änderbar sein.</span><span class="sxs-lookup"><span data-stu-id="db783-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="db783-111">Zu den Konfigurationseigenschaften, die aktualisiert werden können, gehören "Bezeichnungen", "Metriken", "Priorität" und "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="db783-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="db783-112">Weitere https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="db783-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="db783-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db783-113">EXAMPLES</span></span>

### <span data-ttu-id="db783-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db783-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="db783-115">Ändern Sie die Priorität der IoT Edge-Bereitstellung, und aktualisieren Sie die Zielbedingung.</span><span class="sxs-lookup"><span data-stu-id="db783-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="db783-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db783-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="db783-117">Aktualisieren Sie die Metriken und Bezeichnungen der IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="db783-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="db783-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db783-118">PARAMETERS</span></span>

### <span data-ttu-id="db783-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db783-119">-DefaultProfile</span></span>
<span data-ttu-id="db783-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db783-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db783-121">-Force</span><span class="sxs-lookup"><span data-stu-id="db783-121">-Force</span></span>
<span data-ttu-id="db783-122">Ermöglicht das Ersetzen von Bereitstellungsobjekten, auch wenn es seit dem letzten Abruf aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="db783-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="db783-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db783-123">-InputObject</span></span>
<span data-ttu-id="db783-124">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="db783-124">IotHub object</span></span>

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

### <span data-ttu-id="db783-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="db783-125">-IotHubName</span></span>
<span data-ttu-id="db783-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="db783-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="db783-127">-Label</span><span class="sxs-lookup"><span data-stu-id="db783-127">-Label</span></span>
<span data-ttu-id="db783-128">Karte der Bezeichnungen, die auf die Zielbereitstellung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db783-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="db783-129">-metrisch</span><span class="sxs-lookup"><span data-stu-id="db783-129">-Metric</span></span>
<span data-ttu-id="db783-130">Sammlung von Abfragen für die Definition von IoT Edge-Bereitstellungsmetriken.</span><span class="sxs-lookup"><span data-stu-id="db783-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="db783-131">-Name</span><span class="sxs-lookup"><span data-stu-id="db783-131">-Name</span></span>
<span data-ttu-id="db783-132">Id für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="db783-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="db783-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="db783-133">-Priority</span></span>
<span data-ttu-id="db783-134">Gewichtung der Bereitstellung bei Konkurrenzregeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="db783-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="db783-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db783-135">-ResourceGroupName</span></span>
<span data-ttu-id="db783-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="db783-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="db783-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db783-137">-ResourceId</span></span>
<span data-ttu-id="db783-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="db783-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="db783-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="db783-139">-TargetCondition</span></span>
<span data-ttu-id="db783-140">Zielbedingung, für die eine Edgebereitstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="db783-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="db783-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db783-141">-Confirm</span></span>
<span data-ttu-id="db783-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db783-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db783-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="db783-143">-WhatIf</span></span>
<span data-ttu-id="db783-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db783-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db783-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db783-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db783-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db783-146">CommonParameters</span></span>
<span data-ttu-id="db783-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db783-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db783-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db783-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db783-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db783-149">INPUTS</span></span>

### <span data-ttu-id="db783-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="db783-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="db783-151">System.String</span><span class="sxs-lookup"><span data-stu-id="db783-151">System.String</span></span>

## <span data-ttu-id="db783-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db783-152">OUTPUTS</span></span>

### <span data-ttu-id="db783-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="db783-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="db783-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db783-154">NOTES</span></span>

## <span data-ttu-id="db783-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db783-155">RELATED LINKS</span></span>
