---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: e15dbe0f17f66f6bb8aaad0c4cfb1883ecfb2034
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007452"
---
# <span data-ttu-id="a7ee9-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="a7ee9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ee9-103">Aktualisiert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-103">Updates a Batch job.</span></span>

## <span data-ttu-id="a7ee9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7ee9-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7ee9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7ee9-105">DESCRIPTION</span></span>
<span data-ttu-id="a7ee9-106">Das Cmdlet " **Satz-AzBatchJob** " aktualisiert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a7ee9-107">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a7ee9-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a7ee9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7ee9-109">EXAMPLES</span></span>

### <span data-ttu-id="a7ee9-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="a7ee9-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a7ee9-111">Der erste Befehl ruft einen Auftrag mithilfe von **Get-AzBatchJob** ab und speichert ihn dann in der $Job Variablen.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="a7ee9-112">Der zweite Befehl ändert die Priority-Spezifikation für das $Job-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="a7ee9-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Job entspricht.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a7ee9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7ee9-114">PARAMETERS</span></span>

### <span data-ttu-id="a7ee9-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a7ee9-115">-BatchContext</span></span>
<span data-ttu-id="a7ee9-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7ee9-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7ee9-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7ee9-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7ee9-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7ee9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ee9-121">-DefaultProfile</span></span>
<span data-ttu-id="a7ee9-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7ee9-123">-Job</span><span class="sxs-lookup"><span data-stu-id="a7ee9-123">-Job</span></span>
<span data-ttu-id="a7ee9-124">Gibt einen **PSCloudJob** an, mit dem dieses Cmdlet den Stapelverarbeitungs Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ee9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ee9-125">CommonParameters</span></span>
<span data-ttu-id="a7ee9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ee9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ee9-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7ee9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ee9-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7ee9-128">INPUTS</span></span>

### <span data-ttu-id="a7ee9-129">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a7ee9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7ee9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a7ee9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7ee9-131">OUTPUTS</span></span>

### <span data-ttu-id="a7ee9-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a7ee9-132">System.Void</span></span>

## <span data-ttu-id="a7ee9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7ee9-133">NOTES</span></span>

## <span data-ttu-id="a7ee9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7ee9-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7ee9-135">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a7ee9-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a7ee9-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a7ee9-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a7ee9-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a7ee9-139">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a7ee9-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a7ee9-141">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a7ee9-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="a7ee9-142">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a7ee9-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


