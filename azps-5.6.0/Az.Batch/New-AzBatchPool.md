---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939712"
---
# <span data-ttu-id="55ca8-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="55ca8-101">New-AzBatchPool</span></span>

## <span data-ttu-id="55ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="55ca8-103">Erstellt einen Pool im Batchdienst.</span><span class="sxs-lookup"><span data-stu-id="55ca8-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="55ca8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55ca8-104">SYNTAX</span></span>

### <span data-ttu-id="55ca8-105">CloudServiceAndTargetDedicated (Standard)</span><span class="sxs-lookup"><span data-stu-id="55ca8-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55ca8-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="55ca8-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55ca8-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="55ca8-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55ca8-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="55ca8-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55ca8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55ca8-109">DESCRIPTION</span></span>
<span data-ttu-id="55ca8-110">Das **Cmdlet New-AzBatchPool** erstellt einen Pool im Azure Batch-Dienst unter dem Konto, das vom *BatchContext-Parameter angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="55ca8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55ca8-111">EXAMPLES</span></span>

### <span data-ttu-id="55ca8-112">Beispiel 1: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mit CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="55ca8-113">Der Pool ist für die Verwendung STANDARD_D1_V2 virtuellen Computer mit der Betriebssystemversion von Familie vier konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="55ca8-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="55ca8-114">Beispiel 2: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mit VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="55ca8-115">Mit diesem Befehl wird ein neuer Pool mit ID MyPool mit dem Parametersatz TargetDedicated erstellt.</span><span class="sxs-lookup"><span data-stu-id="55ca8-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="55ca8-116">Die Zielzuordnung besteht aus drei Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="55ca8-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="55ca8-117">Der Pool ist für die Verwendung STANDARD_D1_V2 virtuellen Computer mit dem Windows-2016-Datacenter-Betriebssystemabbild konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="55ca8-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="55ca8-118">Beispiel 3: Erstellen eines neuen Pools mit dem Parametersatz "AutoScale"</span><span class="sxs-lookup"><span data-stu-id="55ca8-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="55ca8-119">Mit diesem Befehl wird mit dem Parametersatz AutoScale ein neuer Pool mit ID AutoScalePool erstellt.</span><span class="sxs-lookup"><span data-stu-id="55ca8-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="55ca8-120">Der Pool ist für die Verwendung STANDARD_D1_V2 virtuellen Computern mit dem Windows-2016-Datacenter-Betriebssystemabbild konfiguriert, und die Zielanzahl von Computeknoten wird durch die Formel Autoscale bestimmt.</span><span class="sxs-lookup"><span data-stu-id="55ca8-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="55ca8-121">Beispiel 4: Erstellen eines Pools mit Knoten in einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="55ca8-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="55ca8-122">Beispiel 5: Erstellen eines Pools mit benutzerdefinierten Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="55ca8-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="55ca8-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55ca8-123">PARAMETERS</span></span>

