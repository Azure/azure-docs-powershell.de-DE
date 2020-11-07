---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: b49ab8a6a08802ec670fb605e707ae46c51ddab2
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662026"
---
# <span data-ttu-id="1dc2e-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="1dc2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc2e-103">Aktualisiert die Eigenschaften eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="1dc2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc2e-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc2e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dc2e-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc2e-106">Das Cmdlet " **Satz-AzBatchTask** " aktualisiert die Eigenschaften einer Aufgabe im Azure-Batch Dienst.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="1dc2e-107">Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="1dc2e-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1dc2e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dc2e-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc2e-110">Beispiel 1: Aktualisieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1dc2e-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="1dc2e-111">Der erste Befehl ruft eine Aufgabe mithilfe von **Get-AzBatchTask** ab und speichert Sie dann in der $Task-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="1dc2e-112">Mit den nächsten beiden Befehlen werden die Einschränkungen der Aufgabe in $Task geändert.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="1dc2e-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Task entspricht.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="1dc2e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dc2e-114">PARAMETERS</span></span>

### <span data-ttu-id="1dc2e-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="1dc2e-115">-BatchContext</span></span>
<span data-ttu-id="1dc2e-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1dc2e-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1dc2e-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1dc2e-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1dc2e-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1dc2e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc2e-121">-DefaultProfile</span></span>
<span data-ttu-id="1dc2e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc2e-123">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1dc2e-123">-Task</span></span>
<span data-ttu-id="1dc2e-124">Gibt den **PSCloudTask** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="1dc2e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc2e-125">CommonParameters</span></span>
<span data-ttu-id="1dc2e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc2e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc2e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc2e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc2e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dc2e-128">INPUTS</span></span>

### <span data-ttu-id="1dc2e-129">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="1dc2e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1dc2e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1dc2e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dc2e-131">OUTPUTS</span></span>

### <span data-ttu-id="1dc2e-132">System. void</span><span class="sxs-lookup"><span data-stu-id="1dc2e-132">System.Void</span></span>

## <span data-ttu-id="1dc2e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dc2e-133">NOTES</span></span>

## <span data-ttu-id="1dc2e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dc2e-134">RELATED LINKS</span></span>

[<span data-ttu-id="1dc2e-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="1dc2e-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1dc2e-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1dc2e-137">Neu – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="1dc2e-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="1dc2e-139">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1dc2e-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="1dc2e-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1dc2e-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


