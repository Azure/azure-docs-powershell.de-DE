---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 255db3680707af4e3658ce8a526cfa7b4a4d6f1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847807"
---
# <span data-ttu-id="20819-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="20819-101">New-AzBatchPool</span></span>

## <span data-ttu-id="20819-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20819-102">SYNOPSIS</span></span>
<span data-ttu-id="20819-103">Erstellt einen Pool im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="20819-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="20819-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20819-104">SYNTAX</span></span>

### <span data-ttu-id="20819-105">CloudServiceAndTargetDedicated (Standard)</span><span class="sxs-lookup"><span data-stu-id="20819-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20819-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="20819-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20819-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="20819-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20819-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="20819-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20819-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20819-109">DESCRIPTION</span></span>
<span data-ttu-id="20819-110">Das Cmdlet **New-AzBatchPool** erstellt einen Pool im Azure-Batch Dienst unter dem Konto, das vom *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="20819-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="20819-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20819-111">EXAMPLES</span></span>

### <span data-ttu-id="20819-112">Beispiel 1: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mithilfe von CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="20819-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="20819-113">Beispiel 2: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mithilfe von VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="20819-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="20819-114">Dieser Befehl erstellt einen neuen Pool mit ID MyPool mithilfe des TargetDedicated-Parametersatzes.</span><span class="sxs-lookup"><span data-stu-id="20819-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="20819-115">Die Zielzuordnung ist drei Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="20819-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="20819-116">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden.</span><span class="sxs-lookup"><span data-stu-id="20819-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="20819-117">Beispiel 3: Erstellen eines neuen Pools mit dem AutoScale-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="20819-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="20819-118">Dieser Befehl erstellt einen neuen Pool mit ID-AutoScalePool mit dem Parametersatz AutoScale.</span><span class="sxs-lookup"><span data-stu-id="20819-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="20819-119">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden, und die Ziel Anzahl der Compute-Knoten wird durch die AutoScale-Formel bestimmt.</span><span class="sxs-lookup"><span data-stu-id="20819-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="20819-120">Beispiel 4: Erstellen eines Pools mit Knoten in einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="20819-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="20819-121">Beispiel 5: Erstellen eines Pools mit benutzerdefinierten Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="20819-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="20819-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="20819-122">PARAMETERS</span></span>

