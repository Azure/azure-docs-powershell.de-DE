---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: c401e5b4a85d8c994e96d77f39d646dabb74e02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480549"
---
# <span data-ttu-id="e11b3-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="e11b3-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="e11b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e11b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e11b3-103">Erstellt einen Pool im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="e11b3-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e11b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e11b3-104">SYNTAX</span></span>

### <span data-ttu-id="e11b3-105">CloudServiceAndTargetDedicated (Standard)</span><span class="sxs-lookup"><span data-stu-id="e11b3-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="e11b3-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="e11b3-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="e11b3-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="e11b3-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="e11b3-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="e11b3-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="e11b3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e11b3-109">DESCRIPTION</span></span>
<span data-ttu-id="e11b3-110">Das Cmdlet **New-AzureBatchPool** erstellt einen Pool im Azure-Batch Dienst unter dem Konto, das vom *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e11b3-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="e11b3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e11b3-111">EXAMPLES</span></span>

### <span data-ttu-id="e11b3-112">Beispiel 1: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mithilfe von CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e11b3-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="e11b3-113">Beispiel 2: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz mithilfe von VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="e11b3-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="e11b3-114">Dieser Befehl erstellt einen neuen Pool mit ID MyPool mithilfe des TargetDedicated-Parametersatzes.</span><span class="sxs-lookup"><span data-stu-id="e11b3-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="e11b3-115">Die Zielzuordnung ist drei Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="e11b3-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="e11b3-116">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden.</span><span class="sxs-lookup"><span data-stu-id="e11b3-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="e11b3-117">Beispiel 3: Erstellen eines neuen Pools mit dem AutoScale-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="e11b3-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="e11b3-118">Dieser Befehl erstellt einen neuen Pool mit ID-AutoScalePool mit dem Parametersatz AutoScale.</span><span class="sxs-lookup"><span data-stu-id="e11b3-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="e11b3-119">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden, und die Ziel Anzahl der Compute-Knoten wird durch die AutoScale-Formel bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e11b3-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="e11b3-120">Beispiel 4: Erstellen eines Pools mit Knoten in einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="e11b3-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="e11b3-121">Beispiel 5: Erstellen eines Pools mit benutzerdefinierten Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="e11b3-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="e11b3-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="e11b3-122">PARAMETERS</span></span>

