---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662693"
---
# <span data-ttu-id="6e913-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="6e913-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="6e913-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e913-102">SYNOPSIS</span></span>
<span data-ttu-id="6e913-103">Löscht eine Knoten Datei für einen Vorgang oder einen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="6e913-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e913-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e913-104">SYNTAX</span></span>

### <span data-ttu-id="6e913-105">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6e913-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e913-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="6e913-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e913-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e913-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e913-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e913-108">DESCRIPTION</span></span>
<span data-ttu-id="6e913-109">Das Cmdlet **Remove-AzureBatchNodeFile** löscht eine Azure-Batch-Knoten Datei für einen Task-oder Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="6e913-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="6e913-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e913-110">EXAMPLES</span></span>

### <span data-ttu-id="6e913-111">Beispiel 1: Löschen einer Datei Extent mit einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6e913-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="6e913-112">Dieser Befehl löscht die Knoten Datei mit dem Namen wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6e913-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="6e913-113">Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="6e913-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="6e913-114">Beispiel 2: Löschen einer Datei aus einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="6e913-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="6e913-115">Dieser Befehl löscht die Knoten Datei mit dem Namen startup\testFile.txt aus dem angegebenen Compute-Knoten im Pool mit der ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="6e913-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="6e913-116">Beispiel 3: Entfernen einer Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="6e913-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="6e913-117">Dieser Befehl ruft die Knoten Datei mithilfe von **Get-AzureBatchNodeFile** ab.</span><span class="sxs-lookup"><span data-stu-id="6e913-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="6e913-118">Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="6e913-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="6e913-119">Der Befehl übergibt diese Datei mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e913-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="6e913-120">Das aktuelle Cmdlet entfernt die Knoten Datei.</span><span class="sxs-lookup"><span data-stu-id="6e913-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="6e913-121">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="6e913-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6e913-122">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6e913-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e913-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e913-123">PARAMETERS</span></span>

### <span data-ttu-id="6e913-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6e913-124">-BatchContext</span></span>
<span data-ttu-id="6e913-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e913-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e913-126">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e913-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e913-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e913-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e913-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e913-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e913-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e913-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6e913-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="6e913-130">-ComputeNodeId</span></span>
<span data-ttu-id="6e913-131">Gibt die ID des Compute-Knotens an, der die vom Cmdlet gelöschte Batch-Knoten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="6e913-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e913-132">-DefaultProfile</span></span>
<span data-ttu-id="6e913-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e913-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e913-134">-Force</span><span class="sxs-lookup"><span data-stu-id="6e913-134">-Force</span></span>
<span data-ttu-id="6e913-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6e913-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e913-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e913-136">-InputObject</span></span>
<span data-ttu-id="6e913-137">Gibt das **PSNodeFile** -Objekt an, das die vom Cmdlet gelöschte Knoten Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e913-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="6e913-138">Verwenden Sie zum Abrufen eines **PSNodeFile** das Get-AzureBatchNodeFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e913-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="6e913-139">-JobId</span></span>
<span data-ttu-id="6e913-140">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="6e913-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-141">-Path</span><span class="sxs-lookup"><span data-stu-id="6e913-141">-Path</span></span>
<span data-ttu-id="6e913-142">Der Dateipfad der zu löschenden Knoten Datei.</span><span class="sxs-lookup"><span data-stu-id="6e913-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-143">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="6e913-143">-PoolId</span></span>
<span data-ttu-id="6e913-144">Gibt die ID des Pools an, der die Compute-Knoten enthält, für die dieses Cmdlet eine Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="6e913-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-145">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="6e913-145">-Recursive</span></span>
<span data-ttu-id="6e913-146">Gibt an, dass dieses Cmdlet den Ordner und alle Unterordner und Dateien unterhalb des angegebenen Pfads löscht.</span><span class="sxs-lookup"><span data-stu-id="6e913-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="6e913-147">Dieses Cmdlet ist nur relevant, wenn es sich bei dem Pfad um einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="6e913-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="6e913-148">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="6e913-148">-TaskId</span></span>
<span data-ttu-id="6e913-149">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="6e913-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e913-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e913-150">-Confirm</span></span>
<span data-ttu-id="6e913-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e913-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e913-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e913-152">-WhatIf</span></span>
<span data-ttu-id="6e913-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e913-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e913-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e913-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e913-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e913-155">CommonParameters</span></span>
<span data-ttu-id="6e913-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e913-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e913-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e913-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e913-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e913-158">INPUTS</span></span>

### <span data-ttu-id="6e913-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6e913-159">System.String</span></span>

### <span data-ttu-id="6e913-160">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="6e913-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="6e913-161">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e913-161">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6e913-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e913-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6e913-163">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e913-163">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6e913-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e913-164">OUTPUTS</span></span>

### <span data-ttu-id="6e913-165">System. void</span><span class="sxs-lookup"><span data-stu-id="6e913-165">System.Void</span></span>

## <span data-ttu-id="6e913-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e913-166">NOTES</span></span>

## <span data-ttu-id="6e913-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e913-167">RELATED LINKS</span></span>

[<span data-ttu-id="6e913-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e913-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6e913-169">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="6e913-169">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="6e913-170">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="6e913-170">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


