---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004453"
---
# <span data-ttu-id="6513f-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="6513f-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="6513f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6513f-102">SYNOPSIS</span></span>
<span data-ttu-id="6513f-103">Fügen Sie eine sehr viele automatische Geräte Verwaltungskonfiguration in einem Ziel-viel-Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="6513f-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="6513f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6513f-104">SYNTAX</span></span>

### <span data-ttu-id="6513f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6513f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6513f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6513f-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6513f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6513f-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6513f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6513f-108">DESCRIPTION</span></span>
<span data-ttu-id="6513f-109">Konfigurationsinhalte sind JSON-und geringfügig unterschiedlich, je nach Geräte-oder Modul Absicht.</span><span class="sxs-lookup"><span data-stu-id="6513f-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="6513f-110">Gerätekonfigurationen sind in der Form {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="6513f-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="6513f-111">Modul Konfigurationen sind in der Form {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="6513f-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="6513f-112">Konfigurationen können mit vom Benutzer bereitgestellten Metriken für die bedarfsgesteuerte Auswertung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6513f-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="6513f-113">Benutzer Metriken sind JSON und in Form von {"Abfragen": {...}}</span><span class="sxs-lookup"><span data-stu-id="6513f-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="6513f-114">oder {"Metriken": {"Abfragen": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="6513f-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="6513f-115">Hinweis: die zielbedingung für Module muss mit "from Devices. modules where" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6513f-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="6513f-116">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management .</span><span class="sxs-lookup"><span data-stu-id="6513f-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="6513f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6513f-117">EXAMPLES</span></span>

### <span data-ttu-id="6513f-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6513f-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="6513f-119">Erstellen Sie eine Gerätekonfiguration mit Standardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="6513f-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="6513f-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6513f-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="6513f-121">Erstellen Sie eine Gerätekonfiguration mit einer Priorität von 3, die unter Bedingung gilt, wenn ein Gerät in Gebäude 9 markiert ist und die Umgebung "testen" lautet.</span><span class="sxs-lookup"><span data-stu-id="6513f-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="6513f-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6513f-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="6513f-123">Erstellen Sie eine Gerätekonfiguration mit Benutzer Metriken.</span><span class="sxs-lookup"><span data-stu-id="6513f-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="6513f-124">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6513f-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="6513f-125">Erstellen Sie eine Gerätekonfiguration mit Etiketten.</span><span class="sxs-lookup"><span data-stu-id="6513f-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="6513f-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="6513f-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="6513f-127">Erstellen Sie eine Gerätekonfiguration mit Inhalt.</span><span class="sxs-lookup"><span data-stu-id="6513f-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="6513f-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="6513f-128">PARAMETERS</span></span>

### <span data-ttu-id="6513f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6513f-129">-DefaultProfile</span></span>
<span data-ttu-id="6513f-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6513f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6513f-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="6513f-131">-DeviceContent</span></span>
<span data-ttu-id="6513f-132">Konfiguration für IotHub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="6513f-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="6513f-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6513f-133">-InputObject</span></span>
<span data-ttu-id="6513f-134">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="6513f-134">IotHub object</span></span>

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

### <span data-ttu-id="6513f-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6513f-135">-IotHubName</span></span>
<span data-ttu-id="6513f-136">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="6513f-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6513f-137">-Label</span><span class="sxs-lookup"><span data-stu-id="6513f-137">-Label</span></span>
<span data-ttu-id="6513f-138">Karte der Beschriftungen, die auf die Zielkonfiguration angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6513f-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="6513f-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="6513f-139">-Metric</span></span>
<span data-ttu-id="6513f-140">Querys-Sammlung für die Definition von Konfigurations Metriken.</span><span class="sxs-lookup"><span data-stu-id="6513f-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="6513f-141">-Name</span><span class="sxs-lookup"><span data-stu-id="6513f-141">-Name</span></span>
<span data-ttu-id="6513f-142">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6513f-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="6513f-143">-Priorität</span><span class="sxs-lookup"><span data-stu-id="6513f-143">-Priority</span></span>
<span data-ttu-id="6513f-144">Die Gewichtung der Gerätekonfiguration bei konkurrierenden Regeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="6513f-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="6513f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6513f-145">-ResourceGroupName</span></span>
<span data-ttu-id="6513f-146">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6513f-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6513f-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6513f-147">-ResourceId</span></span>
<span data-ttu-id="6513f-148">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6513f-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6513f-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="6513f-149">-TargetCondition</span></span>
<span data-ttu-id="6513f-150">Die zielbedingung, für die eine Gerätekonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="6513f-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="6513f-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6513f-151">-Confirm</span></span>
<span data-ttu-id="6513f-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6513f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6513f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6513f-153">-WhatIf</span></span>
<span data-ttu-id="6513f-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6513f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6513f-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6513f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6513f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6513f-156">CommonParameters</span></span>
<span data-ttu-id="6513f-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6513f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6513f-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6513f-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6513f-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6513f-159">INPUTS</span></span>

### <span data-ttu-id="6513f-160">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6513f-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6513f-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6513f-161">System.String</span></span>

## <span data-ttu-id="6513f-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6513f-162">OUTPUTS</span></span>

### <span data-ttu-id="6513f-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="6513f-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="6513f-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="6513f-164">NOTES</span></span>

## <span data-ttu-id="6513f-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6513f-165">RELATED LINKS</span></span>
