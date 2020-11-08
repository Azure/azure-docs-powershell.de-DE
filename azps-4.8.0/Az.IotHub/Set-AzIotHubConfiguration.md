---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166448"
---
# <span data-ttu-id="467b0-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="467b0-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="467b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="467b0-102">SYNOPSIS</span></span>
<span data-ttu-id="467b0-103">Aktualisieren Sie die änderbaren Felder der Konfigurationsregistrierung.</span><span class="sxs-lookup"><span data-stu-id="467b0-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="467b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="467b0-104">SYNTAX</span></span>

### <span data-ttu-id="467b0-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="467b0-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="467b0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="467b0-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="467b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="467b0-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467b0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="467b0-108">DESCRIPTION</span></span>
<span data-ttu-id="467b0-109">Aktualisieren Sie die angegebenen Eigenschaften einer sehr viel automatischen Device Management-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="467b0-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="467b0-110">Hinweis: der Konfigurationsinhalt ist unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="467b0-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="467b0-111">Konfigurationseigenschaften, die aktualisiert werden können, sind "Beschriftungen", "Metriken", "Priorität" und "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="467b0-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="467b0-112">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management .</span><span class="sxs-lookup"><span data-stu-id="467b0-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="467b0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="467b0-113">EXAMPLES</span></span>

### <span data-ttu-id="467b0-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="467b0-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="467b0-115">Ändern der Priorität einer Gerätekonfiguration und Aktualisieren der zielbedingung</span><span class="sxs-lookup"><span data-stu-id="467b0-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="467b0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="467b0-116">PARAMETERS</span></span>

### <span data-ttu-id="467b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467b0-117">-DefaultProfile</span></span>
<span data-ttu-id="467b0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="467b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467b0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="467b0-119">-Force</span></span>
<span data-ttu-id="467b0-120">Ermöglicht das Ersetzen von Configuration-Objekten, auch wenn Sie seit dem letzten Abrufen aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="467b0-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="467b0-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="467b0-121">-InputObject</span></span>
<span data-ttu-id="467b0-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="467b0-122">IotHub object</span></span>

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

### <span data-ttu-id="467b0-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="467b0-123">-IotHubName</span></span>
<span data-ttu-id="467b0-124">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="467b0-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="467b0-125">-Label</span><span class="sxs-lookup"><span data-stu-id="467b0-125">-Label</span></span>
<span data-ttu-id="467b0-126">Karte der Beschriftungen, die auf die Zielkonfiguration angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="467b0-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="467b0-127">-Metric</span><span class="sxs-lookup"><span data-stu-id="467b0-127">-Metric</span></span>
<span data-ttu-id="467b0-128">Querys-Sammlung für die Definition von Konfigurations Metriken.</span><span class="sxs-lookup"><span data-stu-id="467b0-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="467b0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="467b0-129">-Name</span></span>
<span data-ttu-id="467b0-130">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="467b0-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="467b0-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="467b0-131">-Priority</span></span>
<span data-ttu-id="467b0-132">Die Gewichtung der Gerätekonfiguration bei konkurrierenden Regeln (höchste Gewinne).</span><span class="sxs-lookup"><span data-stu-id="467b0-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="467b0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467b0-133">-ResourceGroupName</span></span>
<span data-ttu-id="467b0-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="467b0-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="467b0-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="467b0-135">-ResourceId</span></span>
<span data-ttu-id="467b0-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="467b0-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="467b0-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="467b0-137">-TargetCondition</span></span>
<span data-ttu-id="467b0-138">Die zielbedingung, für die eine Gerätekonfiguration gilt.</span><span class="sxs-lookup"><span data-stu-id="467b0-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="467b0-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="467b0-139">-Confirm</span></span>
<span data-ttu-id="467b0-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="467b0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="467b0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467b0-141">-WhatIf</span></span>
<span data-ttu-id="467b0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="467b0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="467b0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="467b0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="467b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467b0-144">CommonParameters</span></span>
<span data-ttu-id="467b0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467b0-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467b0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467b0-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="467b0-147">INPUTS</span></span>

### <span data-ttu-id="467b0-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="467b0-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="467b0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="467b0-149">System.String</span></span>

## <span data-ttu-id="467b0-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="467b0-150">OUTPUTS</span></span>

### <span data-ttu-id="467b0-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="467b0-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="467b0-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="467b0-152">NOTES</span></span>

## <span data-ttu-id="467b0-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="467b0-153">RELATED LINKS</span></span>
