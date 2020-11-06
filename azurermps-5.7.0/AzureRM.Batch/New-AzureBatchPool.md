---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505529"
---
# <span data-ttu-id="02389-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="02389-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="02389-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02389-102">SYNOPSIS</span></span>
<span data-ttu-id="02389-103">Erstellt einen Pool im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="02389-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02389-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02389-104">SYNTAX</span></span>

### <span data-ttu-id="02389-105">CloudServiceAndTargetDedicated (Standard)</span><span class="sxs-lookup"><span data-stu-id="02389-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02389-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="02389-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
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

### <span data-ttu-id="02389-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="02389-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

### <span data-ttu-id="02389-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="02389-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

## <span data-ttu-id="02389-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02389-109">DESCRIPTION</span></span>
<span data-ttu-id="02389-110">Das Cmdlet **New-AzureBatchPool** erstellt einen Pool im Azure-Batch Dienst unter dem Konto, das vom *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02389-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="02389-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02389-111">EXAMPLES</span></span>

### <span data-ttu-id="02389-112">Beispiel 1: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="02389-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="02389-113">Dieser Befehl erstellt einen neuen Pool mit ID MyPool mithilfe des TargetDedicated-Parametersatzes.</span><span class="sxs-lookup"><span data-stu-id="02389-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="02389-114">Die Zielzuordnung ist drei Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="02389-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="02389-115">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden.</span><span class="sxs-lookup"><span data-stu-id="02389-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="02389-116">Beispiel 2: Erstellen eines neuen Pools mit dem AutoScale-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="02389-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="02389-117">Dieser Befehl erstellt einen neuen Pool mit ID-AutoScalePool mit dem Parametersatz AutoScale.</span><span class="sxs-lookup"><span data-stu-id="02389-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="02389-118">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden, und die Ziel Anzahl der Compute-Knoten wird durch die AutoScale-Formel bestimmt.</span><span class="sxs-lookup"><span data-stu-id="02389-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="02389-119">Beispiel 3: Erstellen eines Pools mit Knoten in einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="02389-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="02389-120">Beispiel 4: Erstellen eines Pools mit benutzerdefinierten Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="02389-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="02389-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="02389-121">PARAMETERS</span></span>

