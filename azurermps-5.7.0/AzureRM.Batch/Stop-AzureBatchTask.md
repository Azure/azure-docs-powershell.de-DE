---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478710"
---
# <span data-ttu-id="ed0de-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ed0de-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="ed0de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed0de-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0de-103">Beendet eine Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ed0de-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed0de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed0de-104">SYNTAX</span></span>

### <span data-ttu-id="ed0de-105">ID</span><span class="sxs-lookup"><span data-stu-id="ed0de-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed0de-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed0de-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed0de-107">DESCRIPTION</span></span>
<span data-ttu-id="ed0de-108">Das Cmdlet **Stop-AzureBatchTask** beendet eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ed0de-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="ed0de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed0de-109">EXAMPLES</span></span>

### <span data-ttu-id="ed0de-110">Beispiel 1: Löschen einer stapelverarbeitungsaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="ed0de-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="ed0de-111">Dieser Befehl beendet eine Aufgabe mit der ID Task23 unter dem Auftrag, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="ed0de-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ed0de-112">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="ed0de-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ed0de-113">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ed0de-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ed0de-114">Beispiel 2: Beenden einer Batch Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ed0de-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="ed0de-115">Dieser Befehl ruft die Batch Aufgabe mit der ID Task26 in dem Auftrag ab, der die ID Job-000001 mit dem Get-AzureBatchTask-Cmdlet aufweist.</span><span class="sxs-lookup"><span data-stu-id="ed0de-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="ed0de-116">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed0de-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed0de-117">Der Befehl beendet die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ed0de-117">The command stops that task.</span></span>

## <span data-ttu-id="ed0de-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed0de-118">PARAMETERS</span></span>

### <span data-ttu-id="ed0de-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ed0de-119">-BatchContext</span></span>
<span data-ttu-id="ed0de-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed0de-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed0de-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed0de-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed0de-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed0de-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed0de-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed0de-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed0de-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ed0de-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ed0de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0de-125">-DefaultProfile</span></span>
<span data-ttu-id="ed0de-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed0de-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0de-127">-ID</span><span class="sxs-lookup"><span data-stu-id="ed0de-127">-Id</span></span>
<span data-ttu-id="ed0de-128">Gibt die ID der Aufgabe an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed0de-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0de-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="ed0de-129">-JobId</span></span>
<span data-ttu-id="ed0de-130">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="ed0de-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0de-131">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ed0de-131">-Task</span></span>
<span data-ttu-id="ed0de-132">Gibt die Aufgabe an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed0de-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="ed0de-133">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed0de-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0de-134">CommonParameters</span></span>
<span data-ttu-id="ed0de-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0de-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0de-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0de-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed0de-137">INPUTS</span></span>

### <span data-ttu-id="ed0de-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ed0de-138">BatchAccountContext</span></span>
<span data-ttu-id="ed0de-139">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed0de-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ed0de-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ed0de-140">PSCloudTask</span></span>
<span data-ttu-id="ed0de-141">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed0de-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ed0de-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed0de-142">OUTPUTS</span></span>

## <span data-ttu-id="ed0de-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed0de-143">NOTES</span></span>

## <span data-ttu-id="ed0de-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed0de-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed0de-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ed0de-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ed0de-146">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ed0de-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ed0de-147">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ed0de-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ed0de-148">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ed0de-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


