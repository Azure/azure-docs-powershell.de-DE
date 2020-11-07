---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662328"
---
# <span data-ttu-id="5b5b0-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="5b5b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5b0-103">Aktualisiert die Eigenschaften eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b5b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b5b0-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b5b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="5b5b0-106">Das Cmdlet " **Satz-AzureBatchTask** " aktualisiert die Eigenschaften einer Aufgabe im Azure-Batch Dienst.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="5b5b0-107">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="5b5b0-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="5b5b0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b5b0-109">EXAMPLES</span></span>

### <span data-ttu-id="5b5b0-110">Beispiel 1: Aktualisieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b5b0-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="5b5b0-111">Der erste Befehl ruft eine Aufgabe mithilfe von **Get-AzureBatchTask** ab und speichert Sie dann in der $Task-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="5b5b0-112">Mit den nächsten beiden Befehlen werden die Einschränkungen der Aufgabe in $Task geändert.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="5b5b0-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Task entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="5b5b0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b5b0-114">PARAMETERS</span></span>

### <span data-ttu-id="5b5b0-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5b5b0-115">-BatchContext</span></span>
<span data-ttu-id="5b5b0-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5b5b0-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5b5b0-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5b5b0-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5b5b0-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5b5b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5b0-121">-DefaultProfile</span></span>
<span data-ttu-id="5b5b0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5b0-123">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b5b0-123">-Task</span></span>
<span data-ttu-id="5b5b0-124">Gibt den **PSCloudTask** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5b0-125">CommonParameters</span></span>
<span data-ttu-id="5b5b0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5b0-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b5b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5b0-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b5b0-128">INPUTS</span></span>

### <span data-ttu-id="5b5b0-129">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="5b5b0-130">Parameter: Aufgabe (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b5b0-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="5b5b0-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5b5b0-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5b5b0-132">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b5b0-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5b5b0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b5b0-133">OUTPUTS</span></span>

### <span data-ttu-id="5b5b0-134">System. void</span><span class="sxs-lookup"><span data-stu-id="5b5b0-134">System.Void</span></span>

## <span data-ttu-id="5b5b0-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b5b0-135">NOTES</span></span>

## <span data-ttu-id="5b5b0-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b5b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="5b5b0-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="5b5b0-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5b5b0-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5b5b0-139">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="5b5b0-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="5b5b0-141">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b5b0-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="5b5b0-142">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5b5b0-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


