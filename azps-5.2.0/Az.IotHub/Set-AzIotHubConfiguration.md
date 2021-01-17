---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302784"
---
# <span data-ttu-id="9126e-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="9126e-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="9126e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9126e-102">SYNOPSIS</span></span>
<span data-ttu-id="9126e-103">Aktualisieren Sie die schaltbaren Felder der Konfigurationsregistrierung.</span><span class="sxs-lookup"><span data-stu-id="9126e-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="9126e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9126e-104">SYNTAX</span></span>

### <span data-ttu-id="9126e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9126e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9126e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9126e-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9126e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9126e-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9126e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9126e-108">DESCRIPTION</span></span>
<span data-ttu-id="9126e-109">Aktualisieren der angegebenen Eigenschaften einer automatischen Geräteverwaltungskonfiguration des IoT</span><span class="sxs-lookup"><span data-stu-id="9126e-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="9126e-110">Hinweis: Der Konfigurationsinhalt kann nicht stumm änderbar sein.</span><span class="sxs-lookup"><span data-stu-id="9126e-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="9126e-111">Zu den Konfigurationseigenschaften, die aktualisiert werden können, gehören "Bezeichnungen", "Metriken", "Priorität" und "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="9126e-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="9126e-112">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="9126e-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="9126e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9126e-113">EXAMPLES</span></span>

### <span data-ttu-id="9126e-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9126e-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="9126e-115">Ändern der Priorität einer Gerätekonfiguration und Aktualisieren der Zielbedingung</span><span class="sxs-lookup"><span data-stu-id="9126e-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="9126e-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9126e-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="9126e-117">Aktualisieren der Metriken und Bezeichnungen einer Gerätekonfiguration</span><span class="sxs-lookup"><span data-stu-id="9126e-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="9126e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9126e-118">PARAMETERS</span></span>

### <span data-ttu-id="9126e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9126e-119">-DefaultProfile</span></span>
<span data-ttu-id="9126e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9126e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9126e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9126e-121">-Force</span></span>
<span data-ttu-id="9126e-122">Ermöglicht das Ersetzen von Konfigurationsobjekten, auch wenn es seit dem letzten Abruf aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9126e-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="9126e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9126e-123">-InputObject</span></span>
<span data-ttu-id="9126e-124">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="9126e-124">IotHub object</span></span>

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

### <span data-ttu-id="9126e-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9126e-125">-IotHubName</span></span>
<span data-ttu-id="9126e-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="9126e-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9126e-127">-Label</span><span class="sxs-lookup"><span data-stu-id="9126e-127">-Label</span></span>
<span data-ttu-id="9126e-128">Karte der Bezeichnungen, die auf die Zielkonfiguration angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9126e-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="9126e-129">-metrisch</span><span class="sxs-lookup"><span data-stu-id="9126e-129">-Metric</span></span>
<span data-ttu-id="9126e-130">Sammlung von Abfragen für die Definition von Konfigurationsmetriken.</span><span class="sxs-lookup"><span data-stu-id="9126e-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="9126e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9126e-131">-Name</span></span>
<span data-ttu-id="9126e-132">Id für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9126e-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9126e-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="9126e-133">-Priority</span></span>
<span data-ttu-id="9126e-134">Gewichtung der Gerätekonfiguration bei Konkurrenzregeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="9126e-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="9126e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9126e-135">-ResourceGroupName</span></span>
<span data-ttu-id="9126e-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9126e-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9126e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9126e-137">-ResourceId</span></span>
<span data-ttu-id="9126e-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="9126e-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9126e-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="9126e-139">-TargetCondition</span></span>
<span data-ttu-id="9126e-140">Zielbedingung, für die eine Gerätekonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="9126e-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="9126e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9126e-141">-Confirm</span></span>
<span data-ttu-id="9126e-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9126e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9126e-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9126e-143">-WhatIf</span></span>
<span data-ttu-id="9126e-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9126e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9126e-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9126e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9126e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9126e-146">CommonParameters</span></span>
<span data-ttu-id="9126e-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9126e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9126e-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9126e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9126e-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9126e-149">INPUTS</span></span>

### <span data-ttu-id="9126e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9126e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9126e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9126e-151">System.String</span></span>

## <span data-ttu-id="9126e-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9126e-152">OUTPUTS</span></span>

### <span data-ttu-id="9126e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="9126e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="9126e-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9126e-154">NOTES</span></span>

## <span data-ttu-id="9126e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9126e-155">RELATED LINKS</span></span>
