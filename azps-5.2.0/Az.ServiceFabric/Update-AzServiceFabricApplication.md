---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300003"
---
# <span data-ttu-id="ad675-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ad675-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ad675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad675-102">SYNOPSIS</span></span>
<span data-ttu-id="ad675-103">Aktualisieren Sie eine Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ad675-103">Update a service fabric application.</span></span> <span data-ttu-id="ad675-104">Dadurch können die Anwendungsparameter aktualisiert und/oder die Anwendungstypversion aktualisiert werden, wodurch ein Anwendungsupgrade ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="ad675-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="ad675-105">Unterstützt nur ARM bereitgestellten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ad675-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ad675-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad675-106">SYNTAX</span></span>

### <span data-ttu-id="ad675-107">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad675-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="ad675-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad675-108">ByResourceId</span></span>
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

### <span data-ttu-id="ad675-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad675-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad675-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad675-110">DESCRIPTION</span></span>
<span data-ttu-id="ad675-111">Dieses Cmdlet kann verwendet werden, um Anwendungsparameter zu aktualisieren und die Version des Anwendungstyps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ad675-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="ad675-112">Durch das Aktualisieren des Parameters wird das Modell nur auf der ARM geändert. Nur bei Verwendung einer neuen Typversion löst der Befehl ein Anwendungsupgrade aus.</span><span class="sxs-lookup"><span data-stu-id="ad675-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="ad675-113">Die angegebene Typversion sollte bereits im Cluster mit **"New-AzServiceFabricApplicationTypeVersion" erstellt werden.**</span><span class="sxs-lookup"><span data-stu-id="ad675-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="ad675-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ad675-114">EXAMPLES</span></span>

### <span data-ttu-id="ad675-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad675-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ad675-116">In diesem Beispiel wird ein Anwendungsupgrade gestartet, um die Typversion auf "v2" zu aktualisieren, die mit **"New-AzServiceFabricApplicationTypeVersion" erstellt wurde.**</span><span class="sxs-lookup"><span data-stu-id="ad675-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="ad675-117">Die verwendeten Anwendungsparameter sollten im Anwendungsmanifest definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad675-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="ad675-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad675-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="ad675-119">In diesem Beispiel wird die minimale und maximale Anzahl der Knotenbeschränkung für die Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ad675-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="ad675-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ad675-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="ad675-121">Dieses Beispiel startet ein Anwendungsupgrade, um die Typversion auf "v2" zu aktualisieren, und legt außerdem einige Upgraderichtlinienparameter fest, die ab dem aktuellen Upgrade wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="ad675-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="ad675-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ad675-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ad675-123">In diesem Beispiel werden die Anwendungsparameter aktualisiert, doch werden diese Änderungen nur bis zum nächsten Upgrade der Version auf die Anwendung wirksam.</span><span class="sxs-lookup"><span data-stu-id="ad675-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="ad675-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad675-124">PARAMETERS</span></span>

### <span data-ttu-id="ad675-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="ad675-125">-ApplicationParameter</span></span>
<span data-ttu-id="ad675-126">Geben Sie die Anwendungsparameter als Schlüssel/Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="ad675-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="ad675-127">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ad675-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="ad675-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ad675-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="ad675-129">Angeben der Version des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="ad675-129">Specify the application type version</span></span>

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

### <span data-ttu-id="ad675-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ad675-130">-ClusterName</span></span>
<span data-ttu-id="ad675-131">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="ad675-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ad675-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="ad675-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="ad675-133">Gibt an, ob ein Warnungsinte health-Ereignis während der Integritätsauswertung als Fehlerereignis behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad675-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="ad675-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad675-134">-DefaultProfile</span></span>
<span data-ttu-id="ad675-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad675-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad675-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="ad675-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="ad675-137">Gibt den in der Integritätsrichtlinie für den standardmäßigen Diensttyp zulässigen maximalen Prozentwert von nicht standardmäßigen Partitionen pro Dienst an, der für das überwachte Upgrade verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad675-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ad675-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="ad675-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="ad675-139">Gibt den maximalen Prozentwert der nicht standardmäßigen Replikate pro Dienst an, der von der Integritätsrichtlinie für den standardmäßigen Diensttyp für das überwachte Upgrade verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad675-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ad675-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="ad675-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="ad675-141">Gibt den maximalen Prozentwert der nicht standardmäßigen Dienste an, der in der Integritätsrichtlinie für den Standarddiensttyp zulässig ist, der für das überwachte Upgrade verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad675-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ad675-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="ad675-142">-FailureAction</span></span>
<span data-ttu-id="ad675-143">Gibt die Aktion an, die sie ausführen soll, wenn das überwachte Upgrade fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ad675-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="ad675-144">Die zulässigen Werte für diesen Parameter sind Rollback oder Manuell.</span><span class="sxs-lookup"><span data-stu-id="ad675-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="ad675-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="ad675-145">-ForceRestart</span></span>
<span data-ttu-id="ad675-146">Gibt an, dass der Diensthost neu gestartet wird, auch wenn es sich bei dem Upgrade nur um eine Konfigurationsänderung handelt.</span><span class="sxs-lookup"><span data-stu-id="ad675-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="ad675-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ad675-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="ad675-148">Gibt die Dauer in Sekunden an, nach der Service Fabric die Integritätsprüfung erneut überprüft, wenn die vorherige Integritätsprüfung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ad675-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="ad675-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="ad675-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="ad675-150">Specifies the duration, in seconds, that Service Fabric waits to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span><span class="sxs-lookup"><span data-stu-id="ad675-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="ad675-151">Durch diese Wartezeit werden nicht erkannte Integritätsänderungen direkt nach der Integritätsprüfung verhindert.</span><span class="sxs-lookup"><span data-stu-id="ad675-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="ad675-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="ad675-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="ad675-153">Specifies the duration, in seconds, that Service Fabric waits before it perform the initial health check after it finishes the upgrade on the upgrade domain.</span><span class="sxs-lookup"><span data-stu-id="ad675-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="ad675-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad675-154">-InputObject</span></span>
<span data-ttu-id="ad675-155">Die Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="ad675-155">The application resource.</span></span>

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

