---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503073"
---
# <span data-ttu-id="ed7e1-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="ed7e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7e1-103">Aktualisiert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed7e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7e1-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed7e1-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7e1-106">Das Cmdlet " **Satz-AzureBatchJob** " aktualisiert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="ed7e1-107">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="ed7e1-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="ed7e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed7e1-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7e1-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="ed7e1-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="ed7e1-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzureBatchJob** ab und speichert ihn dann in der $Job-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="ed7e1-112">Der zweite Befehl ändert die Priority-Spezifikation für das $Job-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="ed7e1-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Job entspricht.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="ed7e1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed7e1-114">PARAMETERS</span></span>

### <span data-ttu-id="ed7e1-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ed7e1-115">-BatchContext</span></span>
<span data-ttu-id="ed7e1-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed7e1-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed7e1-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed7e1-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed7e1-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ed7e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7e1-121">-DefaultProfile</span></span>
<span data-ttu-id="ed7e1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed7e1-123">-Job</span><span class="sxs-lookup"><span data-stu-id="ed7e1-123">-Job</span></span>
<span data-ttu-id="ed7e1-124">Gibt einen **PSCloudJob** an, mit dem dieses Cmdlet den Stapelverarbeitungs Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7e1-125">CommonParameters</span></span>
<span data-ttu-id="ed7e1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7e1-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7e1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7e1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed7e1-128">INPUTS</span></span>

### <span data-ttu-id="ed7e1-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ed7e1-129">BatchAccountContext</span></span>
<span data-ttu-id="ed7e1-130">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ed7e1-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-131">PSCloudJob</span></span>
<span data-ttu-id="ed7e1-132">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' PSCloudJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="ed7e1-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed7e1-133">OUTPUTS</span></span>

## <span data-ttu-id="ed7e1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed7e1-134">NOTES</span></span>

## <span data-ttu-id="ed7e1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed7e1-135">RELATED LINKS</span></span>

[<span data-ttu-id="ed7e1-136">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ed7e1-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ed7e1-140">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-142">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ed7e1-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="ed7e1-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ed7e1-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


