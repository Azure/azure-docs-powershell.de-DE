---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168788"
---
# <span data-ttu-id="d01a1-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d01a1-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="d01a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d01a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d01a1-103">Create new service fabric service under the specified application and cluster.</span><span class="sxs-lookup"><span data-stu-id="d01a1-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="d01a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d01a1-104">SYNTAX</span></span>

### <span data-ttu-id="d01a1-105">Stateless-Singleton (Standard)</span><span class="sxs-lookup"><span data-stu-id="d01a1-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d01a1-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="d01a1-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d01a1-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="d01a1-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01a1-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="d01a1-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01a1-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="d01a1-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01a1-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="d01a1-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d01a1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d01a1-111">DESCRIPTION</span></span>
<span data-ttu-id="d01a1-112">Dieses Cmdlet ermöglicht das Erstellen zustandsloser oder zustandsfreier Dienste unter der angegebenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d01a1-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="d01a1-113">Der Dienst sollte im Anwendungsmanifest beendet werden, und der Typ sollte mit dem typ im Manifest identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d01a1-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="d01a1-114">Der Anwendungsname sollte ein Präfix des Dienstnamens sein.</span><span class="sxs-lookup"><span data-stu-id="d01a1-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="d01a1-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d01a1-115">EXAMPLES</span></span>

### <span data-ttu-id="d01a1-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d01a1-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="d01a1-117">In diesem Beispiel wird der neue zustandslose Dienst "testApp~testService1" mit der Instanzenanzahl -1 (für alle Knoten) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d01a1-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="d01a1-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d01a1-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="d01a1-119">In diesem Beispiel wird der neue zustandsreiche Dienst "testApp~testService2" mit einem Ziel von 5 Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="d01a1-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="d01a1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d01a1-120">PARAMETERS</span></span>

### <span data-ttu-id="d01a1-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="d01a1-121">-ApplicationName</span></span>
<span data-ttu-id="d01a1-122">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d01a1-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d01a1-123">-ClusterName</span></span>
<span data-ttu-id="d01a1-124">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="d01a1-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="d01a1-125">-DefaultMoveCost</span></span>
<span data-ttu-id="d01a1-126">Geben Sie die Standardkosten für einen Verschiebezug an.</span><span class="sxs-lookup"><span data-stu-id="d01a1-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="d01a1-127">Höhere Kosten machen es weniger wahrscheinlich, dass der Clusterressourcen-Manager die Replikate verschiebt, wenn versucht wird, den Cluster zu ausgewogener</span><span class="sxs-lookup"><span data-stu-id="d01a1-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01a1-128">-DefaultProfile</span></span>
<span data-ttu-id="d01a1-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d01a1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01a1-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="d01a1-130">-InstanceCount</span></span>
<span data-ttu-id="d01a1-131">Angeben der Instanzenanzahl für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="d01a1-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="d01a1-133">Angeben der Mindestgröße des Replikats für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d01a1-134">-Name</span></span>
<span data-ttu-id="d01a1-135">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="d01a1-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="d01a1-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="d01a1-137">Gibt an, dass der Dienst das benannte Partitionsschema verwendet.</span><span class="sxs-lookup"><span data-stu-id="d01a1-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="d01a1-138">Dienste, die dieses Modell verwenden, enthalten in der Regel Daten, die innerhalb eines gebundenen Sets in bucketed werden können.</span><span class="sxs-lookup"><span data-stu-id="d01a1-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="d01a1-139">Einige häufige Beispiele für Datenfelder, die als benannte Partitionsschlüssel verwendet werden, sind Regionen, Postleitzahlen, Kundengruppen oder andere Geschäftsgrenzen.</span><span class="sxs-lookup"><span data-stu-id="d01a1-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="d01a1-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="d01a1-141">Gibt an, dass der Dienst das Partitionsschema des Singletons verwendet.</span><span class="sxs-lookup"><span data-stu-id="d01a1-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="d01a1-142">Singletonpartitionen werden in der Regel verwendet, wenn für den Dienst kein zusätzliches Routing erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d01a1-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="d01a1-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="d01a1-144">Gibt an, dass der Dienst das Partitionsschema "UniformInt64" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d01a1-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="d01a1-145">Dies bedeutet, dass jede Partition über einen Bereich von int64-Schlüsseln besitzt.</span><span class="sxs-lookup"><span data-stu-id="d01a1-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-146">-UmschließenLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="d01a1-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="d01a1-147">Angeben der Wartezeitdauer für den Verlust für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="d01a1-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="d01a1-149">Angeben der Dauer für den Neustart des Replikats für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01a1-150">-ResourceGroupName</span></span>
<span data-ttu-id="d01a1-151">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d01a1-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="d01a1-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="d01a1-153">Angeben der Dauer des Ständers nach Replikat für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="d01a1-154">-Stateful</span></span>
<span data-ttu-id="d01a1-155">Verwenden für zustandsreiche Dienste</span><span class="sxs-lookup"><span data-stu-id="d01a1-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="d01a1-156">-Stateless</span></span>
<span data-ttu-id="d01a1-157">Verwenden für zustandslose Dienste</span><span class="sxs-lookup"><span data-stu-id="d01a1-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="d01a1-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="d01a1-159">Angeben der Größe des Zielreplikates für den Dienst</span><span class="sxs-lookup"><span data-stu-id="d01a1-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-160">-Type</span><span class="sxs-lookup"><span data-stu-id="d01a1-160">-Type</span></span>
<span data-ttu-id="d01a1-161">Geben Sie den Diensttypnamen der Anwendung an, der im Anwendungsmanifest vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="d01a1-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01a1-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d01a1-162">-Confirm</span></span>
<span data-ttu-id="d01a1-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d01a1-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01a1-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d01a1-164">-WhatIf</span></span>
<span data-ttu-id="d01a1-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d01a1-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d01a1-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d01a1-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01a1-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01a1-167">CommonParameters</span></span>
<span data-ttu-id="d01a1-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01a1-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01a1-169">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d01a1-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01a1-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d01a1-170">INPUTS</span></span>

### <span data-ttu-id="d01a1-171">System.String</span><span class="sxs-lookup"><span data-stu-id="d01a1-171">System.String</span></span>

## <span data-ttu-id="d01a1-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d01a1-172">OUTPUTS</span></span>

### <span data-ttu-id="d01a1-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="d01a1-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="d01a1-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d01a1-174">NOTES</span></span>

## <span data-ttu-id="d01a1-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d01a1-175">RELATED LINKS</span></span>
