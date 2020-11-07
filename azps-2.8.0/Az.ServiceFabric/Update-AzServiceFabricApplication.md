---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: d96a26e4f37d565ac03d8585a803c355aff53b19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824680"
---
# <span data-ttu-id="0e235-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0e235-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="0e235-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e235-102">SYNOPSIS</span></span>
<span data-ttu-id="0e235-103">Aktualisieren einer Service Fabric-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0e235-103">Update a service fabric application.</span></span> <span data-ttu-id="0e235-104">Auf diese Weise können Sie die Anwendungsparameter aktualisieren und/oder die Version des Anwendungstyps aktualisieren, die ein Anwendungs Upgrade auslösen wird.</span><span class="sxs-lookup"><span data-stu-id="0e235-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="0e235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e235-105">SYNTAX</span></span>

### <span data-ttu-id="0e235-106">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e235-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e235-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e235-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e235-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e235-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e235-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e235-109">DESCRIPTION</span></span>
<span data-ttu-id="0e235-110">Dieses Cmdlet kann verwendet werden, um Anwendungsparameter zu aktualisieren und die Version des Anwendungstyps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0e235-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="0e235-111">Beim Aktualisieren des Parameters wird nur das Modell auf der Arm-Seite geändert, nur bei Verwendung einer neuen Typversion wird durch den Befehl ein Anwendungs Upgrade ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0e235-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="0e235-112">Die angegebene Typen Version sollte bereits im Cluster mithilfe von **New-AzServiceFabricApplicationTypeVersion** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0e235-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="0e235-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e235-113">EXAMPLES</span></span>

### <span data-ttu-id="0e235-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e235-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="0e235-115">In diesem Beispiel wird ein Anwendungs Upgrade gestartet, um die Typ-Version auf "V2" zu aktualisieren, die mit **New-AzServiceFabricApplicationTypeVersion** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e235-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="0e235-116">Die verwendeten Anwendungsparameter sollten im Anwendungsmanifest definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e235-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="0e235-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e235-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="0e235-118">In diesem Beispiel werden die minimale und maximale Anzahl von Knoten Einschränkungen für die Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0e235-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="0e235-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0e235-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="0e235-120">In diesem Beispiel wird ein Anwendungs Upgrade gestartet, um die Typversion auf "V2" zu aktualisieren, und es werden auch einige Aktualisierungsrichtlinien Parameter festgelegt, die beim aktuellen Upgrade wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="0e235-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="0e235-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0e235-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="0e235-122">In diesem Beispiel werden die Anwendungsparameter aktualisiert, aber diese Änderungen werden erst wirksam, wenn die nächste Version auf die Anwendung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0e235-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="0e235-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e235-123">PARAMETERS</span></span>

