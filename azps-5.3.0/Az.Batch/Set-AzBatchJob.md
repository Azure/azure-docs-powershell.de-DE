---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471099"
---
# <span data-ttu-id="19938-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="19938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19938-102">SYNOPSIS</span></span>
<span data-ttu-id="19938-103">Aktualisiert einen Batchauftrag.</span><span class="sxs-lookup"><span data-stu-id="19938-103">Updates a Batch job.</span></span>

## <span data-ttu-id="19938-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19938-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19938-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19938-105">DESCRIPTION</span></span>
<span data-ttu-id="19938-106">Das **Cmdlet "Set-AzBatchJob"** aktualisiert einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="19938-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="19938-107">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **"PSCloudJob"-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="19938-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="19938-108">Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.</span><span class="sxs-lookup"><span data-stu-id="19938-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="19938-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19938-109">EXAMPLES</span></span>

### <span data-ttu-id="19938-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="19938-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="19938-111">Der erste Befehl ruft einen Auftrag mithilfe von **"Get-AzBatchJob"** ab und speichert ihn dann in der $Job Variable.</span><span class="sxs-lookup"><span data-stu-id="19938-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="19938-112">Mit dem zweiten Befehl wird die Prioritätsspezifikation für das $Job geändert.</span><span class="sxs-lookup"><span data-stu-id="19938-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="19938-113">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in der $Job.</span><span class="sxs-lookup"><span data-stu-id="19938-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="19938-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19938-114">PARAMETERS</span></span>

### <span data-ttu-id="19938-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="19938-115">-BatchContext</span></span>
<span data-ttu-id="19938-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19938-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19938-117">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="19938-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="19938-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="19938-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="19938-119">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="19938-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="19938-120">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19938-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="19938-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19938-121">-DefaultProfile</span></span>
<span data-ttu-id="19938-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19938-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19938-123">-Job</span><span class="sxs-lookup"><span data-stu-id="19938-123">-Job</span></span>
<span data-ttu-id="19938-124">Gibt einen **PSCloudJob an,** auf den dieses Cmdlet den Batchdienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="19938-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="19938-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19938-125">CommonParameters</span></span>
<span data-ttu-id="19938-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19938-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19938-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19938-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19938-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19938-128">INPUTS</span></span>

### <span data-ttu-id="19938-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="19938-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="19938-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19938-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="19938-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19938-131">OUTPUTS</span></span>

### <span data-ttu-id="19938-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="19938-132">System.Void</span></span>

## <span data-ttu-id="19938-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19938-133">NOTES</span></span>

## <span data-ttu-id="19938-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19938-134">RELATED LINKS</span></span>

[<span data-ttu-id="19938-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="19938-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="19938-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="19938-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="19938-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="19938-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="19938-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="19938-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19938-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="19938-142">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="19938-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