### <span data-ttu-id="55ca8-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="55ca8-124">-ApplicationLicenses</span></span>
<span data-ttu-id="55ca8-125">Die Liste der Anwendungslizenzen, die der Batchdienst für jeden Computeknoten im Pool zur Verfügung stellen wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="55ca8-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="55ca8-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="55ca8-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="55ca8-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="55ca8-128">Gibt den Zeitraum in Minuten an, der verstrichen ist, bevor die Poolgröße gemäß der Formel "AutoScale" automatisch angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="55ca8-129">Der Standardwert beträgt 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="55ca8-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="55ca8-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="55ca8-130">-AutoScaleFormula</span></span>
<span data-ttu-id="55ca8-131">Gibt die Formel zum automatischen Skalieren des Pools an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="55ca8-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="55ca8-132">-BatchContext</span></span>
<span data-ttu-id="55ca8-133">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="55ca8-134">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="55ca8-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="55ca8-135">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="55ca8-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="55ca8-136">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="55ca8-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="55ca8-137">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="55ca8-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="55ca8-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="55ca8-138">-CertificateReferences</span></span>
<span data-ttu-id="55ca8-139">Gibt Zertifikate an, die dem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55ca8-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="55ca8-140">Der Batchdienst installiert die Zertifikate, auf die verwiesen wird, auf jeden Computeknoten des Pools.</span><span class="sxs-lookup"><span data-stu-id="55ca8-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="55ca8-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="55ca8-142">Gibt Konfigurationseinstellungen für einen Pool basierend auf der Azure-Clouddienstplattform an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="55ca8-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ca8-143">-DefaultProfile</span></span>
<span data-ttu-id="55ca8-144">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55ca8-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55ca8-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55ca8-145">-DisplayName</span></span>
<span data-ttu-id="55ca8-146">Gibt den Anzeigenamen des Pools an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="55ca8-147">-ID</span><span class="sxs-lookup"><span data-stu-id="55ca8-147">-Id</span></span>
<span data-ttu-id="55ca8-148">Gibt die ID des zu erstellenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="55ca8-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="55ca8-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="55ca8-150">Gibt an, dass mit diesem Cmdlet der Pool für die direkte Kommunikation zwischen dedizierten Computeknoten eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="55ca8-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="55ca8-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="55ca8-152">Gibt die maximale Anzahl von Aufgaben an, die auf einem einzelnen Computeknoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="55ca8-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="55ca8-153">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="55ca8-153">-Metadata</span></span>
<span data-ttu-id="55ca8-154">Gibt die Metadaten als Schlüssel-Wert-Paare an, die dem neuen Pool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="55ca8-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="55ca8-155">Der Schlüssel ist der Metadatenname.</span><span class="sxs-lookup"><span data-stu-id="55ca8-155">The key is the metadata name.</span></span>
<span data-ttu-id="55ca8-156">Der Wert ist der Metadatenwert.</span><span class="sxs-lookup"><span data-stu-id="55ca8-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="55ca8-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-157">-MountConfiguration</span></span>
<span data-ttu-id="55ca8-158">Eine Liste der Dateisysteme, die auf jedem Knoten im Pool angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="55ca8-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="55ca8-159">Dies unterstützt Azure Files, NFS, CIFS/SMB und Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="55ca8-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ca8-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-160">-NetworkConfiguration</span></span>
<span data-ttu-id="55ca8-161">Die Netzwerkkonfiguration für den Pool.</span><span class="sxs-lookup"><span data-stu-id="55ca8-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="55ca8-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="55ca8-162">-ResizeTimeout</span></span>
<span data-ttu-id="55ca8-163">Gibt die Zeit für die Zuordnung von Computeknoten zum Pool an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="55ca8-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="55ca8-164">-StartTask</span></span>
<span data-ttu-id="55ca8-165">Gibt die Spezifikation für die Startaufgabe für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="55ca8-166">Die Startaufgabe wird ausgeführt, wenn ein Computeknoten dem Pool beitritt oder wenn der Computeknoten neu gestartet oder neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="55ca8-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="55ca8-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="55ca8-168">Gibt die Zielnummer der dedizierten Computeknoten an, die dem Pool zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="55ca8-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="55ca8-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="55ca8-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="55ca8-170">Gibt die Zielanzahl der Computeknoten mit niedriger Priorität an, die dem Pool zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="55ca8-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="55ca8-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="55ca8-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="55ca8-172">Gibt die Vorgangsplanungsrichtlinie an, z. B. "ComputeNodeFillType".</span><span class="sxs-lookup"><span data-stu-id="55ca8-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="55ca8-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="55ca8-173">-UserAccount</span></span>
<span data-ttu-id="55ca8-174">Die Liste der Benutzerkonten, die für jeden Knoten im Pool erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55ca8-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="55ca8-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ca8-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="55ca8-176">Gibt Konfigurationseinstellungen für einen Pool auf der Infrastruktur virtueller Computer an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="55ca8-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="55ca8-177">-VirtualMachineSize</span></span>
<span data-ttu-id="55ca8-178">Gibt die Größe der virtuellen Computer im Pool an.</span><span class="sxs-lookup"><span data-stu-id="55ca8-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="55ca8-179">Weitere Informationen zu den Größen virtueller Computer finden Sie unter Größen für virtuelle Computer https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) (auf der Microsoft Azure-Website).</span><span class="sxs-lookup"><span data-stu-id="55ca8-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="55ca8-180">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55ca8-180">-Confirm</span></span>
<span data-ttu-id="55ca8-181">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55ca8-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ca8-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ca8-182">-WhatIf</span></span>
<span data-ttu-id="55ca8-183">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55ca8-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ca8-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55ca8-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ca8-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ca8-185">CommonParameters</span></span>
<span data-ttu-id="55ca8-186">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ca8-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ca8-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55ca8-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ca8-188">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55ca8-188">INPUTS</span></span>

### <span data-ttu-id="55ca8-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="55ca8-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="55ca8-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55ca8-190">OUTPUTS</span></span>

### <span data-ttu-id="55ca8-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="55ca8-191">System.Void</span></span>

## <span data-ttu-id="55ca8-192">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="55ca8-192">NOTES</span></span>

## <span data-ttu-id="55ca8-193">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="55ca8-193">RELATED LINKS</span></span>

[<span data-ttu-id="55ca8-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="55ca8-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="55ca8-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="55ca8-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="55ca8-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="55ca8-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="55ca8-197">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="55ca8-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
