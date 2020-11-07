---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665274"
---
# <span data-ttu-id="0601f-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0601f-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="0601f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0601f-102">SYNOPSIS</span></span>
<span data-ttu-id="0601f-103">Ruft Batch Pools unter dem angegebenen Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="0601f-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0601f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0601f-104">SYNTAX</span></span>

### <span data-ttu-id="0601f-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0601f-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0601f-106">ID</span><span class="sxs-lookup"><span data-stu-id="0601f-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0601f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0601f-107">DESCRIPTION</span></span>
<span data-ttu-id="0601f-108">Das Cmdlet " **Get-AzureBatchPool** " Ruft die Azure-Batch Pools unter dem Batch Konto ab, das mit dem *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0601f-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="0601f-109">Sie können den *ID-* Parameter verwenden, um einen einzelnen Pool abzurufen, oder Sie können den *Filter* -Parameter verwenden, um die Pools abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0601f-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="0601f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0601f-110">EXAMPLES</span></span>

### <span data-ttu-id="0601f-111">Beispiel 1: Abrufen eines Pools nach ID</span><span class="sxs-lookup"><span data-stu-id="0601f-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="0601f-112">Dieser Befehl ruft den Pool mit der ID MyPool ab.</span><span class="sxs-lookup"><span data-stu-id="0601f-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="0601f-113">Beispiel 2: Abrufen aller Pools mit einem OData-Filter</span><span class="sxs-lookup"><span data-stu-id="0601f-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="0601f-114">Dieser Befehl ruft die Pools ab, deren IDs mit "My" beginnen, indem Sie den *Filter* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="0601f-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="0601f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0601f-115">PARAMETERS</span></span>

### <span data-ttu-id="0601f-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="0601f-116">-BatchContext</span></span>
<span data-ttu-id="0601f-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0601f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0601f-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0601f-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0601f-119">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="0601f-119">-Expand</span></span>
<span data-ttu-id="0601f-120">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="0601f-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="0601f-121">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="0601f-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="0601f-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="0601f-122">-Filter</span></span>
<span data-ttu-id="0601f-123">Gibt die OData-Filterklausel an, die beim Abfragen für Pools verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0601f-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="0601f-124">Wenn Sie keinen Filter angeben, werden alle Pools unter dem mit dem *batchcontext* -Parameter angegebenen Batch Konto zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0601f-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0601f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="0601f-125">-Id</span></span>
<span data-ttu-id="0601f-126">Gibt die ID des abzurufenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="0601f-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="0601f-127">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="0601f-127">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0601f-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0601f-128">-MaxCount</span></span>
<span data-ttu-id="0601f-129">Gibt die maximale Anzahl von Pools an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0601f-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="0601f-130">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="0601f-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0601f-131">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="0601f-131">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0601f-132">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="0601f-132">-Select</span></span>
<span data-ttu-id="0601f-133">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="0601f-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="0601f-134">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0601f-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="0601f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0601f-135">-DefaultProfile</span></span>
<span data-ttu-id="0601f-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0601f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0601f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0601f-137">CommonParameters</span></span>
<span data-ttu-id="0601f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0601f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0601f-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0601f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0601f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0601f-140">INPUTS</span></span>

### <span data-ttu-id="0601f-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0601f-141">BatchAccountContext</span></span>
<span data-ttu-id="0601f-142">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0601f-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0601f-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0601f-143">String</span></span>
<span data-ttu-id="0601f-144">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0601f-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0601f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0601f-145">OUTPUTS</span></span>

### <span data-ttu-id="0601f-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="0601f-146">PSCloudPool</span></span>

## <span data-ttu-id="0601f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="0601f-147">NOTES</span></span>

## <span data-ttu-id="0601f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0601f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0601f-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0601f-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0601f-150">Neu – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0601f-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="0601f-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0601f-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="0601f-152">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0601f-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


