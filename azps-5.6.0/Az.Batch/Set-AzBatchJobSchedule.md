---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945317"
---
# <span data-ttu-id="4b845-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="4b845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b845-102">SYNOPSIS</span></span>
<span data-ttu-id="4b845-103">Legt einen Auftragszeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="4b845-103">Sets a job schedule.</span></span>

## <span data-ttu-id="4b845-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b845-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b845-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b845-105">DESCRIPTION</span></span>
<span data-ttu-id="4b845-106">Das **Cmdlet Set-AzBatchJobSchedule** legt einen Auftragszeitplan im Azure Batch-Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="4b845-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="4b845-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b845-107">EXAMPLES</span></span>

### <span data-ttu-id="4b845-108">Beispiel 1: Aktualisieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="4b845-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="4b845-109">Der erste Befehl ruft einen Auftrag mithilfe von **Get-AzBatchJobSchedule** ab und speichert ihn dann in der $JobSchedule Variablen.</span><span class="sxs-lookup"><span data-stu-id="4b845-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="4b845-110">Mit dem zweiten Befehl wird das Serienintervall für das -Objekt `$JobSchedule.Schedule` geändert.</span><span class="sxs-lookup"><span data-stu-id="4b845-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="4b845-111">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="4b845-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="4b845-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4b845-112">PARAMETERS</span></span>

### <span data-ttu-id="4b845-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4b845-113">-BatchContext</span></span>
<span data-ttu-id="4b845-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b845-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4b845-115">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b845-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4b845-116">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b845-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4b845-117">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b845-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4b845-118">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="4b845-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4b845-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b845-119">-DefaultProfile</span></span>
<span data-ttu-id="4b845-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b845-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b845-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-121">-JobSchedule</span></span>
<span data-ttu-id="4b845-122">Gibt ein **PSCloudJobSchedule-Objekt an,** das einen Auftragszeitplan darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b845-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="4b845-123">Um ein **PSCloudJobSchedule-Objekt zu** erhalten, verwenden Sie das Get-AzBatchJobSchedule Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b845-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b845-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b845-124">CommonParameters</span></span>
<span data-ttu-id="4b845-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b845-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b845-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b845-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b845-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b845-127">INPUTS</span></span>

### <span data-ttu-id="4b845-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="4b845-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4b845-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4b845-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b845-130">OUTPUTS</span></span>

### <span data-ttu-id="4b845-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="4b845-131">System.Void</span></span>

## <span data-ttu-id="4b845-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4b845-132">NOTES</span></span>

## <span data-ttu-id="4b845-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4b845-133">RELATED LINKS</span></span>

[<span data-ttu-id="4b845-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="4b845-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="4b845-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="4b845-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="4b845-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="4b845-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4b845-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


