---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301594"
---
# <span data-ttu-id="31737-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="31737-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="31737-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31737-102">SYNOPSIS</span></span>
<span data-ttu-id="31737-103">Löscht den angegebenen Batch Pool.</span><span class="sxs-lookup"><span data-stu-id="31737-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="31737-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31737-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31737-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31737-105">DESCRIPTION</span></span>
<span data-ttu-id="31737-106">Das Cmdlet **Remove-AzBatchPool** löscht den angegebenen Azure Batch-Pool.</span><span class="sxs-lookup"><span data-stu-id="31737-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="31737-107">Sie werden zur Bestätigung aufgefordert, es sei denn, Sie verwenden den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="31737-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="31737-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31737-108">EXAMPLES</span></span>

### <span data-ttu-id="31737-109">Beispiel 1: Löschen eines Batch Pools nach Pool-ID</span><span class="sxs-lookup"><span data-stu-id="31737-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="31737-110">Dieser Befehl löscht den Pool mit der ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="31737-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="31737-111">Der Benutzer wird zur Bestätigung aufgefordert, bevor der Löschvorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31737-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="31737-112">Beispiel 2: Löschen aller Batch Pools mit Gewalt</span><span class="sxs-lookup"><span data-stu-id="31737-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="31737-113">Dieser Befehl löscht alle Batch-Pools.</span><span class="sxs-lookup"><span data-stu-id="31737-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="31737-114">Da der Parameter *Force* vorhanden ist, wird die Bestätigungsaufforderung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="31737-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="31737-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="31737-115">PARAMETERS</span></span>

### <span data-ttu-id="31737-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="31737-116">-BatchContext</span></span>
<span data-ttu-id="31737-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="31737-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="31737-118">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="31737-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="31737-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31737-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="31737-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="31737-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="31737-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="31737-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="31737-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31737-122">-DefaultProfile</span></span>
<span data-ttu-id="31737-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31737-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31737-124">-Force</span><span class="sxs-lookup"><span data-stu-id="31737-124">-Force</span></span>
<span data-ttu-id="31737-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="31737-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31737-126">-ID</span><span class="sxs-lookup"><span data-stu-id="31737-126">-Id</span></span>
<span data-ttu-id="31737-127">Gibt die ID des zu löschenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="31737-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="31737-128">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="31737-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31737-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31737-129">-Confirm</span></span>
<span data-ttu-id="31737-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31737-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31737-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31737-131">-WhatIf</span></span>
<span data-ttu-id="31737-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31737-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31737-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31737-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31737-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31737-134">CommonParameters</span></span>
<span data-ttu-id="31737-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31737-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31737-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31737-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31737-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31737-137">INPUTS</span></span>

### <span data-ttu-id="31737-138">System. String</span><span class="sxs-lookup"><span data-stu-id="31737-138">System.String</span></span>

### <span data-ttu-id="31737-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="31737-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="31737-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31737-140">OUTPUTS</span></span>

### <span data-ttu-id="31737-141">System. void</span><span class="sxs-lookup"><span data-stu-id="31737-141">System.Void</span></span>

## <span data-ttu-id="31737-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="31737-142">NOTES</span></span>

## <span data-ttu-id="31737-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31737-143">RELATED LINKS</span></span>

[<span data-ttu-id="31737-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="31737-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="31737-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="31737-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="31737-146">Neu – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="31737-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="31737-147">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31737-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
