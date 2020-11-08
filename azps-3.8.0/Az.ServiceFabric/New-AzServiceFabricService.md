---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: c4a082847c8d86271d7ded5d03f9c7c27c00501b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996423"
---
# <span data-ttu-id="6b390-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6b390-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="6b390-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b390-102">SYNOPSIS</span></span>
<span data-ttu-id="6b390-103">Erstellen eines neuen Service Fabric-Diensts unter der angegebenen Anwendung und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="6b390-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="6b390-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b390-104">SYNTAX</span></span>

### <span data-ttu-id="6b390-105">Stateless-Singleton (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b390-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b390-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="6b390-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b390-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="6b390-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b390-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="6b390-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b390-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="6b390-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b390-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="6b390-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b390-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b390-111">DESCRIPTION</span></span>
<span data-ttu-id="6b390-112">Dieses Cmdlet ermöglicht das Erstellen von statuslosen oder statusbehafteten Diensten unter der angegebenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6b390-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="6b390-113">Der Dienst sollte im Anwendungsmanifest beendet werden, und der Typ sollte mit dem im Manifest identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6b390-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="6b390-114">Der Anwendungsname sollte ein Präfix des Dienst namens sein.</span><span class="sxs-lookup"><span data-stu-id="6b390-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="6b390-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b390-115">EXAMPLES</span></span>

### <span data-ttu-id="6b390-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b390-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="6b390-117">In diesem Beispiel wird ein neuer zustandslosen Dienst "testApp ~ testService1" mit instanzenanzahl-1 (auf allen Knoten) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b390-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="6b390-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6b390-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="6b390-119">In diesem Beispiel wird ein neuer statusbehafteter Dienst "testApp ~ testService2" mit einem Ziel von 5 Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b390-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="6b390-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b390-120">PARAMETERS</span></span>

### <span data-ttu-id="6b390-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6b390-121">-ApplicationName</span></span>
<span data-ttu-id="6b390-122">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="6b390-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="6b390-123">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6b390-123">-ClusterName</span></span>
<span data-ttu-id="6b390-124">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6b390-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6b390-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="6b390-125">-DefaultMoveCost</span></span>
<span data-ttu-id="6b390-126">Legen Sie die Standardkosten für einen Umzug fest.</span><span class="sxs-lookup"><span data-stu-id="6b390-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="6b390-127">Höhere Kosten machen es unwahrscheinlicher, dass der Clusterressourcen-Manager das Replikat beim Ausgleichen des Clusters verschiebt.</span><span class="sxs-lookup"><span data-stu-id="6b390-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="6b390-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b390-128">-DefaultProfile</span></span>
<span data-ttu-id="6b390-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b390-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b390-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6b390-130">-InstanceCount</span></span>
<span data-ttu-id="6b390-131">Angeben der instanzenanzahl für den Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="6b390-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="6b390-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="6b390-133">Angeben der minimalen Replikatsatz Größe für den Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="6b390-134">-Name</span><span class="sxs-lookup"><span data-stu-id="6b390-134">-Name</span></span>
<span data-ttu-id="6b390-135">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="6b390-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="6b390-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="6b390-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="6b390-137">Gibt an, dass der Dienst das benannte Partitionsschema verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b390-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="6b390-138">Für Dienste, die dieses Modell verwenden, gibt es in der Regel Daten, die in einem begrenzten Satz bucketed werden können.</span><span class="sxs-lookup"><span data-stu-id="6b390-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="6b390-139">Einige häufige Beispiele für Datenfelder, die als benannte Partitionsschlüssel verwendet werden, sind Regionen, Postleitzahlen, Kundengruppen oder andere Unternehmensgrenzen.</span><span class="sxs-lookup"><span data-stu-id="6b390-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="6b390-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="6b390-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="6b390-141">Gibt an, dass der Dienst das Singleton-Partitionsschema verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b390-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="6b390-142">Singleton-Partitionen werden in der Regel verwendet, wenn der Dienst kein zusätzliches Routing erfordert.</span><span class="sxs-lookup"><span data-stu-id="6b390-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="6b390-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="6b390-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="6b390-144">Gibt an, dass der Dienst das UniformInt64-Partitionsschema verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b390-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="6b390-145">Das bedeutet, dass jede Partition einen Bereich von Int64-Schlüsseln besitzt.</span><span class="sxs-lookup"><span data-stu-id="6b390-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="6b390-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="6b390-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="6b390-147">Angeben der Wartezeit für den Quorum Verlust für den Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="6b390-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="6b390-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="6b390-149">Angeben der Wartedauer für den Replikat Neustart für den Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="6b390-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b390-150">-ResourceGroupName</span></span>
<span data-ttu-id="6b390-151">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6b390-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6b390-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="6b390-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="6b390-153">Angeben der Dauer für den Stand nach Replikat des Diensts</span><span class="sxs-lookup"><span data-stu-id="6b390-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="6b390-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="6b390-154">-Stateful</span></span>
<span data-ttu-id="6b390-155">Verwenden für statusbehafteten Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-155">Use for stateful service</span></span>

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

### <span data-ttu-id="6b390-156">-Statuslos</span><span class="sxs-lookup"><span data-stu-id="6b390-156">-Stateless</span></span>
<span data-ttu-id="6b390-157">Verwenden für statuslosen Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-157">Use for stateless service</span></span>

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

### <span data-ttu-id="6b390-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="6b390-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="6b390-159">Angeben der Zielreplikat Satz Größe für den Dienst</span><span class="sxs-lookup"><span data-stu-id="6b390-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="6b390-160">-Typ</span><span class="sxs-lookup"><span data-stu-id="6b390-160">-Type</span></span>
<span data-ttu-id="6b390-161">Geben Sie den Namen des Diensttyps der Anwendung an, der im Anwendungsmanifest vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="6b390-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="6b390-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b390-162">-Confirm</span></span>
<span data-ttu-id="6b390-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b390-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b390-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b390-164">-WhatIf</span></span>
<span data-ttu-id="6b390-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b390-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b390-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b390-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b390-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b390-167">CommonParameters</span></span>
<span data-ttu-id="6b390-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b390-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b390-169">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b390-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b390-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b390-170">INPUTS</span></span>

### <span data-ttu-id="6b390-171">System. String</span><span class="sxs-lookup"><span data-stu-id="6b390-171">System.String</span></span>

## <span data-ttu-id="6b390-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b390-172">OUTPUTS</span></span>

### <span data-ttu-id="6b390-173">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="6b390-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="6b390-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b390-174">NOTES</span></span>

## <span data-ttu-id="6b390-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b390-175">RELATED LINKS</span></span>
