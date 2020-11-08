---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997131"
---
# <span data-ttu-id="2ec99-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="2ec99-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="2ec99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ec99-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec99-103">Löscht eine Knoten Datei für einen Vorgang oder einen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="2ec99-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="2ec99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ec99-104">SYNTAX</span></span>

### <span data-ttu-id="2ec99-105">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2ec99-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec99-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2ec99-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec99-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec99-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec99-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ec99-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec99-109">Das Cmdlet **Remove-AzBatchNodeFile** löscht eine Azure-Batch-Knoten Datei für einen Task-oder Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="2ec99-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="2ec99-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ec99-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec99-111">Beispiel 1: Löschen einer Datei, die einem Vorgang zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="2ec99-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="2ec99-112">Dieser Befehl löscht die Knoten Datei mit dem Namen wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="2ec99-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="2ec99-113">Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2ec99-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="2ec99-114">Beispiel 2: Löschen einer Datei aus einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="2ec99-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="2ec99-115">Dieser Befehl löscht die Knoten Datei mit dem Namen startup\testFile.txt aus dem angegebenen Compute-Knoten im Pool mit der ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="2ec99-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="2ec99-116">Beispiel 3: Entfernen einer Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2ec99-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="2ec99-117">Dieser Befehl ruft die Knoten Datei mithilfe von **Get-AzBatchNodeFile** ab.</span><span class="sxs-lookup"><span data-stu-id="2ec99-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="2ec99-118">Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2ec99-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="2ec99-119">Der Befehl übergibt diese Datei mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec99-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="2ec99-120">Das aktuelle Cmdlet entfernt die Knoten Datei.</span><span class="sxs-lookup"><span data-stu-id="2ec99-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="2ec99-121">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="2ec99-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2ec99-122">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2ec99-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2ec99-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ec99-123">PARAMETERS</span></span>

### <span data-ttu-id="2ec99-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="2ec99-124">-BatchContext</span></span>
<span data-ttu-id="2ec99-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ec99-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2ec99-126">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ec99-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2ec99-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2ec99-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2ec99-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ec99-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2ec99-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="2ec99-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2ec99-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="2ec99-130">-ComputeNodeId</span></span>
<span data-ttu-id="2ec99-131">Gibt die ID des Compute-Knotens an, der die vom Cmdlet gelöschte Batch-Knoten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="2ec99-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2ec99-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec99-132">-DefaultProfile</span></span>
<span data-ttu-id="2ec99-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ec99-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec99-134">-Force</span><span class="sxs-lookup"><span data-stu-id="2ec99-134">-Force</span></span>
<span data-ttu-id="2ec99-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2ec99-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ec99-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ec99-136">-InputObject</span></span>
<span data-ttu-id="2ec99-137">Gibt das **PSNodeFile** -Objekt an, das die vom Cmdlet gelöschte Knoten Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ec99-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="2ec99-138">Verwenden Sie zum Abrufen eines **PSNodeFile** das Get-AzBatchNodeFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec99-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="2ec99-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="2ec99-139">-JobId</span></span>
<span data-ttu-id="2ec99-140">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="2ec99-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2ec99-141">-Path</span><span class="sxs-lookup"><span data-stu-id="2ec99-141">-Path</span></span>
<span data-ttu-id="2ec99-142">Der Dateipfad der zu löschenden Knoten Datei.</span><span class="sxs-lookup"><span data-stu-id="2ec99-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="2ec99-143">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="2ec99-143">-PoolId</span></span>
<span data-ttu-id="2ec99-144">Gibt die ID des Pools an, der die Compute-Knoten enthält, für die dieses Cmdlet eine Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ec99-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="2ec99-145">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="2ec99-145">-Recursive</span></span>
<span data-ttu-id="2ec99-146">Gibt an, dass dieses Cmdlet den Ordner und alle Unterordner und Dateien unterhalb des angegebenen Pfads löscht.</span><span class="sxs-lookup"><span data-stu-id="2ec99-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="2ec99-147">Dieses Cmdlet ist nur relevant, wenn es sich bei dem Pfad um einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="2ec99-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="2ec99-148">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="2ec99-148">-TaskId</span></span>
<span data-ttu-id="2ec99-149">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2ec99-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="2ec99-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ec99-150">-Confirm</span></span>
<span data-ttu-id="2ec99-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ec99-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec99-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec99-152">-WhatIf</span></span>
<span data-ttu-id="2ec99-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec99-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec99-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ec99-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec99-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec99-155">CommonParameters</span></span>
<span data-ttu-id="2ec99-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec99-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec99-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ec99-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec99-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ec99-158">INPUTS</span></span>

### <span data-ttu-id="2ec99-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec99-159">System.String</span></span>

### <span data-ttu-id="2ec99-160">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="2ec99-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="2ec99-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ec99-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ec99-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ec99-162">OUTPUTS</span></span>

### <span data-ttu-id="2ec99-163">System. void</span><span class="sxs-lookup"><span data-stu-id="2ec99-163">System.Void</span></span>

## <span data-ttu-id="2ec99-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ec99-164">NOTES</span></span>

## <span data-ttu-id="2ec99-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ec99-165">RELATED LINKS</span></span>

[<span data-ttu-id="2ec99-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2ec99-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2ec99-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="2ec99-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="2ec99-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="2ec99-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


