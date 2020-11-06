---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497901"
---
# <span data-ttu-id="79d82-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="79d82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79d82-102">SYNOPSIS</span></span>
<span data-ttu-id="79d82-103">Erstellt einen Auftragszeitplan im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="79d82-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79d82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79d82-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79d82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79d82-105">DESCRIPTION</span></span>
<span data-ttu-id="79d82-106">Das Cmdlet **New-AzureBatchJobSchedule** erstellt einen Auftragszeitplan im Azure-Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="79d82-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="79d82-107">Der Parameter *BatchAccountContext* gibt das Konto an, in dem dieses Cmdlet den Terminplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="79d82-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="79d82-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79d82-108">EXAMPLES</span></span>

### <span data-ttu-id="79d82-109">Beispiel 1: Erstellen eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="79d82-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="79d82-110">In diesem Beispiel wird ein Auftragszeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="79d82-110">This example creates a job schedule.</span></span>

<span data-ttu-id="79d82-111">Mit den ersten fünf Befehlen werden **PSSchedule** -, **PSJobSpecification** -und **PSPoolInformation** -Objekte erstellt und geändert.</span><span class="sxs-lookup"><span data-stu-id="79d82-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="79d82-112">Die Befehle verwenden das New-Object-Cmdlet und die standardmäßige Azure PowerShell-Syntax.</span><span class="sxs-lookup"><span data-stu-id="79d82-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="79d82-113">Die Befehle speichern diese Objekte in den Variablen $Schedule und $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="79d82-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="79d82-114">Der endgültige Befehl erstellt einen Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="79d82-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="79d82-115">Dieser Zeitplan erstellt Aufträge mit einem Serienintervall von einem Tag.</span><span class="sxs-lookup"><span data-stu-id="79d82-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="79d82-116">Die im Pool ausgeführten Aufträge, die die ID-ContosoPool06 aufweisen, wie im fünften Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="79d82-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="79d82-117">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="79d82-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="79d82-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="79d82-118">PARAMETERS</span></span>

### <span data-ttu-id="79d82-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="79d82-119">-BatchContext</span></span>
<span data-ttu-id="79d82-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="79d82-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79d82-121">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79d82-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="79d82-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="79d82-122">-DisplayName</span></span>
<span data-ttu-id="79d82-123">Gibt einen Anzeigenamen für den Auftragszeitplan an.</span><span class="sxs-lookup"><span data-stu-id="79d82-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="79d82-124">-ID</span><span class="sxs-lookup"><span data-stu-id="79d82-124">-Id</span></span>
<span data-ttu-id="79d82-125">Gibt die ID des vom Cmdlet erstellten Auftragszeitplans an.</span><span class="sxs-lookup"><span data-stu-id="79d82-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="79d82-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="79d82-126">-JobSpecification</span></span>
<span data-ttu-id="79d82-127">Gibt die Details der Aufträge an, die dieses Cmdlet in den Auftragszeitplan einschließt.</span><span class="sxs-lookup"><span data-stu-id="79d82-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="79d82-128">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="79d82-128">-Metadata</span></span>
<span data-ttu-id="79d82-129">Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftragszeitplan hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79d82-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="79d82-130">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="79d82-130">The key is the metadata name.</span></span>
<span data-ttu-id="79d82-131">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="79d82-131">The value is the metadata value.</span></span>

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

### <span data-ttu-id="79d82-132">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="79d82-132">-Schedule</span></span>
<span data-ttu-id="79d82-133">Gibt den Zeitplan an, der festlegt, wann Aufträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79d82-133">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="79d82-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d82-134">-DefaultProfile</span></span>
<span data-ttu-id="79d82-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79d82-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79d82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d82-136">CommonParameters</span></span>
<span data-ttu-id="79d82-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d82-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79d82-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d82-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79d82-139">INPUTS</span></span>

### <span data-ttu-id="79d82-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79d82-140">BatchAccountContext</span></span>
<span data-ttu-id="79d82-141">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="79d82-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="79d82-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79d82-142">OUTPUTS</span></span>

## <span data-ttu-id="79d82-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="79d82-143">NOTES</span></span>

## <span data-ttu-id="79d82-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79d82-144">RELATED LINKS</span></span>

[<span data-ttu-id="79d82-145">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="79d82-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="79d82-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="79d82-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="79d82-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="79d82-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="79d82-150">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79d82-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="79d82-151">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="79d82-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