### <span data-ttu-id="0e235-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="0e235-124">-ApplicationParameter</span></span>
<span data-ttu-id="0e235-125">Geben Sie die Anwendungsparameter als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="0e235-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="0e235-126">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0e235-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0e235-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="0e235-128">Angeben der Version des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="0e235-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-129">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0e235-129">-ClusterName</span></span>
<span data-ttu-id="0e235-130">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0e235-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="0e235-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="0e235-132">Gibt an, ob ein Warnungs Integritäts Ereignis während der Integritäts Auswertung als Fehlerereignis behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e235-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e235-133">-DefaultProfile</span></span>
<span data-ttu-id="0e235-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e235-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e235-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="0e235-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="0e235-136">Gibt den maximalen Prozentsatz der unhelthy-Partitionen pro Dienst an, der von der Integritätsrichtlinie für den Standarddiensttyp für das überwachte Upgrade zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0e235-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="0e235-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="0e235-138">Gibt den maximalen Prozentsatz der unhelthy-Replikate pro Dienst an, der von der Integritätsrichtlinie für den Standarddiensttyp für das überwachte Upgrade zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0e235-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="0e235-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="0e235-140">Gibt den maximalen Prozentsatz der unhelthy-Dienste an, die von der Integritätsrichtlinie für den Standarddiensttyp für das überwachte Upgrade zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0e235-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-141">-Fehler-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e235-141">-FailureAction</span></span>
<span data-ttu-id="0e235-142">Gibt die auszuführende Aktion an, wenn das überwachte Upgrade fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0e235-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="0e235-143">Die akzeptablen Werte für diesen Parameter sind Rollback oder manual.</span><span class="sxs-lookup"><span data-stu-id="0e235-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="0e235-144">-ForceRestart</span></span>
<span data-ttu-id="0e235-145">Gibt an, dass der Diensthost neu gestartet wird, selbst wenn es sich bei dem Upgrade um eine nur Konfigurationsänderung handelt.</span><span class="sxs-lookup"><span data-stu-id="0e235-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0e235-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="0e235-147">Gibt die Dauer in Sekunden an, nach der der Dienst Fabric die Integritätsprüfung erneut durchführt, wenn die vorherige Integritätsprüfung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0e235-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="0e235-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="0e235-149">Gibt die Dauer in Sekunden an, die von Service Fabric abgewartet wird, um zu überprüfen, ob die Anwendung stabil ist, bevor Sie zur nächsten Upgrade-Domäne wechseln oder das Upgrade abschließen.</span><span class="sxs-lookup"><span data-stu-id="0e235-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="0e235-150">Diese Wartezeit verhindert, dass nicht erkannte Änderungen des Zustands direkt nach der Integritätsprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0e235-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="0e235-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="0e235-152">Gibt die Dauer in Sekunden an, die von Service Fabric gewartet wird, bevor Sie die anfängliche Integritätsprüfung ausführt, nachdem Sie das Upgrade für die Upgrade-Domäne abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="0e235-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-153">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e235-153">-InputObject</span></span>
<span data-ttu-id="0e235-154">Die Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="0e235-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="0e235-155">-MaximumNodeCount</span></span>
<span data-ttu-id="0e235-156">Gibt die maximale Anzahl von Knoten an, auf denen eine Anwendung platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e235-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="0e235-157">-MinimumNodeCount</span></span>
<span data-ttu-id="0e235-158">Gibt die Mindestanzahl von Knoten an, bei denen Service Fabric Kapazität für diese Anwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0e235-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-159">-Name</span><span class="sxs-lookup"><span data-stu-id="0e235-159">-Name</span></span>
<span data-ttu-id="0e235-160">Angeben des Namens der Anwendung</span><span class="sxs-lookup"><span data-stu-id="0e235-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e235-161">-ResourceGroupName</span></span>
<span data-ttu-id="0e235-162">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0e235-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-163">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e235-163">-ResourceId</span></span>
<span data-ttu-id="0e235-164">Arm-Quell Code der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0e235-164">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="0e235-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="0e235-166">Gibt die Karte der Integritätsrichtlinie an, die für verschiedene Diensttypen als Hashtabelle im folgenden Format verwendet werden soll: @ {"Service TypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="0e235-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="0e235-167">Beispiel: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5, 5; 5"}</span><span class="sxs-lookup"><span data-stu-id="0e235-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="0e235-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="0e235-169">Gibt den maximalen Prozentsatz der Anwendungsinstanzen an, die auf den Knoten im Cluster bereitgestellt werden, die den Integritätsstatus "Fehler" aufweisen, bevor der Anwendungs Integritätsstatus für den Cluster fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="0e235-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0e235-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="0e235-171">Gibt die maximale Zeitdauer (in Sekunden) an, die von Service Fabric für das Upgrade einer einzelnen Upgrade-Domäne benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0e235-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="0e235-172">Nach Ablauf dieses Zeitraums schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="0e235-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0e235-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="0e235-174">Gibt die maximale Zeit an, die Service Fabric wartet, bis ein Dienst in einem sicheren Zustand neu konfiguriert wird, wenn er sich nicht bereits in einem sicheren Zustand befindet, bevor der Service Fabric mit dem Upgrade fortschreitet.</span><span class="sxs-lookup"><span data-stu-id="0e235-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0e235-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="0e235-176">Gibt die maximale Zeitdauer in Sekunden an, die Service Fabric für das gesamte Upgrade benötigt.</span><span class="sxs-lookup"><span data-stu-id="0e235-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="0e235-177">Nach Ablauf dieses Zeitraums schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="0e235-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e235-178">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e235-178">-Confirm</span></span>
<span data-ttu-id="0e235-179">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e235-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e235-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e235-180">-WhatIf</span></span>
<span data-ttu-id="0e235-181">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e235-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e235-182">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e235-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e235-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e235-183">CommonParameters</span></span>
<span data-ttu-id="0e235-184">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e235-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e235-185">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e235-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e235-186">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e235-186">INPUTS</span></span>

### <span data-ttu-id="0e235-187">System. String</span><span class="sxs-lookup"><span data-stu-id="0e235-187">System.String</span></span>

### <span data-ttu-id="0e235-188">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="0e235-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="0e235-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e235-189">OUTPUTS</span></span>

### <span data-ttu-id="0e235-190">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="0e235-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="0e235-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e235-191">NOTES</span></span>

## <span data-ttu-id="0e235-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e235-192">RELATED LINKS</span></span>