### <span data-ttu-id="ad675-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ad675-156">-MaximumNodeCount</span></span>
<span data-ttu-id="ad675-157">Gibt die maximale Anzahl von Knoten an, für die eine Anwendung platzieren werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad675-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="ad675-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ad675-158">-MinimumNodeCount</span></span>
<span data-ttu-id="ad675-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span><span class="sxs-lookup"><span data-stu-id="ad675-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="ad675-160">-Name</span><span class="sxs-lookup"><span data-stu-id="ad675-160">-Name</span></span>
<span data-ttu-id="ad675-161">Angeben des Anwendungsnamens</span><span class="sxs-lookup"><span data-stu-id="ad675-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="ad675-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad675-162">-ResourceGroupName</span></span>
<span data-ttu-id="ad675-163">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ad675-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ad675-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad675-164">-ResourceId</span></span>
<span data-ttu-id="ad675-165">Arm ResourceId der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ad675-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ad675-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="ad675-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="ad675-167">Gibt die Zuordnung der Integritätsrichtlinie an, die für verschiedene Diensttypen als Hashtabelle im folgenden Format verwendet werden soll: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="ad675-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="ad675-168">Beispiel: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="ad675-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="ad675-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="ad675-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="ad675-170">Gibt den maximalen Prozentsatz der Anwendungsinstanzen an, die auf den Knoten im Cluster bereitgestellt werden, für die ein Fehlerstatus vor dem Fehler des Anwendungsstatus für den Cluster auftritt.</span><span class="sxs-lookup"><span data-stu-id="ad675-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="ad675-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ad675-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="ad675-172">Gibt die maximale Zeit (in Sekunden) an, die Service Fabric zum Upgrade einer einzelnen Upgradedomäne benötigt.</span><span class="sxs-lookup"><span data-stu-id="ad675-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="ad675-173">Nach diesem Zeitraum schlägt das Upgrade fehl.</span><span class="sxs-lookup"><span data-stu-id="ad675-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="ad675-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ad675-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="ad675-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span><span class="sxs-lookup"><span data-stu-id="ad675-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="ad675-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ad675-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="ad675-177">Gibt die maximale Zeit (in Sekunden) an, die Service Fabric für das gesamte Upgrade benötigt.</span><span class="sxs-lookup"><span data-stu-id="ad675-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="ad675-178">Nach diesem Zeitraum schlägt das Upgrade fehl.</span><span class="sxs-lookup"><span data-stu-id="ad675-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="ad675-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad675-179">-Confirm</span></span>
<span data-ttu-id="ad675-180">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad675-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad675-181">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ad675-181">-WhatIf</span></span>
<span data-ttu-id="ad675-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad675-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad675-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad675-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad675-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad675-184">CommonParameters</span></span>
<span data-ttu-id="ad675-185">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad675-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad675-186">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad675-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad675-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ad675-187">INPUTS</span></span>

### <span data-ttu-id="ad675-188">System.String</span><span class="sxs-lookup"><span data-stu-id="ad675-188">System.String</span></span>

### <span data-ttu-id="ad675-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ad675-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ad675-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ad675-190">OUTPUTS</span></span>

### <span data-ttu-id="ad675-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ad675-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ad675-192">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ad675-192">NOTES</span></span>

## <span data-ttu-id="ad675-193">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ad675-193">RELATED LINKS</span></span>
