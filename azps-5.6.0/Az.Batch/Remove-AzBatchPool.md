---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 6dd5082485d8028a0f1593db9c84bdc571b8c6bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943139"
---
# <span data-ttu-id="d4b5a-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d4b5a-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="d4b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b5a-103">Löscht den angegebenen Batchpool.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="d4b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4b5a-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b5a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d4b5a-106">Das **Cmdlet Remove-AzBatchPool** löscht den angegebenen Azure Batch-Pool.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="d4b5a-107">Sie werden zur Bestätigung aufgefordert, es sei denn, Sie verwenden den *Parameter Erzwingen.*</span><span class="sxs-lookup"><span data-stu-id="d4b5a-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="d4b5a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4b5a-108">EXAMPLES</span></span>

### <span data-ttu-id="d4b5a-109">Beispiel 1: Löschen eines Batchpools nach Pool-ID</span><span class="sxs-lookup"><span data-stu-id="d4b5a-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="d4b5a-110">Mit diesem Befehl wird der Pool mit DER ID MyPool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="d4b5a-111">Der Benutzer wird zur Bestätigung aufgefordert, bevor der Löschvorgang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="d4b5a-112">Beispiel 2: Löschen aller Batchpools mit Gewalt</span><span class="sxs-lookup"><span data-stu-id="d4b5a-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="d4b5a-113">Mit diesem Befehl werden alle Batchpools gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="d4b5a-114">Da der *Parameter Kraft* vorhanden ist, wird die Bestätigungsaufforderung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="d4b5a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4b5a-115">PARAMETERS</span></span>

### <span data-ttu-id="d4b5a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4b5a-116">-BatchContext</span></span>
<span data-ttu-id="d4b5a-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4b5a-118">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d4b5a-119">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d4b5a-120">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d4b5a-121">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d4b5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b5a-122">-DefaultProfile</span></span>
<span data-ttu-id="d4b5a-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b5a-124">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d4b5a-124">-Force</span></span>
<span data-ttu-id="d4b5a-125">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4b5a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d4b5a-126">-Id</span></span>
<span data-ttu-id="d4b5a-127">Gibt die ID des zu löschenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="d4b5a-128">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d4b5a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4b5a-129">-Confirm</span></span>
<span data-ttu-id="d4b5a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b5a-131">-WhatIf</span></span>
<span data-ttu-id="d4b5a-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b5a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b5a-134">CommonParameters</span></span>
<span data-ttu-id="d4b5a-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b5a-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4b5a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b5a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4b5a-137">INPUTS</span></span>

### <span data-ttu-id="d4b5a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d4b5a-138">System.String</span></span>

### <span data-ttu-id="d4b5a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4b5a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d4b5a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4b5a-140">OUTPUTS</span></span>

### <span data-ttu-id="d4b5a-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="d4b5a-141">System.Void</span></span>

## <span data-ttu-id="d4b5a-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4b5a-142">NOTES</span></span>

## <span data-ttu-id="d4b5a-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4b5a-143">RELATED LINKS</span></span>

[<span data-ttu-id="d4b5a-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d4b5a-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d4b5a-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d4b5a-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d4b5a-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d4b5a-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="d4b5a-147">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4b5a-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
