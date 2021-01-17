---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471705"
---
# <span data-ttu-id="97eb8-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="97eb8-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="97eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="97eb8-103">Entfernen Sie den ACL rekursiv für den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="97eb8-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="97eb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97eb8-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97eb8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="97eb8-106">Das **Cmdlet "Remove-AzDataLakeGen2AclRecursive"** entfernt den ACL rekursiv für den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="97eb8-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="97eb8-107">Die ACL-Einträge in der ursprünglichen ACL, die über die gleichen AccessControlType-, DefaultScope- und EntityId-Eingabe-ACL-Einträge (auch mit unterschiedlichen Berechtigungen) verfügt, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="97eb8-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="97eb8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97eb8-108">EXAMPLES</span></span>

### <span data-ttu-id="97eb8-109">Beispiel 1: Rekursives Entfernen von ACL für eine Stammsteuerung des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="97eb8-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="97eb8-110">Mit diesem Befehl wird zuerst ein ACL-Objekt mit zwei acl-Einträgen erstellt und dann rekursiv in einem Stammverzeichnis eines Dateisystems entfernt.</span><span class="sxs-lookup"><span data-stu-id="97eb8-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="97eb8-111">Beispiel 2: Rekursives Entfernen von ACL für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="97eb8-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="97eb8-112">Mit diesem Befehl wird ACL zuerst rekursiv für ein Verzeichnis entfernt und ist fehlgeschlagen. Anschließend wird es mit ContinuationToken fortgesetzt, nachdem der Benutzer die fehlgeschlagene Datei korrigiert hat.</span><span class="sxs-lookup"><span data-stu-id="97eb8-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="97eb8-113">Beispiel 3: Entfernen eines rekursiven ACL-Abschnitts nach Abschnitt</span><span class="sxs-lookup"><span data-stu-id="97eb8-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="97eb8-114">Dieses Skript entfernt ACL rescursiv für verzeichnisblöckeweise mit der Abschnittsgröße "BatchSize \* MaxBatchCount".</span><span class="sxs-lookup"><span data-stu-id="97eb8-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="97eb8-115">Dieses Skript enthält eine Blockgröße von 50000.</span><span class="sxs-lookup"><span data-stu-id="97eb8-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="97eb8-116">Beispiel 4: Rekursives Entfernen von "ACL" für ein Verzeichnis und "ContinueOnFailure" und anschließendes Fortsetzen von Fehlern nach dem anderen</span><span class="sxs-lookup"><span data-stu-id="97eb8-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="97eb8-117">Mit diesem Befehl wird ACL zuerst rekursiv in ein Verzeichnis mit "ContinueOnFailure" entfernt, und bei einigen Elementen ist ein Fehler auftritt, und die fehlgeschlagenen Elemente werden dann nach dem anderen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="97eb8-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="97eb8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97eb8-118">PARAMETERS</span></span>

### <span data-ttu-id="97eb8-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="97eb8-119">-Acl</span></span>
<span data-ttu-id="97eb8-120">Die POSIX-Zugriffssteuerungsliste, die rekursiv für die Datei oder das Verzeichnis festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="97eb8-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97eb8-121">-AsJob</span></span>
<span data-ttu-id="97eb8-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="97eb8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97eb8-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="97eb8-123">-BatchSize</span></span>
<span data-ttu-id="97eb8-124">Wenn die Größe des Datensets die Batchgröße überschreitet, wird der Vorgang in mehrere Anforderungen aufgeteilt, sodass der Fortschritt nachverfolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="97eb8-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="97eb8-125">Die Batchgröße sollte zwischen 1 und 2000 liegen.</span><span class="sxs-lookup"><span data-stu-id="97eb8-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="97eb8-126">Der Standardwert ist 2000.</span><span class="sxs-lookup"><span data-stu-id="97eb8-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-127">-Context</span><span class="sxs-lookup"><span data-stu-id="97eb8-127">-Context</span></span>
<span data-ttu-id="97eb8-128">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="97eb8-128">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="97eb8-129">-ContinuationToken</span></span>
<span data-ttu-id="97eb8-130">Fortsetzungstoken.</span><span class="sxs-lookup"><span data-stu-id="97eb8-130">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="97eb8-131">-ContinueOnFailure</span></span>
<span data-ttu-id="97eb8-132">Legen Sie diesen Parameter so ein, dass Fehler ignoriert werden, und setzen Sie die Prozedur mit dem Vorgang für andere Unterentitäten des Verzeichnisses fort.</span><span class="sxs-lookup"><span data-stu-id="97eb8-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="97eb8-133">Standardmäßig wird der Vorgang bei Auftreten von Fehlern schnell beendet.</span><span class="sxs-lookup"><span data-stu-id="97eb8-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="97eb8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97eb8-134">-DefaultProfile</span></span>
<span data-ttu-id="97eb8-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97eb8-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="97eb8-136">-FileSystem</span></span>
<span data-ttu-id="97eb8-137">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="97eb8-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="97eb8-138">-MaxBatchCount</span></span>
<span data-ttu-id="97eb8-139">Maximale Anzahl von Batches, für die ein einzelner Änderungszugriffssteuerungsvorgang ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="97eb8-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="97eb8-140">Wenn die Größe des Datasets die Multiplikation "BatchSize" von MaxBatchCount überschreitet, wird das Fortsetzungstoken zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="97eb8-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-141">-Path</span><span class="sxs-lookup"><span data-stu-id="97eb8-141">-Path</span></span>
<span data-ttu-id="97eb8-142">Der Pfad im angegebenen FileSystem, der rekursiv geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97eb8-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="97eb8-143">Kann eine Datei oder ein Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="97eb8-143">Can be a file or directory.</span></span>
<span data-ttu-id="97eb8-144">Im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/".</span><span class="sxs-lookup"><span data-stu-id="97eb8-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="97eb8-145">Überspringen Sie das Festlegen dieses Parameters, um "Acl" rekursiv aus dem Stammverzeichnis des Dateisystems zu ändern.</span><span class="sxs-lookup"><span data-stu-id="97eb8-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97eb8-146">-Confirm</span></span>
<span data-ttu-id="97eb8-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97eb8-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="97eb8-148">-WhatIf</span></span>
<span data-ttu-id="97eb8-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97eb8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97eb8-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97eb8-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97eb8-151">CommonParameters</span></span>
<span data-ttu-id="97eb8-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97eb8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97eb8-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97eb8-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97eb8-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97eb8-154">INPUTS</span></span>

### <span data-ttu-id="97eb8-155">System.String</span><span class="sxs-lookup"><span data-stu-id="97eb8-155">System.String</span></span>

### <span data-ttu-id="97eb8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="97eb8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="97eb8-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97eb8-157">OUTPUTS</span></span>

### <span data-ttu-id="97eb8-158">System.String</span><span class="sxs-lookup"><span data-stu-id="97eb8-158">System.String</span></span>

## <span data-ttu-id="97eb8-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97eb8-159">NOTES</span></span>

## <span data-ttu-id="97eb8-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97eb8-160">RELATED LINKS</span></span>
