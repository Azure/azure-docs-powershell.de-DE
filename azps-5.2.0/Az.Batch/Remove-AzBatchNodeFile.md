---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301531"
---
# <span data-ttu-id="f26da-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f26da-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="f26da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26da-102">SYNOPSIS</span></span>
<span data-ttu-id="f26da-103">Löscht eine Knotendatei für eine Aufgabe oder einen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="f26da-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="f26da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f26da-104">SYNTAX</span></span>

### <span data-ttu-id="f26da-105">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f26da-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f26da-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f26da-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f26da-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f26da-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f26da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f26da-108">DESCRIPTION</span></span>
<span data-ttu-id="f26da-109">Das **Cmdlet "Remove-AzBatchNodeFile"** löscht eine Azure Batch-Knotendatei für eine Aufgabe oder einen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="f26da-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="f26da-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f26da-110">EXAMPLES</span></span>

### <span data-ttu-id="f26da-111">Beispiel 1: Löschen einer datei, die einer Aufgabe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="f26da-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="f26da-112">Mit diesem Befehl wird die Knotendatei mit dem Namen wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="f26da-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="f26da-113">Diese Datei ist der Aufgabe zugeordnet, die die ID Task26 unter dem Auftragsauftrag 0000001 enthält.</span><span class="sxs-lookup"><span data-stu-id="f26da-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="f26da-114">Beispiel 2: Löschen einer Datei aus einem Rechenknoten</span><span class="sxs-lookup"><span data-stu-id="f26da-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="f26da-115">Mit diesem Befehl wird die Knotendatei mit dem Namen "startup\testFile.txt" aus dem angegebenen Berechnungsknoten im Pool mit dem ID Pool07 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f26da-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="f26da-116">Beispiel 3: Entfernen einer Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f26da-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="f26da-117">Dieser Befehl ruft die Knotendatei mit **"Get-AzBatchNodeFile" ab.**</span><span class="sxs-lookup"><span data-stu-id="f26da-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="f26da-118">Diese Datei ist der Aufgabe zugeordnet, die die ID Task26 unter dem Auftragsauftrag 0000001 enthält.</span><span class="sxs-lookup"><span data-stu-id="f26da-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="f26da-119">Der Befehl übergibt diese Datei mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f26da-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="f26da-120">Das aktuelle Cmdlet entfernt die Knotendatei.</span><span class="sxs-lookup"><span data-stu-id="f26da-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="f26da-121">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="f26da-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f26da-122">Daher fordert Sie der Befehl nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="f26da-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f26da-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f26da-123">PARAMETERS</span></span>

### <span data-ttu-id="f26da-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f26da-124">-BatchContext</span></span>
<span data-ttu-id="f26da-125">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f26da-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f26da-126">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="f26da-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f26da-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f26da-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f26da-128">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f26da-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f26da-129">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f26da-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f26da-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f26da-130">-ComputeNodeId</span></span>
<span data-ttu-id="f26da-131">Gibt die ID des Computeknotens an, der die Vom Cmdlet gelöschte Batchknotendatei enthält.</span><span class="sxs-lookup"><span data-stu-id="f26da-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f26da-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26da-132">-DefaultProfile</span></span>
<span data-ttu-id="f26da-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f26da-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f26da-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f26da-134">-Force</span></span>
<span data-ttu-id="f26da-135">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="f26da-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f26da-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f26da-136">-InputObject</span></span>
<span data-ttu-id="f26da-137">Gibt das **PSNodeFile-Objekt** an, das die Knotendatei repräsentiert, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f26da-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="f26da-138">Verwenden Sie das **cmdlet "Get-AzBatchNodeFile",** um eine PSNodeFile zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f26da-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="f26da-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="f26da-139">-JobId</span></span>
<span data-ttu-id="f26da-140">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f26da-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="f26da-141">-Path</span><span class="sxs-lookup"><span data-stu-id="f26da-141">-Path</span></span>
<span data-ttu-id="f26da-142">Der Dateipfad der zu löschende Knotendatei.</span><span class="sxs-lookup"><span data-stu-id="f26da-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="f26da-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f26da-143">-PoolId</span></span>
<span data-ttu-id="f26da-144">Gibt die ID des Pools an, der die Rechenknoten enthält, für die dieses Cmdlet eine Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="f26da-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="f26da-145">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="f26da-145">-Recursive</span></span>
<span data-ttu-id="f26da-146">Gibt an, dass dieses Cmdlet den Ordner sowie alle Unterordner und Dateien unter dem angegebenen Pfad löscht.</span><span class="sxs-lookup"><span data-stu-id="f26da-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="f26da-147">Dieses Cmdlet ist nur relevant, wenn es sich bei dem Pfad um einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="f26da-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="f26da-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="f26da-148">-TaskId</span></span>
<span data-ttu-id="f26da-149">Gibt die ID des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="f26da-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="f26da-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f26da-150">-Confirm</span></span>
<span data-ttu-id="f26da-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f26da-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f26da-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f26da-152">-WhatIf</span></span>
<span data-ttu-id="f26da-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f26da-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f26da-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f26da-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f26da-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26da-155">CommonParameters</span></span>
<span data-ttu-id="f26da-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f26da-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26da-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f26da-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26da-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f26da-158">INPUTS</span></span>

### <span data-ttu-id="f26da-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f26da-159">System.String</span></span>

### <span data-ttu-id="f26da-160">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="f26da-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="f26da-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f26da-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f26da-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f26da-162">OUTPUTS</span></span>

### <span data-ttu-id="f26da-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="f26da-163">System.Void</span></span>

## <span data-ttu-id="f26da-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f26da-164">NOTES</span></span>

## <span data-ttu-id="f26da-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f26da-165">RELATED LINKS</span></span>

[<span data-ttu-id="f26da-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f26da-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f26da-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f26da-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="f26da-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f26da-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


