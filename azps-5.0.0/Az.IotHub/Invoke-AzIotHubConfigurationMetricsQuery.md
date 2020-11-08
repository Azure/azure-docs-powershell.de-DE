---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180474"
---
# <span data-ttu-id="81b17-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="81b17-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="81b17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81b17-102">SYNOPSIS</span></span>
<span data-ttu-id="81b17-103">Rufen Sie eine Abfrage mit einer sehr viel Device Configuration-Metrik auf.</span><span class="sxs-lookup"><span data-stu-id="81b17-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="81b17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81b17-104">SYNTAX</span></span>

### <span data-ttu-id="81b17-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="81b17-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81b17-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="81b17-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81b17-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="81b17-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81b17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81b17-108">DESCRIPTION</span></span>
<span data-ttu-id="81b17-109">Bewerten Sie eine Zielbenutzer definierte oder System Metrik, die in einer viel Gerätekonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="81b17-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="81b17-110">Es gibt vordefinierte System Metriken, die von viel Hub berechnet werden und nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="81b17-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="81b17-111">"Targeted" gibt die Anzahl der Geräte Zwillinge an, die der zielbedingung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="81b17-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="81b17-112">"Angewendet" hat die Anzahl der Geräte Zwillinge angegeben, die von der Konfiguration geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="81b17-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="81b17-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81b17-113">EXAMPLES</span></span>

### <span data-ttu-id="81b17-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81b17-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="81b17-115">Werten Sie die benutzerdefinierte "warningLimit"-Metrik aus.</span><span class="sxs-lookup"><span data-stu-id="81b17-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="81b17-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81b17-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="81b17-117">Bewerten Sie die "Angewandte" Metrik des Systems.</span><span class="sxs-lookup"><span data-stu-id="81b17-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="81b17-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="81b17-118">PARAMETERS</span></span>

### <span data-ttu-id="81b17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b17-119">-DefaultProfile</span></span>
<span data-ttu-id="81b17-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81b17-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b17-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81b17-121">-InputObject</span></span>
<span data-ttu-id="81b17-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="81b17-122">IotHub object</span></span>

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

### <span data-ttu-id="81b17-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="81b17-123">-IotHubName</span></span>
<span data-ttu-id="81b17-124">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="81b17-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="81b17-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="81b17-125">-MetricName</span></span>
<span data-ttu-id="81b17-126">Zielmetrik für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="81b17-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="81b17-127">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="81b17-127">-MetricType</span></span>
<span data-ttu-id="81b17-128">Gibt an, welche metrische Sammlung verwendet werden soll, um eine Metrik zu suchen.</span><span class="sxs-lookup"><span data-stu-id="81b17-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="81b17-129">-Name</span><span class="sxs-lookup"><span data-stu-id="81b17-129">-Name</span></span>
<span data-ttu-id="81b17-130">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81b17-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="81b17-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b17-131">-ResourceGroupName</span></span>
<span data-ttu-id="81b17-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="81b17-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="81b17-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="81b17-133">-ResourceId</span></span>
<span data-ttu-id="81b17-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="81b17-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="81b17-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81b17-135">-Confirm</span></span>
<span data-ttu-id="81b17-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81b17-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b17-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b17-137">-WhatIf</span></span>
<span data-ttu-id="81b17-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81b17-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b17-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81b17-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b17-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b17-140">CommonParameters</span></span>
<span data-ttu-id="81b17-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b17-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b17-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b17-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b17-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81b17-143">INPUTS</span></span>

### <span data-ttu-id="81b17-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="81b17-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="81b17-145">System. String</span><span class="sxs-lookup"><span data-stu-id="81b17-145">System.String</span></span>

## <span data-ttu-id="81b17-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81b17-146">OUTPUTS</span></span>

### <span data-ttu-id="81b17-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="81b17-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="81b17-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="81b17-148">NOTES</span></span>

## <span data-ttu-id="81b17-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81b17-149">RELATED LINKS</span></span>
