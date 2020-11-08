---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5ff22b437ab209891495bb7778eca7d5c86ac1da
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007414"
---
# <span data-ttu-id="cea0b-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cea0b-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="cea0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cea0b-102">SYNOPSIS</span></span>
<span data-ttu-id="cea0b-103">Löscht ein Benutzerkonto aus einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="cea0b-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="cea0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cea0b-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cea0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cea0b-105">DESCRIPTION</span></span>
<span data-ttu-id="cea0b-106">Das Cmdlet **Remove-AzBatchComputeNodeUser** löscht ein Benutzerkonto aus einem Azure-Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="cea0b-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="cea0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cea0b-107">EXAMPLES</span></span>

### <span data-ttu-id="cea0b-108">Beispiel 1: Löschen eines Benutzers aus einem Compute-Knoten ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="cea0b-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="cea0b-109">Mit diesem Befehl wird der Benutzernamens "User14" aus dem Compute-Knoten namens "ComputeNode01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cea0b-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="cea0b-110">Der Compute-Knoten befindet sich im Pool mit dem Namen Pool01.</span><span class="sxs-lookup"><span data-stu-id="cea0b-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="cea0b-111">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="cea0b-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cea0b-112">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="cea0b-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cea0b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea0b-113">PARAMETERS</span></span>

### <span data-ttu-id="cea0b-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cea0b-114">-BatchContext</span></span>
<span data-ttu-id="cea0b-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea0b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cea0b-116">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea0b-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cea0b-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cea0b-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cea0b-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea0b-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cea0b-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cea0b-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cea0b-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="cea0b-120">-ComputeNodeId</span></span>
<span data-ttu-id="cea0b-121">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet das Benutzerkonto löscht.</span><span class="sxs-lookup"><span data-stu-id="cea0b-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea0b-122">-DefaultProfile</span></span>
<span data-ttu-id="cea0b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cea0b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea0b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cea0b-124">-Name</span></span>
<span data-ttu-id="cea0b-125">Gibt den Namen des zu löschenden Benutzerkontos an.</span><span class="sxs-lookup"><span data-stu-id="cea0b-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="cea0b-126">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="cea0b-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea0b-127">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="cea0b-127">-PoolId</span></span>
<span data-ttu-id="cea0b-128">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cea0b-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="cea0b-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cea0b-129">-Confirm</span></span>
<span data-ttu-id="cea0b-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cea0b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea0b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea0b-131">-WhatIf</span></span>
<span data-ttu-id="cea0b-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea0b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea0b-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cea0b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea0b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea0b-134">CommonParameters</span></span>
<span data-ttu-id="cea0b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea0b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea0b-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cea0b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea0b-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cea0b-137">INPUTS</span></span>

### <span data-ttu-id="cea0b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cea0b-138">System.String</span></span>

### <span data-ttu-id="cea0b-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cea0b-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cea0b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cea0b-140">OUTPUTS</span></span>

### <span data-ttu-id="cea0b-141">System. void</span><span class="sxs-lookup"><span data-stu-id="cea0b-141">System.Void</span></span>

## <span data-ttu-id="cea0b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cea0b-142">NOTES</span></span>

## <span data-ttu-id="cea0b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cea0b-143">RELATED LINKS</span></span>

[<span data-ttu-id="cea0b-144">Neu – AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cea0b-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="cea0b-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cea0b-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cea0b-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cea0b-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


