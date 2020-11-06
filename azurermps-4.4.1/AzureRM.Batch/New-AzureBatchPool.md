---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497897"
---
# <span data-ttu-id="6c073-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c073-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="6c073-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c073-102">SYNOPSIS</span></span>
<span data-ttu-id="6c073-103">Erstellt einen Pool im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="6c073-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c073-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c073-104">SYNTAX</span></span>

### <span data-ttu-id="6c073-105">CloudServiceAndTargetDedicated (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c073-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c073-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="6c073-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c073-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="6c073-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c073-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="6c073-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c073-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c073-109">DESCRIPTION</span></span>
<span data-ttu-id="6c073-110">Das Cmdlet **New-AzureBatchPool** erstellt einen Pool im Azure-Batch Dienst unter dem Konto, das vom *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c073-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="6c073-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c073-111">EXAMPLES</span></span>

### <span data-ttu-id="6c073-112">Beispiel 1: Erstellen eines neuen Pools mit dem TargetDedicated-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="6c073-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="6c073-113">Dieser Befehl erstellt einen neuen Pool mit ID MyPool mithilfe des TargetDedicated-Parametersatzes.</span><span class="sxs-lookup"><span data-stu-id="6c073-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="6c073-114">Die Zielzuordnung ist drei Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="6c073-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="6c073-115">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden.</span><span class="sxs-lookup"><span data-stu-id="6c073-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="6c073-116">Beispiel 2: Erstellen eines neuen Pools mit dem AutoScale-Parametersatz</span><span class="sxs-lookup"><span data-stu-id="6c073-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="6c073-117">Dieser Befehl erstellt einen neuen Pool mit ID-AutoScalePool mit dem Parametersatz AutoScale.</span><span class="sxs-lookup"><span data-stu-id="6c073-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="6c073-118">Der Pool ist für die Verwendung kleiner virtueller Computer konfiguriert, die mit der neuesten Version der Betriebssystemfamilie Four abbilden, und die Ziel Anzahl der Compute-Knoten wird durch die AutoScale-Formel bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6c073-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="6c073-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c073-119">PARAMETERS</span></span>

### <span data-ttu-id="6c073-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="6c073-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c073-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="6c073-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="6c073-122">Gibt die Zeitdauer (in Minuten) an, die verstreicht, bevor die Poolgröße automatisch entsprechend der AutoScale-Formel angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="6c073-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="6c073-123">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="6c073-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="6c073-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="6c073-124">-AutoScaleFormula</span></span>
<span data-ttu-id="6c073-125">Gibt die Formel zum automatischen Skalieren des Pools an.</span><span class="sxs-lookup"><span data-stu-id="6c073-125">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="6c073-126">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6c073-126">-BatchContext</span></span>
<span data-ttu-id="6c073-127">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c073-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6c073-128">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c073-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6c073-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="6c073-129">-CertificateReferences</span></span>
<span data-ttu-id="6c073-130">Gibt Zertifikate an, die dem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c073-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="6c073-131">Der Stapelverarbeitungs Dienst installiert die referenzierten Zertifikate auf jedem Compute-Knoten des Pools.</span><span class="sxs-lookup"><span data-stu-id="6c073-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c073-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c073-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="6c073-133">Gibt die Konfigurationseinstellungen für einen Pool an, der auf der Azure Cloud-Dienstplattform basiert.</span><span class="sxs-lookup"><span data-stu-id="6c073-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="6c073-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6c073-134">-DisplayName</span></span>
<span data-ttu-id="6c073-135">Gibt den Anzeigenamen des Pools an.</span><span class="sxs-lookup"><span data-stu-id="6c073-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="6c073-136">-ID</span><span class="sxs-lookup"><span data-stu-id="6c073-136">-Id</span></span>
<span data-ttu-id="6c073-137">Gibt die ID des zu erstellende Pools an.</span><span class="sxs-lookup"><span data-stu-id="6c073-137">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="6c073-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="6c073-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="6c073-139">Gibt an, dass dieses Cmdlet den Pool für die direkte Kommunikation zwischen dedizierten Compute-Knoten einrichtet.</span><span class="sxs-lookup"><span data-stu-id="6c073-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="6c073-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c073-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="6c073-141">Gibt die maximale Anzahl von Aufgaben an, die für einen einzelnen Compute-Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6c073-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="6c073-142">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="6c073-142">-Metadata</span></span>
<span data-ttu-id="6c073-143">Gibt die Metadaten als Schlüssel-Wert-Paare an, die dem neuen Pool hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c073-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="6c073-144">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="6c073-144">The key is the metadata name.</span></span>
<span data-ttu-id="6c073-145">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="6c073-145">The value is the metadata value.</span></span>

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

### <span data-ttu-id="6c073-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c073-146">-NetworkConfiguration</span></span>
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

### <span data-ttu-id="6c073-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="6c073-147">-ResizeTimeout</span></span>
<span data-ttu-id="6c073-148">Gibt das Timeout für das Zuweisen von Compute-Knoten zum Pool an.</span><span class="sxs-lookup"><span data-stu-id="6c073-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="6c073-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="6c073-149">-StartTask</span></span>
<span data-ttu-id="6c073-150">Gibt die Spezifikation für den Startvorgang für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="6c073-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="6c073-151">Die Startaufgabe wird ausgeführt, wenn ein Compute-Knoten dem Pool Beitritt, oder wenn der Compute-Knoten neu gestartet oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6c073-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="6c073-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="6c073-152">-TargetDedicated</span></span>
<span data-ttu-id="6c073-153">Gibt die Ziel Anzahl der Compute-Knoten an, die dem Pool zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c073-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="6c073-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="6c073-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="6c073-155">Gibt die Aufgaben Planungsrichtlinie an, beispielsweise die ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="6c073-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="6c073-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c073-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="6c073-157">Gibt Konfigurationseinstellungen für einen Pool in der Virtual Machines-Infrastruktur an.</span><span class="sxs-lookup"><span data-stu-id="6c073-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="6c073-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="6c073-158">-VirtualMachineSize</span></span>
<span data-ttu-id="6c073-159">Gibt die Größe der virtuellen Computer im Pool an.</span><span class="sxs-lookup"><span data-stu-id="6c073-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="6c073-160">Weitere Informationen zu Größen für virtuelle Maschinen finden Sie unter Größen für virtuelle Maschinen https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) auf der Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="6c073-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="6c073-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c073-161">-Confirm</span></span>
<span data-ttu-id="6c073-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c073-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c073-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c073-163">-WhatIf</span></span>
<span data-ttu-id="6c073-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c073-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c073-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c073-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c073-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c073-166">-DefaultProfile</span></span>
<span data-ttu-id="6c073-167">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c073-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c073-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c073-168">CommonParameters</span></span>
<span data-ttu-id="6c073-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c073-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c073-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c073-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c073-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c073-171">INPUTS</span></span>

### <span data-ttu-id="6c073-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c073-172">BatchAccountContext</span></span>
<span data-ttu-id="6c073-173">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c073-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="6c073-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c073-174">OUTPUTS</span></span>

## <span data-ttu-id="6c073-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c073-175">NOTES</span></span>

## <span data-ttu-id="6c073-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c073-176">RELATED LINKS</span></span>

[<span data-ttu-id="6c073-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6c073-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6c073-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c073-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="6c073-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c073-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="6c073-180">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6c073-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


