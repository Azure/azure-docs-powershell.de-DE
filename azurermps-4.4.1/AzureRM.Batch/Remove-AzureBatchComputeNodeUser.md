---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501945"
---
# <span data-ttu-id="b8c82-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b8c82-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="b8c82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8c82-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c82-103">Löscht ein Benutzerkonto aus einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="b8c82-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8c82-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8c82-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c82-106">Das Cmdlet **Remove-AzureBatchComputeNodeUser** löscht ein Benutzerkonto aus einem Azure-Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="b8c82-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="b8c82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8c82-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c82-108">Beispiel 1: Löschen eines Benutzers aus einem Compute-Knoten ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="b8c82-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="b8c82-109">Mit diesem Befehl wird der Benutzernamens "User14" aus dem Compute-Knoten namens "ComputeNode01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8c82-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="b8c82-110">Der Compute-Knoten befindet sich im Pool mit dem Namen Pool01.</span><span class="sxs-lookup"><span data-stu-id="b8c82-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="b8c82-111">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8c82-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b8c82-112">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b8c82-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b8c82-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8c82-113">PARAMETERS</span></span>

### <span data-ttu-id="b8c82-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b8c82-114">-BatchContext</span></span>
<span data-ttu-id="b8c82-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8c82-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8c82-116">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c82-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b8c82-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="b8c82-117">-ComputeNodeId</span></span>
<span data-ttu-id="b8c82-118">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet das Benutzerkonto löscht.</span><span class="sxs-lookup"><span data-stu-id="b8c82-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="b8c82-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c82-119">-Name</span></span>
<span data-ttu-id="b8c82-120">Gibt den Namen des zu löschenden Benutzerkontos an.</span><span class="sxs-lookup"><span data-stu-id="b8c82-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="b8c82-121">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="b8c82-121">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b8c82-122">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="b8c82-122">-PoolId</span></span>
<span data-ttu-id="b8c82-123">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8c82-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="b8c82-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8c82-124">-Confirm</span></span>
<span data-ttu-id="b8c82-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8c82-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c82-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c82-126">-WhatIf</span></span>
<span data-ttu-id="b8c82-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8c82-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c82-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8c82-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c82-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c82-129">-DefaultProfile</span></span>
<span data-ttu-id="b8c82-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8c82-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c82-131">CommonParameters</span></span>
<span data-ttu-id="b8c82-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c82-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c82-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c82-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8c82-134">INPUTS</span></span>

### <span data-ttu-id="b8c82-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8c82-135">BatchAccountContext</span></span>
<span data-ttu-id="b8c82-136">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8c82-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b8c82-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8c82-137">OUTPUTS</span></span>

## <span data-ttu-id="b8c82-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8c82-138">NOTES</span></span>

## <span data-ttu-id="b8c82-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8c82-139">RELATED LINKS</span></span>

[<span data-ttu-id="b8c82-140">Neu – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b8c82-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b8c82-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b8c82-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b8c82-142">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b8c82-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


