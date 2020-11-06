---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0524a55284d5c93db006248c12aa5a44f40deee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480550"
---
# <span data-ttu-id="c44d9-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c44d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c44d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c44d9-103">Erstellt einen Auftragszeitplan im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c44d9-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c44d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c44d9-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c44d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c44d9-105">DESCRIPTION</span></span>
<span data-ttu-id="c44d9-106">Das Cmdlet **New-AzureBatchJobSchedule** erstellt einen Auftragszeitplan im Azure-Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c44d9-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="c44d9-107">Der Parameter *BatchAccountContext* gibt das Konto an, in dem dieses Cmdlet den Terminplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="c44d9-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="c44d9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c44d9-108">EXAMPLES</span></span>

### <span data-ttu-id="c44d9-109">Beispiel 1: Erstellen eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="c44d9-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="c44d9-110">In diesem Beispiel wird ein Auftragszeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="c44d9-110">This example creates a job schedule.</span></span>
<span data-ttu-id="c44d9-111">Mit den ersten fünf Befehlen werden **PSSchedule** -, **PSJobSpecification** -und **PSPoolInformation** -Objekte erstellt und geändert.</span><span class="sxs-lookup"><span data-stu-id="c44d9-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="c44d9-112">Die Befehle verwenden das New-Object-Cmdlet und die standardmäßige Azure PowerShell-Syntax.</span><span class="sxs-lookup"><span data-stu-id="c44d9-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="c44d9-113">Die Befehle speichern diese Objekte in den Variablen $Schedule und $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="c44d9-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="c44d9-114">Der endgültige Befehl erstellt einen Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c44d9-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c44d9-115">Dieser Zeitplan erstellt Aufträge mit einem Serienintervall von einem Tag.</span><span class="sxs-lookup"><span data-stu-id="c44d9-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="c44d9-116">Die im Pool ausgeführten Aufträge, die die ID-ContosoPool06 aufweisen, wie im fünften Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="c44d9-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="c44d9-117">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c44d9-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c44d9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c44d9-118">PARAMETERS</span></span>

### <span data-ttu-id="c44d9-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c44d9-119">-BatchContext</span></span>
<span data-ttu-id="c44d9-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c44d9-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c44d9-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c44d9-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c44d9-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c44d9-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c44d9-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c44d9-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c44d9-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c44d9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c44d9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44d9-125">-DefaultProfile</span></span>
<span data-ttu-id="c44d9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c44d9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c44d9-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c44d9-127">-DisplayName</span></span>
<span data-ttu-id="c44d9-128">Gibt einen Anzeigenamen für den Auftragszeitplan an.</span><span class="sxs-lookup"><span data-stu-id="c44d9-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="c44d9-129">-ID</span><span class="sxs-lookup"><span data-stu-id="c44d9-129">-Id</span></span>
<span data-ttu-id="c44d9-130">Gibt die ID des vom Cmdlet erstellten Auftragszeitplans an.</span><span class="sxs-lookup"><span data-stu-id="c44d9-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c44d9-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="c44d9-131">-JobSpecification</span></span>
<span data-ttu-id="c44d9-132">Gibt die Details der Aufträge an, die dieses Cmdlet in den Auftragszeitplan einschließt.</span><span class="sxs-lookup"><span data-stu-id="c44d9-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d9-133">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="c44d9-133">-Metadata</span></span>
<span data-ttu-id="c44d9-134">Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftragszeitplan hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c44d9-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="c44d9-135">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c44d9-135">The key is the metadata name.</span></span>
<span data-ttu-id="c44d9-136">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c44d9-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="c44d9-137">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="c44d9-137">-Schedule</span></span>
<span data-ttu-id="c44d9-138">Gibt den Zeitplan an, der festlegt, wann Aufträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c44d9-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44d9-139">CommonParameters</span></span>
<span data-ttu-id="c44d9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44d9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44d9-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44d9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44d9-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c44d9-142">INPUTS</span></span>

### <span data-ttu-id="c44d9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c44d9-143">System.String</span></span>

### <span data-ttu-id="c44d9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c44d9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c44d9-145">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c44d9-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c44d9-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c44d9-146">OUTPUTS</span></span>

### <span data-ttu-id="c44d9-147">System. void</span><span class="sxs-lookup"><span data-stu-id="c44d9-147">System.Void</span></span>

## <span data-ttu-id="c44d9-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c44d9-148">NOTES</span></span>

## <span data-ttu-id="c44d9-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c44d9-149">RELATED LINKS</span></span>

[<span data-ttu-id="c44d9-150">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-150">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c44d9-151">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-151">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c44d9-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c44d9-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c44d9-153">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-153">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c44d9-154">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-154">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c44d9-155">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c44d9-155">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c44d9-156">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c44d9-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


