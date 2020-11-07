---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 59afa8f2ad5b1cf8739bece249d63574c8db6e4c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662115"
---
# <span data-ttu-id="9a9b9-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9a9b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9b9-103">Deaktiviert einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="9a9b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a9b9-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a9b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a9b9-106">Das Cmdlet **Disable-AzBatchJobSchedule** deaktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="9a9b9-107">Wenn Sie einen Terminplan deaktivieren, werden keine Aufträge entsprechend diesem Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="9a9b9-108">Sie können einen deaktivierten Zeitplan später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="9a9b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a9b9-109">EXAMPLES</span></span>

### <span data-ttu-id="9a9b9-110">Beispiel 1: Deaktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="9a9b9-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9a9b9-111">Dieser Befehl deaktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9a9b9-112">Verwenden Sie das Cmdlet **Get-AzBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-112">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9a9b9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a9b9-113">PARAMETERS</span></span>

### <span data-ttu-id="9a9b9-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="9a9b9-114">-BatchContext</span></span>
<span data-ttu-id="9a9b9-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9a9b9-116">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9a9b9-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9a9b9-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9a9b9-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9a9b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9b9-120">-DefaultProfile</span></span>
<span data-ttu-id="9a9b9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a9b9-122">-ID</span><span class="sxs-lookup"><span data-stu-id="9a9b9-122">-Id</span></span>
<span data-ttu-id="9a9b9-123">Gibt die ID des Auftragszeitplans an, der vom Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9b9-124">CommonParameters</span></span>
<span data-ttu-id="9a9b9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9b9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9b9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a9b9-127">INPUTS</span></span>

### <span data-ttu-id="9a9b9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a9b9-128">System.String</span></span>

### <span data-ttu-id="9a9b9-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9a9b9-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9a9b9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a9b9-130">OUTPUTS</span></span>

### <span data-ttu-id="9a9b9-131">System. void</span><span class="sxs-lookup"><span data-stu-id="9a9b9-131">System.Void</span></span>

## <span data-ttu-id="9a9b9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a9b9-132">NOTES</span></span>

## <span data-ttu-id="9a9b9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a9b9-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a9b9-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9a9b9-135">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9a9b9-135">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9a9b9-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9a9b9-137">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9a9b9-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9a9b9-139">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9a9b9-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="9a9b9-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9a9b9-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


