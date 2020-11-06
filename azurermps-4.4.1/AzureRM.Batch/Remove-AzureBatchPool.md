---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497874"
---
# <span data-ttu-id="9ce8c-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9ce8c-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="9ce8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ce8c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce8c-103">Löscht den angegebenen Batch Pool.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce8c-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ce8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ce8c-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce8c-106">Das Cmdlet **Remove-AzureBatchPool** löscht den angegebenen Azure Batch-Pool.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="9ce8c-107">Sie werden zur Bestätigung aufgefordert, es sei denn, Sie verwenden den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="9ce8c-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="9ce8c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ce8c-108">EXAMPLES</span></span>

### <span data-ttu-id="9ce8c-109">Beispiel 1: Löschen eines Batch Pools nach Pool-ID</span><span class="sxs-lookup"><span data-stu-id="9ce8c-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="9ce8c-110">Dieser Befehl löscht den Pool mit der ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="9ce8c-111">Der Benutzer wird zur Bestätigung aufgefordert, bevor der Löschvorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="9ce8c-112">Beispiel 2: Löschen aller Batch Pools mit Gewalt</span><span class="sxs-lookup"><span data-stu-id="9ce8c-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="9ce8c-113">Dieser Befehl löscht alle Batch-Pools.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="9ce8c-114">Da der Parameter *Force* vorhanden ist, wird die Bestätigungsaufforderung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="9ce8c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ce8c-115">PARAMETERS</span></span>

### <span data-ttu-id="9ce8c-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="9ce8c-116">-BatchContext</span></span>
<span data-ttu-id="9ce8c-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9ce8c-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9ce8c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9ce8c-119">-Force</span></span>
<span data-ttu-id="9ce8c-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ce8c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9ce8c-121">-Id</span></span>
<span data-ttu-id="9ce8c-122">Gibt die ID des zu löschenden Pools an.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="9ce8c-123">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="9ce8c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ce8c-124">-Confirm</span></span>
<span data-ttu-id="9ce8c-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce8c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce8c-126">-WhatIf</span></span>
<span data-ttu-id="9ce8c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce8c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce8c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce8c-129">-DefaultProfile</span></span>
<span data-ttu-id="9ce8c-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ce8c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce8c-131">CommonParameters</span></span>
<span data-ttu-id="9ce8c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce8c-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce8c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce8c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ce8c-134">INPUTS</span></span>

### <span data-ttu-id="9ce8c-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9ce8c-135">BatchAccountContext</span></span>
<span data-ttu-id="9ce8c-136">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ce8c-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9ce8c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ce8c-137">OUTPUTS</span></span>

## <span data-ttu-id="9ce8c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ce8c-138">NOTES</span></span>

## <span data-ttu-id="9ce8c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ce8c-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ce8c-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9ce8c-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9ce8c-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9ce8c-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="9ce8c-142">Neu – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9ce8c-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="9ce8c-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9ce8c-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