### <span data-ttu-id="20819-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="20819-123">-ApplicationLicenses</span></span>
<span data-ttu-id="20819-124">Die Liste der Anwendungslizenzen, die vom Batch Dienst für jeden Compute-Knoten im Pool verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="20819-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="20819-125">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="20819-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="20819-127">Gibt die Zeitdauer (in Minuten) an, die verstreicht, bevor die Poolgröße automatisch entsprechend der AutoScale-Formel angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="20819-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="20819-128">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="20819-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="20819-129">-AutoScaleFormula</span></span>
<span data-ttu-id="20819-130">Gibt die Formel zum automatischen Skalieren des Pools an.</span><span class="sxs-lookup"><span data-stu-id="20819-130">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-131">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="20819-131">-BatchContext</span></span>
<span data-ttu-id="20819-132">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="20819-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20819-133">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="20819-133">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20819-134">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="20819-134">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20819-135">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="20819-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20819-136">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="20819-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20819-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="20819-137">-CertificateReferences</span></span>
<span data-ttu-id="20819-138">Gibt Zertifikate an, die dem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="20819-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="20819-139">Der Stapelverarbeitungs Dienst installiert die referenzierten Zertifikate auf jedem Compute-Knoten des Pools.</span><span class="sxs-lookup"><span data-stu-id="20819-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="20819-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="20819-141">Gibt die Konfigurationseinstellungen für einen Pool an, der auf der Azure Cloud-Dienstplattform basiert.</span><span class="sxs-lookup"><span data-stu-id="20819-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20819-142">-DefaultProfile</span></span>
<span data-ttu-id="20819-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20819-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20819-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="20819-144">-DisplayName</span></span>
<span data-ttu-id="20819-145">Gibt den Anzeigenamen des Pools an.</span><span class="sxs-lookup"><span data-stu-id="20819-145">Specifies the display name of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-146">-ID</span><span class="sxs-lookup"><span data-stu-id="20819-146">-Id</span></span>
<span data-ttu-id="20819-147">Gibt die ID des zu erstellende Pools an.</span><span class="sxs-lookup"><span data-stu-id="20819-147">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="20819-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="20819-149">Gibt an, dass dieses Cmdlet den Pool für die direkte Kommunikation zwischen dedizierten Compute-Knoten einrichtet.</span><span class="sxs-lookup"><span data-stu-id="20819-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="20819-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="20819-151">Gibt die maximale Anzahl von Aufgaben an, die für einen einzelnen Compute-Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="20819-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-152">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="20819-152">-Metadata</span></span>
<span data-ttu-id="20819-153">Gibt die Metadaten als Schlüssel-Wert-Paare an, die dem neuen Pool hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20819-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="20819-154">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="20819-154">The key is the metadata name.</span></span>
<span data-ttu-id="20819-155">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="20819-155">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20819-156">-NetworkConfiguration</span></span>
<span data-ttu-id="20819-157">Die Netzwerkkonfiguration für den Pool.</span><span class="sxs-lookup"><span data-stu-id="20819-157">The network configuration for the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="20819-158">-ResizeTimeout</span></span>
<span data-ttu-id="20819-159">Gibt das Timeout für das Zuweisen von Compute-Knoten zum Pool an.</span><span class="sxs-lookup"><span data-stu-id="20819-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="20819-160">-StartTask</span></span>
<span data-ttu-id="20819-161">Gibt die Spezifikation für den Startvorgang für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="20819-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="20819-162">Die Startaufgabe wird ausgeführt, wenn ein Compute-Knoten dem Pool Beitritt, oder wenn der Compute-Knoten neu gestartet oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="20819-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="20819-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="20819-164">Gibt die Ziel Anzahl dedizierter Compute-Knoten an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20819-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="20819-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="20819-166">Gibt die Ziel Anzahl von Compute-Knoten mit niedriger Priorität an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20819-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="20819-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="20819-168">Gibt die Aufgaben Planungsrichtlinie an, beispielsweise die ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="20819-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-169">-Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="20819-169">-UserAccount</span></span>
<span data-ttu-id="20819-170">Die Liste der Benutzerkonten, die auf jedem Knoten im Pool erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20819-170">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="20819-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="20819-172">Gibt Konfigurationseinstellungen für einen Pool in der Virtual Machines-Infrastruktur an.</span><span class="sxs-lookup"><span data-stu-id="20819-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="20819-173">-VirtualMachineSize</span></span>
<span data-ttu-id="20819-174">Gibt die Größe der virtuellen Computer im Pool an.</span><span class="sxs-lookup"><span data-stu-id="20819-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="20819-175">Weitere Informationen zu Größen für virtuelle Maschinen finden Sie unter Größen für virtuelle Maschinen https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) auf der Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="20819-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="20819-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20819-176">-Confirm</span></span>
<span data-ttu-id="20819-177">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20819-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20819-178">-WhatIf</span></span>
<span data-ttu-id="20819-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20819-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20819-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20819-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20819-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20819-181">CommonParameters</span></span>
<span data-ttu-id="20819-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20819-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20819-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20819-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20819-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20819-184">INPUTS</span></span>

### <span data-ttu-id="20819-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20819-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20819-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20819-186">OUTPUTS</span></span>

### <span data-ttu-id="20819-187">System. void</span><span class="sxs-lookup"><span data-stu-id="20819-187">System.Void</span></span>

## <span data-ttu-id="20819-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="20819-188">NOTES</span></span>

## <span data-ttu-id="20819-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20819-189">RELATED LINKS</span></span>

[<span data-ttu-id="20819-190">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="20819-190">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20819-191">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="20819-191">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="20819-192">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="20819-192">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="20819-193">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="20819-193">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