### <span data-ttu-id="e11b3-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="e11b3-123">-ApplicationLicenses</span></span>
<span data-ttu-id="e11b3-124">Die Liste der Anwendungslizenzen, die vom Batch Dienst für jeden Compute-Knoten im Pool verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="e11b3-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="e11b3-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="e11b3-125">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="e11b3-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="e11b3-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="e11b3-127">Gibt die Zeitdauer (in Minuten) an, die verstreicht, bevor die Poolgröße automatisch entsprechend der AutoScale-Formel angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="e11b3-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="e11b3-128">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e11b3-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="e11b3-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="e11b3-129">-AutoScaleFormula</span></span>
<span data-ttu-id="e11b3-130">Gibt die Formel zum automatischen Skalieren des Pools an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-130">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="e11b3-131">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="e11b3-131">-BatchContext</span></span>
<span data-ttu-id="e11b3-132">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e11b3-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e11b3-133">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e11b3-133">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e11b3-134">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-134">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e11b3-135">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="e11b3-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e11b3-136">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e11b3-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="e11b3-137">-CertificateReferences</span></span>
<span data-ttu-id="e11b3-138">Gibt Zertifikate an, die dem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e11b3-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="e11b3-139">Der Stapelverarbeitungs Dienst installiert die referenzierten Zertifikate auf jedem Compute-Knoten des Pools.</span><span class="sxs-lookup"><span data-stu-id="e11b3-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="e11b3-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e11b3-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="e11b3-141">Gibt die Konfigurationseinstellungen für einen Pool an, der auf der Azure Cloud-Dienstplattform basiert.</span><span class="sxs-lookup"><span data-stu-id="e11b3-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="e11b3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e11b3-142">-DefaultProfile</span></span>
<span data-ttu-id="e11b3-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e11b3-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11b3-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e11b3-144">-DisplayName</span></span>
<span data-ttu-id="e11b3-145">Gibt den Anzeigenamen des Pools an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="e11b3-146">-ID</span><span class="sxs-lookup"><span data-stu-id="e11b3-146">-Id</span></span>
<span data-ttu-id="e11b3-147">Gibt die ID des zu erstellende Pools an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="e11b3-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="e11b3-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="e11b3-149">Gibt an, dass dieses Cmdlet den Pool für die direkte Kommunikation zwischen dedizierten Compute-Knoten einrichtet.</span><span class="sxs-lookup"><span data-stu-id="e11b3-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="e11b3-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="e11b3-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="e11b3-151">Gibt die maximale Anzahl von Aufgaben an, die für einen einzelnen Compute-Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="e11b3-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="e11b3-152">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="e11b3-152">-Metadata</span></span>
<span data-ttu-id="e11b3-153">Gibt die Metadaten als Schlüssel-Wert-Paare an, die dem neuen Pool hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="e11b3-154">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="e11b3-154">The key is the metadata name.</span></span>
<span data-ttu-id="e11b3-155">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="e11b3-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="e11b3-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e11b3-156">-NetworkConfiguration</span></span>
<span data-ttu-id="e11b3-157">Die Netzwerkkonfiguration für den Pool.</span><span class="sxs-lookup"><span data-stu-id="e11b3-157">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="e11b3-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="e11b3-158">-ResizeTimeout</span></span>
<span data-ttu-id="e11b3-159">Gibt das Timeout für das Zuweisen von Compute-Knoten zum Pool an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="e11b3-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="e11b3-160">-StartTask</span></span>
<span data-ttu-id="e11b3-161">Gibt die Spezifikation für den Startvorgang für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="e11b3-162">Die Startaufgabe wird ausgeführt, wenn ein Compute-Knoten dem Pool Beitritt, oder wenn der Compute-Knoten neu gestartet oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e11b3-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="e11b3-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e11b3-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="e11b3-164">Gibt die Ziel Anzahl dedizierter Compute-Knoten an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="e11b3-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e11b3-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="e11b3-166">Gibt die Ziel Anzahl von Compute-Knoten mit niedriger Priorität an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="e11b3-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="e11b3-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="e11b3-168">Gibt die Aufgaben Planungsrichtlinie an, beispielsweise die ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="e11b3-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="e11b3-169">-Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="e11b3-169">-UserAccount</span></span>
<span data-ttu-id="e11b3-170">Die Liste der Benutzerkonten, die auf jedem Knoten im Pool erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-170">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="e11b3-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="e11b3-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="e11b3-172">Gibt Konfigurationseinstellungen für einen Pool in der Virtual Machines-Infrastruktur an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="e11b3-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="e11b3-173">-VirtualMachineSize</span></span>
<span data-ttu-id="e11b3-174">Gibt die Größe der virtuellen Computer im Pool an.</span><span class="sxs-lookup"><span data-stu-id="e11b3-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="e11b3-175">Weitere Informationen zu Größen für virtuelle Maschinen finden Sie unter Größen für virtuelle Maschinen https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) auf der Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="e11b3-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="e11b3-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e11b3-176">-Confirm</span></span>
<span data-ttu-id="e11b3-177">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e11b3-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e11b3-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e11b3-178">-WhatIf</span></span>
<span data-ttu-id="e11b3-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e11b3-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e11b3-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e11b3-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e11b3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11b3-181">CommonParameters</span></span>
<span data-ttu-id="e11b3-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e11b3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11b3-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e11b3-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11b3-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e11b3-184">INPUTS</span></span>

### <span data-ttu-id="e11b3-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e11b3-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e11b3-186">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e11b3-186">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e11b3-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e11b3-187">OUTPUTS</span></span>

### <span data-ttu-id="e11b3-188">System. void</span><span class="sxs-lookup"><span data-stu-id="e11b3-188">System.Void</span></span>

## <span data-ttu-id="e11b3-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="e11b3-189">NOTES</span></span>

## <span data-ttu-id="e11b3-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e11b3-190">RELATED LINKS</span></span>

[<span data-ttu-id="e11b3-191">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e11b3-191">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e11b3-192">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="e11b3-192">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="e11b3-193">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="e11b3-193">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="e11b3-194">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e11b3-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


