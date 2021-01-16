---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294622"
---
# <span data-ttu-id="d89a3-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="d89a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d89a3-103">Legt einen Auftragszeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="d89a3-103">Sets a job schedule.</span></span>

## <span data-ttu-id="d89a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d89a3-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89a3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d89a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d89a3-106">Das **Cmdlet "Set-AzBatchJobSchedule"** legt einen Auftragszeitplan im Azure -Batchdienst fest.</span><span class="sxs-lookup"><span data-stu-id="d89a3-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="d89a3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d89a3-107">EXAMPLES</span></span>

### <span data-ttu-id="d89a3-108">Beispiel 1: Aktualisieren eines Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="d89a3-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="d89a3-109">Der erste Befehl ruft einen Auftrag mithilfe von **"Get-AzBatchJobSchedule"** ab und speichert ihn dann in der $JobSchedule Variable.</span><span class="sxs-lookup"><span data-stu-id="d89a3-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="d89a3-110">Der zweite Befehl ändert das Wiederholungsintervall für das `$JobSchedule.Schedule` Objekt.</span><span class="sxs-lookup"><span data-stu-id="d89a3-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="d89a3-111">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in der $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="d89a3-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="d89a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d89a3-112">PARAMETERS</span></span>

### <span data-ttu-id="d89a3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d89a3-113">-BatchContext</span></span>
<span data-ttu-id="d89a3-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d89a3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d89a3-115">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d89a3-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d89a3-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d89a3-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d89a3-117">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="d89a3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d89a3-118">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d89a3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d89a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89a3-119">-DefaultProfile</span></span>
<span data-ttu-id="d89a3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d89a3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89a3-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-121">-JobSchedule</span></span>
<span data-ttu-id="d89a3-122">Gibt ein **PSCloudJobSchedule-Objekt** an, das einen Auftragszeitplan darstellt.</span><span class="sxs-lookup"><span data-stu-id="d89a3-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="d89a3-123">Verwenden Sie zum Abrufen **eines PSCloudJobSchedule-Objekts** das Get-AzBatchJobSchedule Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d89a3-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="d89a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89a3-124">CommonParameters</span></span>
<span data-ttu-id="d89a3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89a3-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d89a3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89a3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d89a3-127">INPUTS</span></span>

### <span data-ttu-id="d89a3-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="d89a3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d89a3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d89a3-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d89a3-130">OUTPUTS</span></span>

### <span data-ttu-id="d89a3-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="d89a3-131">System.Void</span></span>

## <span data-ttu-id="d89a3-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d89a3-132">NOTES</span></span>

## <span data-ttu-id="d89a3-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d89a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="d89a3-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="d89a3-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="d89a3-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d89a3-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="d89a3-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="d89a3-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d89a3-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


