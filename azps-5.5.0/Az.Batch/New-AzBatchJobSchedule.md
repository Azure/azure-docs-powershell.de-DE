---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162489"
---
# <span data-ttu-id="be969-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="be969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be969-102">SYNOPSIS</span></span>
<span data-ttu-id="be969-103">Erstellt einen Auftragszeitplan im Batchdienst.</span><span class="sxs-lookup"><span data-stu-id="be969-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="be969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be969-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be969-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be969-105">DESCRIPTION</span></span>
<span data-ttu-id="be969-106">Das **Cmdlet "New-AzBatchJobSchedule"** erstellt einen Auftragszeitplan im Azure Batch-Dienst.</span><span class="sxs-lookup"><span data-stu-id="be969-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="be969-107">Der *Parameter "BatchAccountContext"* gibt das Konto an, in dem dieses Cmdlet den Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="be969-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="be969-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be969-108">EXAMPLES</span></span>

### <span data-ttu-id="be969-109">Beispiel 1: Erstellen eines Stellenplans</span><span class="sxs-lookup"><span data-stu-id="be969-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="be969-110">In diesem Beispiel wird ein Stellenplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="be969-110">This example creates a job schedule.</span></span>
<span data-ttu-id="be969-111">Die ersten fünf Befehle erstellen und ändern **psSchedule-,** **PSJobSpecification-** und **PSPoolInformation-Objekte.**</span><span class="sxs-lookup"><span data-stu-id="be969-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="be969-112">Für die Befehle werden das New-Object und die standardmäßige Azure New-Object verwendet.</span><span class="sxs-lookup"><span data-stu-id="be969-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="be969-113">Die Befehle speichern diese Objekte in den $Schedule und $JobSpecification Variablen.</span><span class="sxs-lookup"><span data-stu-id="be969-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="be969-114">Der letzte Befehl erstellt einen Auftragszeitplan mit der ID "JobSchedule17".</span><span class="sxs-lookup"><span data-stu-id="be969-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="be969-115">Mit diesem Zeitplan werden Aufträge mit einem Wiederholungsintervall von einem Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="be969-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="be969-116">Die Aufträge werden für den Pool ausgeführt, der die ID "ContosoPool06" hat, wie im fünften Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="be969-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="be969-117">Verwenden Sie **das Cmdlet "Get-AzBatchAccountKey",** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="be969-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="be969-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be969-118">PARAMETERS</span></span>

### <span data-ttu-id="be969-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="be969-119">-BatchContext</span></span>
<span data-ttu-id="be969-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be969-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="be969-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="be969-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="be969-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="be969-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="be969-123">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="be969-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="be969-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be969-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="be969-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be969-125">-DefaultProfile</span></span>
<span data-ttu-id="be969-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be969-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be969-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="be969-127">-DisplayName</span></span>
<span data-ttu-id="be969-128">Gibt einen Anzeigenamen für den Auftragszeitplan an.</span><span class="sxs-lookup"><span data-stu-id="be969-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="be969-129">-ID</span><span class="sxs-lookup"><span data-stu-id="be969-129">-Id</span></span>
<span data-ttu-id="be969-130">Gibt die ID des Auftragsplans an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="be969-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="be969-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="be969-131">-JobSpecification</span></span>
<span data-ttu-id="be969-132">Gibt die Details der Aufträge an, die dieses Cmdlet im Auftragszeitplan enthält.</span><span class="sxs-lookup"><span data-stu-id="be969-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="be969-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="be969-133">-Metadata</span></span>
<span data-ttu-id="be969-134">Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftragszeitplan hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="be969-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="be969-135">Der Schlüssel ist der Metadatenname.</span><span class="sxs-lookup"><span data-stu-id="be969-135">The key is the metadata name.</span></span>
<span data-ttu-id="be969-136">Der Wert ist der Metadatenwert.</span><span class="sxs-lookup"><span data-stu-id="be969-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="be969-137">-Schedule</span><span class="sxs-lookup"><span data-stu-id="be969-137">-Schedule</span></span>
<span data-ttu-id="be969-138">Gibt den Zeitplan an, der bestimmt, wann Aufträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be969-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="be969-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be969-139">CommonParameters</span></span>
<span data-ttu-id="be969-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be969-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be969-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be969-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be969-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be969-142">INPUTS</span></span>

### <span data-ttu-id="be969-143">System.String</span><span class="sxs-lookup"><span data-stu-id="be969-143">System.String</span></span>

### <span data-ttu-id="be969-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="be969-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="be969-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be969-145">OUTPUTS</span></span>

### <span data-ttu-id="be969-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="be969-146">System.Void</span></span>

## <span data-ttu-id="be969-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be969-147">NOTES</span></span>

## <span data-ttu-id="be969-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be969-148">RELATED LINKS</span></span>

[<span data-ttu-id="be969-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="be969-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="be969-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="be969-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="be969-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="be969-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="be969-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="be969-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="be969-155">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="be969-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
