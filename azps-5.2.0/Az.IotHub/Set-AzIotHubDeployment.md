---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291688"
---
# <span data-ttu-id="8bc52-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="8bc52-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="8bc52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc52-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc52-103">Aktualisieren Sie die anpassbaren Felder der IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="8bc52-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="8bc52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bc52-104">SYNTAX</span></span>

### <span data-ttu-id="8bc52-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bc52-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc52-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bc52-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc52-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bc52-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc52-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bc52-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc52-109">Aktualisieren sie die angegebenen Eigenschaften einer IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="8bc52-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="8bc52-110">Hinweis: Der Konfigurationsinhalt kann nicht stumm änderbar sein.</span><span class="sxs-lookup"><span data-stu-id="8bc52-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="8bc52-111">Zu den Konfigurationseigenschaften, die aktualisiert werden können, gehören "Bezeichnungen", "Metriken", "Priorität" und "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="8bc52-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="8bc52-112">Weitere https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="8bc52-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="8bc52-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bc52-113">EXAMPLES</span></span>

### <span data-ttu-id="8bc52-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bc52-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="8bc52-115">Ändern Sie die Priorität der IoT Edge-Bereitstellung, und aktualisieren Sie die Zielbedingung.</span><span class="sxs-lookup"><span data-stu-id="8bc52-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="8bc52-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8bc52-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="8bc52-117">Aktualisieren Sie die Metriken und Bezeichnungen der IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="8bc52-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="8bc52-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc52-118">PARAMETERS</span></span>

### <span data-ttu-id="8bc52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc52-119">-DefaultProfile</span></span>
<span data-ttu-id="8bc52-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bc52-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc52-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc52-121">-Force</span></span>
<span data-ttu-id="8bc52-122">Ermöglicht das Ersetzen von Bereitstellungsobjekten, auch wenn es seit dem letzten Abruf aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8bc52-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="8bc52-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc52-123">-InputObject</span></span>
<span data-ttu-id="8bc52-124">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="8bc52-124">IotHub object</span></span>

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

### <span data-ttu-id="8bc52-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8bc52-125">-IotHubName</span></span>
<span data-ttu-id="8bc52-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="8bc52-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8bc52-127">-Label</span><span class="sxs-lookup"><span data-stu-id="8bc52-127">-Label</span></span>
<span data-ttu-id="8bc52-128">Karte der Bezeichnungen, die auf die Zielbereitstellung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8bc52-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="8bc52-129">-metrisch</span><span class="sxs-lookup"><span data-stu-id="8bc52-129">-Metric</span></span>
<span data-ttu-id="8bc52-130">Sammlung von Abfragen für die Definition von IoT Edge-Bereitstellungsmetriken.</span><span class="sxs-lookup"><span data-stu-id="8bc52-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="8bc52-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8bc52-131">-Name</span></span>
<span data-ttu-id="8bc52-132">Id für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="8bc52-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="8bc52-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="8bc52-133">-Priority</span></span>
<span data-ttu-id="8bc52-134">Gewichtung der Bereitstellung bei Konkurrenzregeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="8bc52-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="8bc52-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc52-135">-ResourceGroupName</span></span>
<span data-ttu-id="8bc52-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8bc52-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8bc52-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc52-137">-ResourceId</span></span>
<span data-ttu-id="8bc52-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8bc52-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8bc52-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="8bc52-139">-TargetCondition</span></span>
<span data-ttu-id="8bc52-140">Zielbedingung, für die eine Edgebereitstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="8bc52-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="8bc52-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bc52-141">-Confirm</span></span>
<span data-ttu-id="8bc52-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bc52-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc52-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8bc52-143">-WhatIf</span></span>
<span data-ttu-id="8bc52-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bc52-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc52-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bc52-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc52-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc52-146">CommonParameters</span></span>
<span data-ttu-id="8bc52-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc52-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc52-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc52-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc52-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bc52-149">INPUTS</span></span>

### <span data-ttu-id="8bc52-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8bc52-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8bc52-151">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc52-151">System.String</span></span>

## <span data-ttu-id="8bc52-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bc52-152">OUTPUTS</span></span>

### <span data-ttu-id="8bc52-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8bc52-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="8bc52-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8bc52-154">NOTES</span></span>

## <span data-ttu-id="8bc52-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8bc52-155">RELATED LINKS</span></span>
