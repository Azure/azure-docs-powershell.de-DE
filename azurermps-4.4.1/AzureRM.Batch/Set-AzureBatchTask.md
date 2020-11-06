---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503257"
---
# <span data-ttu-id="bfb81-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="bfb81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfb81-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb81-103">Aktualisiert die Eigenschaften eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bfb81-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfb81-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb81-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb81-106">Das Cmdlet " **Satz-AzureBatchTask** " aktualisiert die Eigenschaften einer Aufgabe im Azure-Batch Dienst.</span><span class="sxs-lookup"><span data-stu-id="bfb81-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="bfb81-107">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bfb81-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="bfb81-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="bfb81-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="bfb81-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfb81-109">EXAMPLES</span></span>

### <span data-ttu-id="bfb81-110">Beispiel 1: Aktualisieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bfb81-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="bfb81-111">Der erste Befehl ruft eine Aufgabe mithilfe von **Get-AzureBatchTask** ab und speichert Sie dann in der $Task-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bfb81-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="bfb81-112">Mit den nächsten beiden Befehlen werden die Einschränkungen der Aufgabe in $Task geändert.</span><span class="sxs-lookup"><span data-stu-id="bfb81-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="bfb81-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Task entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfb81-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="bfb81-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfb81-114">PARAMETERS</span></span>

### <span data-ttu-id="bfb81-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="bfb81-115">-BatchContext</span></span>
<span data-ttu-id="bfb81-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfb81-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bfb81-117">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb81-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bfb81-118">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bfb81-118">-Task</span></span>
<span data-ttu-id="bfb81-119">Gibt den **PSCloudTask** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bfb81-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="bfb81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb81-120">-DefaultProfile</span></span>
<span data-ttu-id="bfb81-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfb81-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb81-122">CommonParameters</span></span>
<span data-ttu-id="bfb81-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb81-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb81-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb81-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfb81-125">INPUTS</span></span>

### <span data-ttu-id="bfb81-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bfb81-126">BatchAccountContext</span></span>
<span data-ttu-id="bfb81-127">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfb81-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bfb81-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-128">PSCloudTask</span></span>
<span data-ttu-id="bfb81-129">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfb81-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="bfb81-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfb81-130">OUTPUTS</span></span>

## <span data-ttu-id="bfb81-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfb81-131">NOTES</span></span>

## <span data-ttu-id="bfb81-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfb81-132">RELATED LINKS</span></span>

[<span data-ttu-id="bfb81-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="bfb81-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bfb81-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bfb81-135">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="bfb81-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="bfb81-137">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfb81-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="bfb81-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bfb81-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


