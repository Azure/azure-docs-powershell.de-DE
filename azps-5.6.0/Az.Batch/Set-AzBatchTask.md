---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939704"
---
# <span data-ttu-id="2e4d6-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="2e4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4d6-103">Aktualisiert die Eigenschaften einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="2e4d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e4d6-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e4d6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4d6-106">Das **Cmdlet Set-AzBatchTask** aktualisiert die Eigenschaften einer Aufgabe im Azure Batch-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="2e4d6-107">Verwenden Sie Get-AzBatchTask-Cmdlet, um ein **PSCloudTask-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="2e4d6-108">Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2e4d6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e4d6-109">EXAMPLES</span></span>

### <span data-ttu-id="2e4d6-110">Beispiel 1: Aktualisieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2e4d6-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="2e4d6-111">Der erste Befehl ruft eine Aufgabe mithilfe von **Get-AzBatchTask ab** und speichert sie dann in der $Task Variablen.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="2e4d6-112">Die nächsten beiden Befehle ändern die Einschränkungen der Aufgabe in $Task.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="2e4d6-113">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in $Task.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="2e4d6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2e4d6-114">PARAMETERS</span></span>

### <span data-ttu-id="2e4d6-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2e4d6-115">-BatchContext</span></span>
<span data-ttu-id="2e4d6-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2e4d6-117">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2e4d6-118">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2e4d6-119">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2e4d6-120">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2e4d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4d6-121">-DefaultProfile</span></span>
<span data-ttu-id="2e4d6-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e4d6-123">-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2e4d6-123">-Task</span></span>
<span data-ttu-id="2e4d6-124">Gibt den **PSCloudTask an, für** den dieses Cmdlet den Batchdienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="2e4d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4d6-125">CommonParameters</span></span>
<span data-ttu-id="2e4d6-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4d6-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e4d6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4d6-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e4d6-128">INPUTS</span></span>

### <span data-ttu-id="2e4d6-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="2e4d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2e4d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2e4d6-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e4d6-131">OUTPUTS</span></span>

### <span data-ttu-id="2e4d6-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="2e4d6-132">System.Void</span></span>

## <span data-ttu-id="2e4d6-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2e4d6-133">NOTES</span></span>

## <span data-ttu-id="2e4d6-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2e4d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e4d6-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="2e4d6-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2e4d6-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2e4d6-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="2e4d6-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="2e4d6-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2e4d6-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="2e4d6-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2e4d6-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
