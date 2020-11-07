---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664241"
---
# <span data-ttu-id="141fe-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="141fe-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="141fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="141fe-102">SYNOPSIS</span></span>
<span data-ttu-id="141fe-103">Löscht ein Benutzerkonto aus einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="141fe-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="141fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="141fe-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="141fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="141fe-105">DESCRIPTION</span></span>
<span data-ttu-id="141fe-106">Das Cmdlet **Remove-AzureBatchComputeNodeUser** löscht ein Benutzerkonto aus einem Azure-Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="141fe-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="141fe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="141fe-107">EXAMPLES</span></span>

### <span data-ttu-id="141fe-108">Beispiel 1: Löschen eines Benutzers aus einem Compute-Knoten ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="141fe-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="141fe-109">Mit diesem Befehl wird der Benutzernamens "User14" aus dem Compute-Knoten namens "ComputeNode01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="141fe-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="141fe-110">Der Compute-Knoten befindet sich im Pool mit dem Namen Pool01.</span><span class="sxs-lookup"><span data-stu-id="141fe-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="141fe-111">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="141fe-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="141fe-112">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="141fe-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="141fe-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="141fe-113">PARAMETERS</span></span>

### <span data-ttu-id="141fe-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="141fe-114">-BatchContext</span></span>
<span data-ttu-id="141fe-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="141fe-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="141fe-116">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="141fe-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="141fe-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="141fe-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="141fe-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="141fe-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="141fe-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="141fe-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="141fe-120">-ComputeNodeId</span></span>
<span data-ttu-id="141fe-121">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet das Benutzerkonto löscht.</span><span class="sxs-lookup"><span data-stu-id="141fe-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141fe-122">-DefaultProfile</span></span>
<span data-ttu-id="141fe-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="141fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-124">-Name</span><span class="sxs-lookup"><span data-stu-id="141fe-124">-Name</span></span>
<span data-ttu-id="141fe-125">Gibt den Namen des zu löschenden Benutzerkontos an.</span><span class="sxs-lookup"><span data-stu-id="141fe-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="141fe-126">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="141fe-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-127">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="141fe-127">-PoolId</span></span>
<span data-ttu-id="141fe-128">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="141fe-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="141fe-129">-Confirm</span></span>
<span data-ttu-id="141fe-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="141fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141fe-131">-WhatIf</span></span>
<span data-ttu-id="141fe-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="141fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141fe-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="141fe-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141fe-134">CommonParameters</span></span>
<span data-ttu-id="141fe-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141fe-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141fe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141fe-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="141fe-137">INPUTS</span></span>

### <span data-ttu-id="141fe-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="141fe-138">BatchAccountContext</span></span>
<span data-ttu-id="141fe-139">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="141fe-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="141fe-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="141fe-140">OUTPUTS</span></span>

## <span data-ttu-id="141fe-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="141fe-141">NOTES</span></span>

## <span data-ttu-id="141fe-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="141fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="141fe-143">Neu – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="141fe-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="141fe-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="141fe-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="141fe-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="141fe-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


