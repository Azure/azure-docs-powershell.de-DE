---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176100"
---
# <span data-ttu-id="1aff4-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="1aff4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aff4-102">SYNOPSIS</span></span>
<span data-ttu-id="1aff4-103">Aktualisiert einen Batchauftrag.</span><span class="sxs-lookup"><span data-stu-id="1aff4-103">Updates a Batch job.</span></span>

## <span data-ttu-id="1aff4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aff4-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aff4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1aff4-105">DESCRIPTION</span></span>
<span data-ttu-id="1aff4-106">Das **Cmdlet "Set-AzBatchJob"** aktualisiert einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="1aff4-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="1aff4-107">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **"PSCloudJob"-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="1aff4-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="1aff4-108">Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.</span><span class="sxs-lookup"><span data-stu-id="1aff4-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1aff4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1aff4-109">EXAMPLES</span></span>

### <span data-ttu-id="1aff4-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="1aff4-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="1aff4-111">Der erste Befehl ruft einen Auftrag mithilfe von **"Get-AzBatchJob"** ab und speichert ihn dann in der $Job Variable.</span><span class="sxs-lookup"><span data-stu-id="1aff4-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="1aff4-112">Mit dem zweiten Befehl wird die Prioritätsspezifikation für das $Job geändert.</span><span class="sxs-lookup"><span data-stu-id="1aff4-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="1aff4-113">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in der $Job.</span><span class="sxs-lookup"><span data-stu-id="1aff4-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="1aff4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aff4-114">PARAMETERS</span></span>

### <span data-ttu-id="1aff4-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1aff4-115">-BatchContext</span></span>
<span data-ttu-id="1aff4-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1aff4-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1aff4-117">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1aff4-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1aff4-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1aff4-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1aff4-119">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1aff4-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1aff4-120">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1aff4-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1aff4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aff4-121">-DefaultProfile</span></span>
<span data-ttu-id="1aff4-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aff4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aff4-123">-Job</span><span class="sxs-lookup"><span data-stu-id="1aff4-123">-Job</span></span>
<span data-ttu-id="1aff4-124">Gibt einen **PSCloudJob an,** an den dieses Cmdlet den Batchdienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1aff4-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="1aff4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aff4-125">CommonParameters</span></span>
<span data-ttu-id="1aff4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aff4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aff4-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aff4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aff4-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1aff4-128">INPUTS</span></span>

### <span data-ttu-id="1aff4-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1aff4-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1aff4-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1aff4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1aff4-131">OUTPUTS</span></span>

### <span data-ttu-id="1aff4-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="1aff4-132">System.Void</span></span>

## <span data-ttu-id="1aff4-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1aff4-133">NOTES</span></span>

## <span data-ttu-id="1aff4-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1aff4-134">RELATED LINKS</span></span>

[<span data-ttu-id="1aff4-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="1aff4-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1aff4-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1aff4-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1aff4-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1aff4-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1aff4-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1aff4-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1aff4-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1aff4-142">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1aff4-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
