---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167348"
---
# <span data-ttu-id="a5eaa-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="a5eaa-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="a5eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="a5eaa-103">Rufen Sie eine metrische Abfrage für die Bereitstellung von IoT Edge auf.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="a5eaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5eaa-104">SYNTAX</span></span>

### <span data-ttu-id="a5eaa-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5eaa-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5eaa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5eaa-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5eaa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a5eaa-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5eaa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5eaa-108">DESCRIPTION</span></span>
<span data-ttu-id="a5eaa-109">Auswerten einer benutzerdefinierten Ziel- oder Systemmetrik, die in einer IoT -Edge-Bereitstellung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="a5eaa-110">Es gibt vordefinierte Systemmetriken, die von Iot Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="a5eaa-111">"Gezielt" zeigt die IoT Edge-Geräte, die der Bereitstellungszielbedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="a5eaa-112">"Angewendet" zeigt die gezielten IoT-Edge-Geräte an, die nicht auf eine andere Bereitstellung mit höherer Priorität ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="a5eaa-113">"Melden des Erfolgs" zeigt die IoT-Edge-Geräte, die gemeldet haben, dass die Module erfolgreich bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="a5eaa-114">"Fehler melden" zeigt die IoT-Edge-Geräte, die gemeldet haben, dass ein oder mehrere Module nicht erfolgreich bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="a5eaa-115">Um den Fehler weiter zu untersuchen, stellen Sie remote eine Verbindung mit diesen Geräten herzustellen und die Protokolldateien an.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="a5eaa-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5eaa-116">EXAMPLES</span></span>

### <span data-ttu-id="a5eaa-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5eaa-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="a5eaa-118">Werten Sie die benutzerdefinierte definierte Metrik "warningLimit" aus.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="a5eaa-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5eaa-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="a5eaa-120">Bewerten Sie die Systemmetrik "Berichterstellungserfolg".</span><span class="sxs-lookup"><span data-stu-id="a5eaa-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="a5eaa-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5eaa-121">PARAMETERS</span></span>

### <span data-ttu-id="a5eaa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5eaa-122">-DefaultProfile</span></span>
<span data-ttu-id="a5eaa-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5eaa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5eaa-124">-InputObject</span></span>
<span data-ttu-id="a5eaa-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="a5eaa-125">IotHub object</span></span>

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

### <span data-ttu-id="a5eaa-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a5eaa-126">-IotHubName</span></span>
<span data-ttu-id="a5eaa-127">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="a5eaa-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a5eaa-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="a5eaa-128">-MetricName</span></span>
<span data-ttu-id="a5eaa-129">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="a5eaa-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="a5eaa-130">-MetricType</span></span>
<span data-ttu-id="a5eaa-131">Gibt an, welche metrische Sammlung zum Nachschlageen einer Metrik verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="a5eaa-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a5eaa-132">-Name</span></span>
<span data-ttu-id="a5eaa-133">Id für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="a5eaa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5eaa-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5eaa-135">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a5eaa-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a5eaa-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5eaa-136">-ResourceId</span></span>
<span data-ttu-id="a5eaa-137">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a5eaa-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a5eaa-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5eaa-138">-Confirm</span></span>
<span data-ttu-id="a5eaa-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5eaa-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5eaa-140">-WhatIf</span></span>
<span data-ttu-id="a5eaa-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5eaa-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5eaa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5eaa-143">CommonParameters</span></span>
<span data-ttu-id="a5eaa-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5eaa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5eaa-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5eaa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5eaa-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5eaa-146">INPUTS</span></span>

### <span data-ttu-id="a5eaa-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a5eaa-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a5eaa-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a5eaa-148">System.String</span></span>

## <span data-ttu-id="a5eaa-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5eaa-149">OUTPUTS</span></span>

### <span data-ttu-id="a5eaa-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="a5eaa-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="a5eaa-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5eaa-151">NOTES</span></span>

## <span data-ttu-id="a5eaa-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5eaa-152">RELATED LINKS</span></span>
