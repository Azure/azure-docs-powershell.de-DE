---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177996"
---
# <span data-ttu-id="23190-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="23190-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="23190-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23190-102">SYNOPSIS</span></span>
<span data-ttu-id="23190-103">Fügen Sie eine viel Edge-Bereitstellung in einem Ziel-viel-Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="23190-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="23190-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23190-104">SYNTAX</span></span>

### <span data-ttu-id="23190-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23190-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23190-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="23190-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23190-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="23190-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23190-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23190-108">DESCRIPTION</span></span>
<span data-ttu-id="23190-109">Edge-Bereitstellungen können mit benutzerdefinierten Metriken für die bedarfsgesteuerte Auswertung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23190-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="23190-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring .</span><span class="sxs-lookup"><span data-stu-id="23190-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="23190-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23190-111">EXAMPLES</span></span>

### <span data-ttu-id="23190-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23190-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="23190-113">Erstellen Sie eine Edge-Bereitstellung mit Standardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="23190-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="23190-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23190-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="23190-115">Erstellen Sie eine Edge-Bereitstellung mit einer Priorität von 3, die unter Bedingung gilt, wenn ein Gerät in Gebäude 9 markiert ist und die Umgebung "testen" lautet.</span><span class="sxs-lookup"><span data-stu-id="23190-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="23190-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23190-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="23190-117">Erstellen Sie eine Edge-Bereitstellung mit Benutzer Metriken.</span><span class="sxs-lookup"><span data-stu-id="23190-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="23190-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="23190-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="23190-119">Erstellen Sie eine Edge-Bereitstellung mit Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="23190-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="23190-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="23190-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="23190-121">Erstellen Sie eine Edge-Bereitstellung mit Inhalten.</span><span class="sxs-lookup"><span data-stu-id="23190-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="23190-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="23190-122">PARAMETERS</span></span>

### <span data-ttu-id="23190-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23190-123">-DefaultProfile</span></span>
<span data-ttu-id="23190-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23190-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23190-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23190-125">-InputObject</span></span>
<span data-ttu-id="23190-126">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="23190-126">IotHub object</span></span>

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

### <span data-ttu-id="23190-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="23190-127">-IotHubName</span></span>
<span data-ttu-id="23190-128">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="23190-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="23190-129">-Label</span><span class="sxs-lookup"><span data-stu-id="23190-129">-Label</span></span>
<span data-ttu-id="23190-130">Karte der Beschriftungen, die auf die Ziel Bereitstellung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="23190-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="23190-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="23190-131">-Metric</span></span>
<span data-ttu-id="23190-132">Querys-Sammlung für die Definition von "viel Edge Deployment Metrics".</span><span class="sxs-lookup"><span data-stu-id="23190-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="23190-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="23190-133">-ModulesContent</span></span>
<span data-ttu-id="23190-134">Bereitstellungs Inhalt von Modulen für viel Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="23190-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="23190-135">-Name</span><span class="sxs-lookup"><span data-stu-id="23190-135">-Name</span></span>
<span data-ttu-id="23190-136">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="23190-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="23190-137">-Priorität</span><span class="sxs-lookup"><span data-stu-id="23190-137">-Priority</span></span>
<span data-ttu-id="23190-138">Das Gewicht der Bereitstellung bei konkurrierenden Regeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="23190-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="23190-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23190-139">-ResourceGroupName</span></span>
<span data-ttu-id="23190-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="23190-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="23190-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="23190-141">-ResourceId</span></span>
<span data-ttu-id="23190-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="23190-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="23190-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="23190-143">-TargetCondition</span></span>
<span data-ttu-id="23190-144">Die zielbedingung, auf die eine Edge-Bereitstellung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="23190-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="23190-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23190-145">-Confirm</span></span>
<span data-ttu-id="23190-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23190-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23190-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23190-147">-WhatIf</span></span>
<span data-ttu-id="23190-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23190-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23190-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23190-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23190-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23190-150">CommonParameters</span></span>
<span data-ttu-id="23190-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23190-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23190-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23190-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23190-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23190-153">INPUTS</span></span>

### <span data-ttu-id="23190-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="23190-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="23190-155">System. String</span><span class="sxs-lookup"><span data-stu-id="23190-155">System.String</span></span>

## <span data-ttu-id="23190-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23190-156">OUTPUTS</span></span>

### <span data-ttu-id="23190-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="23190-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="23190-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="23190-158">NOTES</span></span>

## <span data-ttu-id="23190-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23190-159">RELATED LINKS</span></span>
