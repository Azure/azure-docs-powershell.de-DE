---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820932"
---
# <span data-ttu-id="d67e0-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="d67e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d67e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d67e0-103">Legt einen Auftragszeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="d67e0-103">Sets a job schedule.</span></span>

## <span data-ttu-id="d67e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d67e0-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d67e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d67e0-106">Das Cmdlet " **Set-AzBatchJobSchedule** " legt einen Auftragszeitplan im Azure-Batch Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="d67e0-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="d67e0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d67e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d67e0-108">Beispiel 1: Aktualisieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="d67e0-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="d67e0-109">Der erste Befehl ruft einen Auftrag mithilfe von **Get-AzBatchJobSchedule** ab und speichert ihn dann in der $JobSchedule Variablen.</span><span class="sxs-lookup"><span data-stu-id="d67e0-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="d67e0-110">Der zweite Befehl ändert das Serienintervall für das `$JobSchedule.Schedule` Objekt.</span><span class="sxs-lookup"><span data-stu-id="d67e0-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="d67e0-111">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $JobSchedule entspricht.</span><span class="sxs-lookup"><span data-stu-id="d67e0-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="d67e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d67e0-112">PARAMETERS</span></span>

### <span data-ttu-id="d67e0-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="d67e0-113">-BatchContext</span></span>
<span data-ttu-id="d67e0-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d67e0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d67e0-115">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d67e0-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d67e0-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d67e0-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d67e0-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d67e0-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d67e0-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d67e0-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d67e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67e0-119">-DefaultProfile</span></span>
<span data-ttu-id="d67e0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d67e0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67e0-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-121">-JobSchedule</span></span>
<span data-ttu-id="d67e0-122">Gibt ein **PSCloudJobSchedule** -Objekt an, das einen Auftragszeitplan darstellt.</span><span class="sxs-lookup"><span data-stu-id="d67e0-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="d67e0-123">Verwenden Sie das Get-AzBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d67e0-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="d67e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67e0-124">CommonParameters</span></span>
<span data-ttu-id="d67e0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67e0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67e0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d67e0-127">INPUTS</span></span>

### <span data-ttu-id="d67e0-128">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="d67e0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d67e0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d67e0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d67e0-130">OUTPUTS</span></span>

### <span data-ttu-id="d67e0-131">System. void</span><span class="sxs-lookup"><span data-stu-id="d67e0-131">System.Void</span></span>

## <span data-ttu-id="d67e0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d67e0-132">NOTES</span></span>

## <span data-ttu-id="d67e0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d67e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="d67e0-134">Deaktivieren-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="d67e0-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="d67e0-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d67e0-137">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="d67e0-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="d67e0-139">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d67e0-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


