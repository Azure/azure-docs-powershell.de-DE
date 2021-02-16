---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170501"
---
# <span data-ttu-id="36a43-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="36a43-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="36a43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a43-102">SYNOPSIS</span></span>
<span data-ttu-id="36a43-103">Rufen Sie eine metrische Abfrage für die Konfiguration eines IoT-Geräts auf.</span><span class="sxs-lookup"><span data-stu-id="36a43-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="36a43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36a43-104">SYNTAX</span></span>

### <span data-ttu-id="36a43-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36a43-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36a43-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36a43-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36a43-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36a43-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36a43-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36a43-108">DESCRIPTION</span></span>
<span data-ttu-id="36a43-109">Auswerten einer benutzerdefinierten Ziel- oder Systemmetrik, die in einer IoT-Gerätekonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="36a43-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="36a43-110">Es gibt vordefinierte Systemmetriken, die von Iot Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="36a43-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="36a43-111">"Targeted" gibt die Anzahl der Gerätegeräte an, die der Zielbedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="36a43-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="36a43-112">"Applied" hat die Anzahl der Gerätegeräte angegeben, die durch die Konfiguration geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="36a43-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="36a43-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36a43-113">EXAMPLES</span></span>

### <span data-ttu-id="36a43-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36a43-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="36a43-115">Werten Sie die benutzerdefinierte definierte Metrik "warningLimit" aus.</span><span class="sxs-lookup"><span data-stu-id="36a43-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="36a43-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="36a43-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="36a43-117">Werten Sie die Metrik "Angewendet" des Systems aus.</span><span class="sxs-lookup"><span data-stu-id="36a43-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="36a43-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a43-118">PARAMETERS</span></span>

### <span data-ttu-id="36a43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a43-119">-DefaultProfile</span></span>
<span data-ttu-id="36a43-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a43-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36a43-121">-InputObject</span></span>
<span data-ttu-id="36a43-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="36a43-122">IotHub object</span></span>

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

### <span data-ttu-id="36a43-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="36a43-123">-IotHubName</span></span>
<span data-ttu-id="36a43-124">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="36a43-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="36a43-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="36a43-125">-MetricName</span></span>
<span data-ttu-id="36a43-126">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="36a43-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="36a43-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="36a43-127">-MetricType</span></span>
<span data-ttu-id="36a43-128">Gibt an, welche metrische Sammlung zum Nachschlageen einer Metrik verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="36a43-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="36a43-129">-Name</span><span class="sxs-lookup"><span data-stu-id="36a43-129">-Name</span></span>
<span data-ttu-id="36a43-130">Id für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="36a43-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="36a43-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a43-131">-ResourceGroupName</span></span>
<span data-ttu-id="36a43-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="36a43-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="36a43-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36a43-133">-ResourceId</span></span>
<span data-ttu-id="36a43-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="36a43-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="36a43-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36a43-135">-Confirm</span></span>
<span data-ttu-id="36a43-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36a43-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a43-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36a43-137">-WhatIf</span></span>
<span data-ttu-id="36a43-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36a43-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a43-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36a43-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a43-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a43-140">CommonParameters</span></span>
<span data-ttu-id="36a43-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a43-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a43-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a43-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a43-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36a43-143">INPUTS</span></span>

### <span data-ttu-id="36a43-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="36a43-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="36a43-145">System.String</span><span class="sxs-lookup"><span data-stu-id="36a43-145">System.String</span></span>

## <span data-ttu-id="36a43-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36a43-146">OUTPUTS</span></span>

### <span data-ttu-id="36a43-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="36a43-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="36a43-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36a43-148">NOTES</span></span>

## <span data-ttu-id="36a43-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36a43-149">RELATED LINKS</span></span>
