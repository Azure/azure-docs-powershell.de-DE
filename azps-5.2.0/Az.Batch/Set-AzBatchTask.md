---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299840"
---
# <span data-ttu-id="57a8a-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="57a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="57a8a-103">Aktualisiert die Eigenschaften einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="57a8a-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="57a8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57a8a-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57a8a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="57a8a-106">Das **Cmdlet "Set-AzBatchTask"** aktualisiert die Eigenschaften einer Aufgabe im Azure Batch-Dienst.</span><span class="sxs-lookup"><span data-stu-id="57a8a-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="57a8a-107">Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **"PSCloudTask"-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="57a8a-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="57a8a-108">Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.</span><span class="sxs-lookup"><span data-stu-id="57a8a-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="57a8a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="57a8a-110">Beispiel 1: Aktualisieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="57a8a-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="57a8a-111">Der erste Befehl ruft eine Aufgabe mithilfe von **"Get-AzBatchTask"** ab und speichert sie dann in der $Task Variable.</span><span class="sxs-lookup"><span data-stu-id="57a8a-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="57a8a-112">Mit den nächsten beiden Befehlen werden die Einschränkungen des Vorgangs in $Task.</span><span class="sxs-lookup"><span data-stu-id="57a8a-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="57a8a-113">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in der $Task.</span><span class="sxs-lookup"><span data-stu-id="57a8a-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="57a8a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57a8a-114">PARAMETERS</span></span>

### <span data-ttu-id="57a8a-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="57a8a-115">-BatchContext</span></span>
<span data-ttu-id="57a8a-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57a8a-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="57a8a-117">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="57a8a-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="57a8a-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57a8a-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="57a8a-119">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="57a8a-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="57a8a-120">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57a8a-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="57a8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a8a-121">-DefaultProfile</span></span>
<span data-ttu-id="57a8a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57a8a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57a8a-123">-Task</span><span class="sxs-lookup"><span data-stu-id="57a8a-123">-Task</span></span>
<span data-ttu-id="57a8a-124">Gibt den **PSCloudTask** an, für den dieses Cmdlet den Batchdienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="57a8a-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="57a8a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a8a-125">CommonParameters</span></span>
<span data-ttu-id="57a8a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a8a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a8a-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57a8a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a8a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57a8a-128">INPUTS</span></span>

### <span data-ttu-id="57a8a-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="57a8a-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="57a8a-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="57a8a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57a8a-131">OUTPUTS</span></span>

### <span data-ttu-id="57a8a-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="57a8a-132">System.Void</span></span>

## <span data-ttu-id="57a8a-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57a8a-133">NOTES</span></span>

## <span data-ttu-id="57a8a-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57a8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="57a8a-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="57a8a-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="57a8a-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="57a8a-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="57a8a-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="57a8a-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57a8a-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="57a8a-140">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="57a8a-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
