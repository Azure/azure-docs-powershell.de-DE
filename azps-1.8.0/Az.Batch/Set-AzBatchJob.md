---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662032"
---
# <span data-ttu-id="b42b0-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="b42b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b42b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b42b0-103">Aktualisiert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b42b0-103">Updates a Batch job.</span></span>

## <span data-ttu-id="b42b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b42b0-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b42b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b42b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b42b0-106">Das Cmdlet " **Satz-AzBatchJob** " aktualisiert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b42b0-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="b42b0-107">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b42b0-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="b42b0-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="b42b0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b42b0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b42b0-109">EXAMPLES</span></span>

### <span data-ttu-id="b42b0-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="b42b0-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="b42b0-111">Der erste Befehl ruft einen Auftrag mithilfe von **Get-AzBatchJob** ab und speichert ihn dann in der $Job Variablen.</span><span class="sxs-lookup"><span data-stu-id="b42b0-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="b42b0-112">Der zweite Befehl ändert die Priority-Spezifikation für das $Job-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b42b0-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="b42b0-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Job entspricht.</span><span class="sxs-lookup"><span data-stu-id="b42b0-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="b42b0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b42b0-114">PARAMETERS</span></span>

### <span data-ttu-id="b42b0-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b42b0-115">-BatchContext</span></span>
<span data-ttu-id="b42b0-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b42b0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b42b0-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b42b0-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b42b0-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b42b0-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b42b0-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="b42b0-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b42b0-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="b42b0-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b42b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42b0-121">-DefaultProfile</span></span>
<span data-ttu-id="b42b0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b42b0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b42b0-123">-Job</span><span class="sxs-lookup"><span data-stu-id="b42b0-123">-Job</span></span>
<span data-ttu-id="b42b0-124">Gibt einen **PSCloudJob** an, mit dem dieses Cmdlet den Stapelverarbeitungs Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b42b0-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="b42b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42b0-125">CommonParameters</span></span>
<span data-ttu-id="b42b0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b42b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42b0-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b42b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42b0-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b42b0-128">INPUTS</span></span>

### <span data-ttu-id="b42b0-129">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="b42b0-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b42b0-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b42b0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b42b0-131">OUTPUTS</span></span>

### <span data-ttu-id="b42b0-132">System. void</span><span class="sxs-lookup"><span data-stu-id="b42b0-132">System.Void</span></span>

## <span data-ttu-id="b42b0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b42b0-133">NOTES</span></span>

## <span data-ttu-id="b42b0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b42b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b42b0-135">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b42b0-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b42b0-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b42b0-138">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b42b0-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b42b0-139">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b42b0-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b42b0-141">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b42b0-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b42b0-142">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b42b0-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


