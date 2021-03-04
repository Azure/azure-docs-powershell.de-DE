---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 07772e7d0cbec3a2cd8241de3afa0100e1c253cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924112"
---
# <span data-ttu-id="92807-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="92807-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="92807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92807-102">SYNOPSIS</span></span>
<span data-ttu-id="92807-103">Rufen Sie eine Metrikabfrage für die IoT-Gerätekonfiguration auf.</span><span class="sxs-lookup"><span data-stu-id="92807-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="92807-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92807-104">SYNTAX</span></span>

### <span data-ttu-id="92807-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92807-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92807-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92807-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92807-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92807-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92807-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92807-108">DESCRIPTION</span></span>
<span data-ttu-id="92807-109">Auswerten einer benutzerdefinierten Zielmetrik oder Systemmetrik, die in einer IoT-Gerätekonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92807-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="92807-110">Es gibt vordefinierte Systemmetriken, die von Iot Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="92807-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="92807-111">"Gezielt" gibt die Anzahl der Gerätezungen an, die der Zielbedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="92807-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="92807-112">"Angewendet" hat die Anzahl der Gerätezungen angegeben, die von der Konfiguration geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="92807-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="92807-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92807-113">EXAMPLES</span></span>

### <span data-ttu-id="92807-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92807-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="92807-115">Werten Sie die benutzerdefinierte definierte Metrik "warningLimit" aus.</span><span class="sxs-lookup"><span data-stu-id="92807-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="92807-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92807-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="92807-117">Werten Sie die Metrik "angewendet" des Systems aus.</span><span class="sxs-lookup"><span data-stu-id="92807-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="92807-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92807-118">PARAMETERS</span></span>

### <span data-ttu-id="92807-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92807-119">-DefaultProfile</span></span>
<span data-ttu-id="92807-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92807-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92807-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92807-121">-InputObject</span></span>
<span data-ttu-id="92807-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="92807-122">IotHub object</span></span>

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

### <span data-ttu-id="92807-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="92807-123">-IotHubName</span></span>
<span data-ttu-id="92807-124">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="92807-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="92807-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="92807-125">-MetricName</span></span>
<span data-ttu-id="92807-126">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="92807-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="92807-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="92807-127">-MetricType</span></span>
<span data-ttu-id="92807-128">Gibt an, welche Metriksammlung zum Nachschlageen einer Metrik verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="92807-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92807-129">-Name</span><span class="sxs-lookup"><span data-stu-id="92807-129">-Name</span></span>
<span data-ttu-id="92807-130">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="92807-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="92807-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92807-131">-ResourceGroupName</span></span>
<span data-ttu-id="92807-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="92807-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92807-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92807-133">-ResourceId</span></span>
<span data-ttu-id="92807-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="92807-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="92807-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92807-135">-Confirm</span></span>
<span data-ttu-id="92807-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92807-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92807-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92807-137">-WhatIf</span></span>
<span data-ttu-id="92807-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92807-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92807-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92807-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92807-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92807-140">CommonParameters</span></span>
<span data-ttu-id="92807-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92807-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92807-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92807-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92807-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92807-143">INPUTS</span></span>

### <span data-ttu-id="92807-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="92807-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="92807-145">System.String</span><span class="sxs-lookup"><span data-stu-id="92807-145">System.String</span></span>

## <span data-ttu-id="92807-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92807-146">OUTPUTS</span></span>

### <span data-ttu-id="92807-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="92807-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="92807-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92807-148">NOTES</span></span>

## <span data-ttu-id="92807-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92807-149">RELATED LINKS</span></span>
