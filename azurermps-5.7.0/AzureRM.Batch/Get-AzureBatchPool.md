---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478762"
---
# <span data-ttu-id="cb14d-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cb14d-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="cb14d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb14d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb14d-103">Ruft Batch Pools unter dem angegebenen Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="cb14d-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb14d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb14d-104">SYNTAX</span></span>

### <span data-ttu-id="cb14d-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb14d-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb14d-106">ID</span><span class="sxs-lookup"><span data-stu-id="cb14d-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb14d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb14d-107">DESCRIPTION</span></span>
<span data-ttu-id="cb14d-108">Das Cmdlet " **Get-AzureBatchPool** " Ruft die Azure-Batch Pools unter dem Batch Konto ab, das mit dem *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb14d-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="cb14d-109">Sie können den *ID-* Parameter verwenden, um einen einzelnen Pool abzurufen, oder Sie können den *Filter* -Parameter verwenden, um die Pools abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cb14d-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="cb14d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb14d-110">EXAMPLES</span></span>

### <span data-ttu-id="cb14d-111">Beispiel 1: Abrufen eines Pools nach ID</span><span class="sxs-lookup"><span data-stu-id="cb14d-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="cb14d-112">Dieser Befehl ruft den Pool mit der ID MyPool ab.</span><span class="sxs-lookup"><span data-stu-id="cb14d-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="cb14d-113">Beispiel 2: Abrufen aller Pools mit einem OData-Filter</span><span class="sxs-lookup"><span data-stu-id="cb14d-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="cb14d-114">Dieser Befehl ruft die Pools ab, deren IDs mit "My" beginnen, indem Sie den *Filter* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb14d-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="cb14d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb14d-115">PARAMETERS</span></span>

### <span data-ttu-id="cb14d-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cb14d-116">-BatchContext</span></span>
<span data-ttu-id="cb14d-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb14d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb14d-118">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb14d-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cb14d-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb14d-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cb14d-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb14d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cb14d-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cb14d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cb14d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb14d-122">-DefaultProfile</span></span>
<span data-ttu-id="cb14d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb14d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb14d-124">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="cb14d-124">-Expand</span></span>
<span data-ttu-id="cb14d-125">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="cb14d-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="cb14d-126">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="cb14d-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="cb14d-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="cb14d-127">-Filter</span></span>
<span data-ttu-id="cb14d-128">Gibt die OData-Filterklausel an, die beim Abfragen für Pools verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb14d-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="cb14d-129">Wenn Sie keinen Filter angeben, werden alle Pools unter dem mit dem *batchcontext* -Parameter angegebenen Batch Konto zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb14d-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14d-130">-ID</span><span class="sxs-lookup"><span data-stu-id="cb14d-130">-Id</span></span>
<span data-ttu-id="cb14d-131">Gibt die ID des abzurufenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="cb14d-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="cb14d-132">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="cb14d-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb14d-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cb14d-133">-MaxCount</span></span>
<span data-ttu-id="cb14d-134">Gibt die maximale Anzahl von Pools an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb14d-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="cb14d-135">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="cb14d-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="cb14d-136">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="cb14d-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14d-137">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="cb14d-137">-Select</span></span>
<span data-ttu-id="cb14d-138">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="cb14d-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="cb14d-139">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb14d-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="cb14d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb14d-140">CommonParameters</span></span>
<span data-ttu-id="cb14d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb14d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb14d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb14d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb14d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb14d-143">INPUTS</span></span>

### <span data-ttu-id="cb14d-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb14d-144">BatchAccountContext</span></span>
<span data-ttu-id="cb14d-145">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb14d-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cb14d-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cb14d-146">String</span></span>
<span data-ttu-id="cb14d-147">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb14d-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cb14d-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb14d-148">OUTPUTS</span></span>

### <span data-ttu-id="cb14d-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="cb14d-149">PSCloudPool</span></span>

## <span data-ttu-id="cb14d-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb14d-150">NOTES</span></span>

## <span data-ttu-id="cb14d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb14d-151">RELATED LINKS</span></span>

[<span data-ttu-id="cb14d-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cb14d-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cb14d-153">Neu – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cb14d-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="cb14d-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cb14d-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="cb14d-155">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cb14d-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


