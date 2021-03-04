---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 02870d2bf0016704328e157b948b9db8ae1207f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924104"
---
# <span data-ttu-id="e9e69-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="e9e69-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="e9e69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e69-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e69-103">Rufen Sie eine IoT Edge-Bereitstellungsmetrikabfrage auf.</span><span class="sxs-lookup"><span data-stu-id="e9e69-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="e9e69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9e69-104">SYNTAX</span></span>

### <span data-ttu-id="e9e69-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9e69-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e69-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9e69-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9e69-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e9e69-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9e69-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9e69-108">DESCRIPTION</span></span>
<span data-ttu-id="e9e69-109">Auswerten einer benutzerdefinierten Zielmetrik oder Systemmetrik, die in einer IoT Edge-Bereitstellung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e9e69-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="e9e69-110">Es gibt vordefinierte Systemmetriken, die von Iot Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="e9e69-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="e9e69-111">"Gezielt" zeigt die IoT Edge-Geräte an, die der Bereitstellungszielbedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e9e69-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="e9e69-112">"Angewendet" zeigt die gezielten IoT Edge-Geräte an, die nicht auf eine andere Bereitstellung mit höherer Priorität ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="e9e69-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="e9e69-113">"Berichterstellungserfolg" zeigt die IoT Edge-Geräte, die berichtet haben, dass die Module erfolgreich bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e9e69-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="e9e69-114">"Berichtsfehler" zeigt die IoT Edge-Geräte, die gemeldet haben, dass mindestens ein Modul nicht erfolgreich bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9e69-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="e9e69-115">Um den Fehler weiter zu untersuchen, stellen Sie eine Remoteverbindung mit diesen Geräten ein, und zeigen Sie die Protokolldateien an.</span><span class="sxs-lookup"><span data-stu-id="e9e69-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="e9e69-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9e69-116">EXAMPLES</span></span>

### <span data-ttu-id="e9e69-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9e69-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="e9e69-118">Werten Sie die benutzerdefinierte definierte Metrik "warningLimit" aus.</span><span class="sxs-lookup"><span data-stu-id="e9e69-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="e9e69-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e9e69-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="e9e69-120">Bewerten Sie die Metrik "Berichterstellungserfolg" des Systems.</span><span class="sxs-lookup"><span data-stu-id="e9e69-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="e9e69-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9e69-121">PARAMETERS</span></span>

### <span data-ttu-id="e9e69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e69-122">-DefaultProfile</span></span>
<span data-ttu-id="e9e69-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9e69-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e69-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9e69-124">-InputObject</span></span>
<span data-ttu-id="e9e69-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e9e69-125">IotHub object</span></span>

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

### <span data-ttu-id="e9e69-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e9e69-126">-IotHubName</span></span>
<span data-ttu-id="e9e69-127">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="e9e69-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e9e69-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e9e69-128">-MetricName</span></span>
<span data-ttu-id="e9e69-129">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="e9e69-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="e9e69-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="e9e69-130">-MetricType</span></span>
<span data-ttu-id="e9e69-131">Gibt an, welche Metriksammlung zum Nachschlageen einer Metrik verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9e69-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="e9e69-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e9e69-132">-Name</span></span>
<span data-ttu-id="e9e69-133">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e9e69-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="e9e69-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9e69-134">-ResourceGroupName</span></span>
<span data-ttu-id="e9e69-135">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e9e69-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e9e69-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e69-136">-ResourceId</span></span>
<span data-ttu-id="e9e69-137">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e9e69-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e9e69-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9e69-138">-Confirm</span></span>
<span data-ttu-id="e9e69-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9e69-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e69-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e69-140">-WhatIf</span></span>
<span data-ttu-id="e9e69-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9e69-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e69-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9e69-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e69-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e69-143">CommonParameters</span></span>
<span data-ttu-id="e9e69-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e69-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e69-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e69-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e69-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e69-146">INPUTS</span></span>

### <span data-ttu-id="e9e69-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e9e69-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e9e69-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e9e69-148">System.String</span></span>

## <span data-ttu-id="e9e69-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e69-149">OUTPUTS</span></span>

### <span data-ttu-id="e9e69-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="e9e69-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="e9e69-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e9e69-151">NOTES</span></span>

## <span data-ttu-id="e9e69-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e9e69-152">RELATED LINKS</span></span>
