---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009246"
---
# <span data-ttu-id="89503-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="89503-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="89503-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89503-102">SYNOPSIS</span></span>
<span data-ttu-id="89503-103">Aktualisieren Sie die änderbaren Felder der Bereitstellung viel Edge.</span><span class="sxs-lookup"><span data-stu-id="89503-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="89503-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89503-104">SYNTAX</span></span>

### <span data-ttu-id="89503-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89503-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89503-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89503-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89503-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89503-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89503-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89503-108">DESCRIPTION</span></span>
<span data-ttu-id="89503-109">Aktualisieren Sie die angegebenen Eigenschaften einer viel Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="89503-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="89503-110">Hinweis: der Konfigurationsinhalt ist unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="89503-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="89503-111">Konfigurationseigenschaften, die aktualisiert werden können, sind "Beschriftungen", "Metriken", "Priorität" und "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="89503-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="89503-112">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  .</span><span class="sxs-lookup"><span data-stu-id="89503-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="89503-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89503-113">EXAMPLES</span></span>

### <span data-ttu-id="89503-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89503-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="89503-115">Ändern Sie die Priorität der viel Edge-Bereitstellung, und aktualisieren Sie deren zielbedingung.</span><span class="sxs-lookup"><span data-stu-id="89503-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="89503-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="89503-116">PARAMETERS</span></span>

### <span data-ttu-id="89503-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89503-117">-DefaultProfile</span></span>
<span data-ttu-id="89503-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89503-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89503-119">-Force</span><span class="sxs-lookup"><span data-stu-id="89503-119">-Force</span></span>
<span data-ttu-id="89503-120">Ermöglicht die Ersetzung des Bereitstellungsobjekts, auch wenn es seit dem letzten Abrufen aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89503-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="89503-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89503-121">-InputObject</span></span>
<span data-ttu-id="89503-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="89503-122">IotHub object</span></span>

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

### <span data-ttu-id="89503-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="89503-123">-IotHubName</span></span>
<span data-ttu-id="89503-124">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="89503-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="89503-125">-Label</span><span class="sxs-lookup"><span data-stu-id="89503-125">-Label</span></span>
<span data-ttu-id="89503-126">Karte der Beschriftungen, die auf die Ziel Bereitstellung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89503-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="89503-127">-Metric</span><span class="sxs-lookup"><span data-stu-id="89503-127">-Metric</span></span>
<span data-ttu-id="89503-128">Querys-Sammlung für die Definition von "viel Edge Deployment Metrics".</span><span class="sxs-lookup"><span data-stu-id="89503-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="89503-129">-Name</span><span class="sxs-lookup"><span data-stu-id="89503-129">-Name</span></span>
<span data-ttu-id="89503-130">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="89503-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="89503-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="89503-131">-Priority</span></span>
<span data-ttu-id="89503-132">Das Gewicht der Bereitstellung bei konkurrierenden Regeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="89503-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="89503-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89503-133">-ResourceGroupName</span></span>
<span data-ttu-id="89503-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="89503-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89503-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89503-135">-ResourceId</span></span>
<span data-ttu-id="89503-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="89503-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="89503-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="89503-137">-TargetCondition</span></span>
<span data-ttu-id="89503-138">Die zielbedingung, auf die eine Edge-Bereitstellung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89503-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="89503-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89503-139">-Confirm</span></span>
<span data-ttu-id="89503-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89503-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89503-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89503-141">-WhatIf</span></span>
<span data-ttu-id="89503-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89503-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89503-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89503-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89503-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89503-144">CommonParameters</span></span>
<span data-ttu-id="89503-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89503-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89503-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89503-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89503-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89503-147">INPUTS</span></span>

### <span data-ttu-id="89503-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="89503-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="89503-149">System. String</span><span class="sxs-lookup"><span data-stu-id="89503-149">System.String</span></span>

## <span data-ttu-id="89503-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89503-150">OUTPUTS</span></span>

### <span data-ttu-id="89503-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="89503-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="89503-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="89503-152">NOTES</span></span>

## <span data-ttu-id="89503-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89503-153">RELATED LINKS</span></span>