### <span data-ttu-id="02389-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="02389-122">-ApplicationLicenses</span></span>
<span data-ttu-id="02389-123">Die Liste der Anwendungslizenzen, die vom Batch Dienst für jeden Compute-Knoten im Pool verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="02389-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="02389-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="02389-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="02389-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="02389-126">Gibt die Zeitdauer (in Minuten) an, die verstreicht, bevor die Poolgröße automatisch entsprechend der AutoScale-Formel angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="02389-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="02389-127">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="02389-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="02389-128">-AutoScaleFormula</span></span>
<span data-ttu-id="02389-129">Gibt die Formel zum automatischen Skalieren des Pools an.</span><span class="sxs-lookup"><span data-stu-id="02389-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-130">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="02389-130">-BatchContext</span></span>
<span data-ttu-id="02389-131">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="02389-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02389-132">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="02389-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02389-133">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="02389-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02389-134">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="02389-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02389-135">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="02389-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02389-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="02389-136">-CertificateReferences</span></span>
<span data-ttu-id="02389-137">Gibt Zertifikate an, die dem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="02389-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="02389-138">Der Stapelverarbeitungs Dienst installiert die referenzierten Zertifikate auf jedem Compute-Knoten des Pools.</span><span class="sxs-lookup"><span data-stu-id="02389-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="02389-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="02389-140">Gibt die Konfigurationseinstellungen für einen Pool an, der auf der Azure Cloud-Dienstplattform basiert.</span><span class="sxs-lookup"><span data-stu-id="02389-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02389-141">-DefaultProfile</span></span>
<span data-ttu-id="02389-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02389-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02389-143">-DisplayName</span></span>
<span data-ttu-id="02389-144">Gibt den Anzeigenamen des Pools an.</span><span class="sxs-lookup"><span data-stu-id="02389-144">Specifies the display name of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-145">-ID</span><span class="sxs-lookup"><span data-stu-id="02389-145">-Id</span></span>
<span data-ttu-id="02389-146">Gibt die ID des zu erstellende Pools an.</span><span class="sxs-lookup"><span data-stu-id="02389-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="02389-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="02389-148">Gibt an, dass dieses Cmdlet den Pool für die direkte Kommunikation zwischen dedizierten Compute-Knoten einrichtet.</span><span class="sxs-lookup"><span data-stu-id="02389-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="02389-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="02389-150">Gibt die maximale Anzahl von Aufgaben an, die für einen einzelnen Compute-Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="02389-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-151">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="02389-151">-Metadata</span></span>
<span data-ttu-id="02389-152">Gibt die Metadaten als Schlüssel-Wert-Paare an, die dem neuen Pool hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02389-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="02389-153">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="02389-153">The key is the metadata name.</span></span>
<span data-ttu-id="02389-154">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="02389-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="02389-155">-NetworkConfiguration</span></span>
<span data-ttu-id="02389-156">Die Netzwerkkonfiguration für den Pool.</span><span class="sxs-lookup"><span data-stu-id="02389-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="02389-157">-ResizeTimeout</span></span>
<span data-ttu-id="02389-158">Gibt das Timeout für das Zuweisen von Compute-Knoten zum Pool an.</span><span class="sxs-lookup"><span data-stu-id="02389-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="02389-159">-StartTask</span></span>
<span data-ttu-id="02389-160">Gibt die Spezifikation für den Startvorgang für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="02389-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="02389-161">Die Startaufgabe wird ausgeführt, wenn ein Compute-Knoten dem Pool Beitritt, oder wenn der Compute-Knoten neu gestartet oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="02389-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="02389-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="02389-163">Gibt die Ziel Anzahl dedizierter Compute-Knoten an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02389-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="02389-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="02389-165">Gibt die Ziel Anzahl von Compute-Knoten mit niedriger Priorität an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02389-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="02389-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="02389-167">Gibt die Aufgaben Planungsrichtlinie an, beispielsweise die ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="02389-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-168">-Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="02389-168">-UserAccount</span></span>
<span data-ttu-id="02389-169">Die Liste der Benutzerkonten, die auf jedem Knoten im Pool erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02389-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="02389-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="02389-171">Gibt Konfigurationseinstellungen für einen Pool in der Virtual Machines-Infrastruktur an.</span><span class="sxs-lookup"><span data-stu-id="02389-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="02389-172">-VirtualMachineSize</span></span>
<span data-ttu-id="02389-173">Gibt die Größe der virtuellen Computer im Pool an.</span><span class="sxs-lookup"><span data-stu-id="02389-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="02389-174">Weitere Informationen zu Größen für virtuelle Maschinen finden Sie unter Größen für virtuelle Maschinen https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) auf der Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="02389-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02389-175">-Confirm</span></span>
<span data-ttu-id="02389-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02389-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02389-177">-WhatIf</span></span>
<span data-ttu-id="02389-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02389-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02389-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02389-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02389-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02389-180">CommonParameters</span></span>
<span data-ttu-id="02389-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02389-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02389-182">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02389-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02389-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02389-183">INPUTS</span></span>

### <span data-ttu-id="02389-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02389-184">BatchAccountContext</span></span>
<span data-ttu-id="02389-185">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02389-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="02389-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02389-186">OUTPUTS</span></span>

## <span data-ttu-id="02389-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="02389-187">NOTES</span></span>

## <span data-ttu-id="02389-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02389-188">RELATED LINKS</span></span>

[<span data-ttu-id="02389-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="02389-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="02389-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="02389-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="02389-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="02389-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="02389-192">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="02389-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


