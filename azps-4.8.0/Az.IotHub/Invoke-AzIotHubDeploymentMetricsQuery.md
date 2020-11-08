---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175125"
---
# <span data-ttu-id="b1b37-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="b1b37-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="b1b37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1b37-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b37-103">Rufen Sie eine sehr viel Edge Deployment Metric-Abfrage auf.</span><span class="sxs-lookup"><span data-stu-id="b1b37-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="b1b37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b37-104">SYNTAX</span></span>

### <span data-ttu-id="b1b37-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1b37-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b37-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1b37-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b37-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1b37-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1b37-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b37-108">DESCRIPTION</span></span>
<span data-ttu-id="b1b37-109">Bewerten Sie eine Zielbenutzer definierte oder System Metrik, die in einer viel Edge-Bereitstellung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1b37-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="b1b37-110">Es gibt vordefinierte System Metriken, die von viel Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="b1b37-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="b1b37-111">"Targeted" zeigt die viel Edge-Geräte an, die der Bereitstellungsziel Bedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b1b37-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="b1b37-112">"Angewendet" zeigt die gezielten vielseitigen Geräte an, die nicht von einer anderen Bereitstellung mit höherer Priorität abzielen.</span><span class="sxs-lookup"><span data-stu-id="b1b37-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="b1b37-113">"Berichts Erfolg" zeigt die viel Edge-Geräte, die berichteten, dass die Module erfolgreich bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b1b37-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="b1b37-114">"Fehler bei der Meldung" zeigt die vielseitigen Geräte an, die gemeldet haben, dass ein oder mehrere Module nicht erfolgreich bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b1b37-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="b1b37-115">Wenn Sie den Fehler weiter untersuchen möchten, stellen Sie eine Remoteverbindung mit diesen Geräten her, und zeigen Sie die Protokolldateien an.</span><span class="sxs-lookup"><span data-stu-id="b1b37-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="b1b37-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1b37-116">EXAMPLES</span></span>

### <span data-ttu-id="b1b37-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1b37-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="b1b37-118">Werten Sie die benutzerdefinierte "warningLimit"-Metrik aus.</span><span class="sxs-lookup"><span data-stu-id="b1b37-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="b1b37-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b1b37-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="b1b37-120">Bewerten Sie die Metrik des Systems "Berichts Erfolg".</span><span class="sxs-lookup"><span data-stu-id="b1b37-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="b1b37-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b37-121">PARAMETERS</span></span>

### <span data-ttu-id="b1b37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b37-122">-DefaultProfile</span></span>
<span data-ttu-id="b1b37-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1b37-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b37-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1b37-124">-InputObject</span></span>
<span data-ttu-id="b1b37-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1b37-125">IotHub object</span></span>

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

### <span data-ttu-id="b1b37-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b1b37-126">-IotHubName</span></span>
<span data-ttu-id="b1b37-127">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b1b37-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b1b37-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="b1b37-128">-MetricName</span></span>
<span data-ttu-id="b1b37-129">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="b1b37-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="b1b37-130">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="b1b37-130">-MetricType</span></span>
<span data-ttu-id="b1b37-131">Gibt an, welche metrische Sammlung verwendet werden soll, um eine Metrik zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b1b37-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="b1b37-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b1b37-132">-Name</span></span>
<span data-ttu-id="b1b37-133">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b1b37-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b1b37-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b37-134">-ResourceGroupName</span></span>
<span data-ttu-id="b1b37-135">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b1b37-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b1b37-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b1b37-136">-ResourceId</span></span>
<span data-ttu-id="b1b37-137">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b1b37-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b1b37-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1b37-138">-Confirm</span></span>
<span data-ttu-id="b1b37-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1b37-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b37-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b37-140">-WhatIf</span></span>
<span data-ttu-id="b1b37-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1b37-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b37-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1b37-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b37-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b37-143">CommonParameters</span></span>
<span data-ttu-id="b1b37-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b37-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b37-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b37-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b37-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1b37-146">INPUTS</span></span>

### <span data-ttu-id="b1b37-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b1b37-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b1b37-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b1b37-148">System.String</span></span>

## <span data-ttu-id="b1b37-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1b37-149">OUTPUTS</span></span>

### <span data-ttu-id="b1b37-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="b1b37-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="b1b37-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1b37-151">NOTES</span></span>

## <span data-ttu-id="b1b37-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1b37-152">RELATED LINKS</span></span>
