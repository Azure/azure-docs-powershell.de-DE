---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179547"
---
# <span data-ttu-id="eeb4a-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="eeb4a-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="eeb4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eeb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb4a-103">Entfernen Sie ACL rekursiv für den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="eeb4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb4a-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeb4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eeb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb4a-106">Das Cmdlet **Remove-AzDataLakeGen2AclRecursive** entfernt ACL rekursiv für den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="eeb4a-107">Die ACL-Einträge in der ursprünglichen ACL, die denselben AccessControlType, DefaultScope und Entitäts-Nr. mit Eingabe-ACL-Einträgen (sogar mit unterschiedlicher Berechtigung) haben, werden von Wil LBE entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="eeb4a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eeb4a-108">EXAMPLES</span></span>

### <span data-ttu-id="eeb4a-109">Beispiel 1: rekursives Entfernen von ACL auf einem root-directiry von Dateisystem</span><span class="sxs-lookup"><span data-stu-id="eeb4a-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
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

<span data-ttu-id="eeb4a-110">Mit diesem Befehl wird zunächst ein ACL-Objekt mit zwei ACL-Einträgen erstellt und dann ACL rekursiv in einem Stammverzeichnis eines Dateisystems entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="eeb4a-111">Beispiel 2: rekursives Entfernen von ACL für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="eeb4a-111">Example 2: Remove ACL recursively on a directory</span></span>
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

<span data-ttu-id="eeb4a-112">Dieser Befehl entfernt ACL zunächst rekursiv in einem Verzeichnis und ist fehlgeschlagen und wird dann mit ContinuationToken fortgesetzt, nachdem der Benutzer die fehlerhafte Datei repariert hat.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="eeb4a-113">Beispiel 3: Entfernen von ACL rekursiv Chunk nach Chunk</span><span class="sxs-lookup"><span data-stu-id="eeb4a-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
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

<span data-ttu-id="eeb4a-114">Dieses Skript entfernt ACL-rescursively für Verzeichnis Chunk nach Chunk, wobei die Chunkgröße als BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="eeb4a-115">Chunk Size ist 50000 in diesem Skript.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="eeb4a-116">Beispiel 4: Entfernen Sie ACL rekursiv für ein Verzeichnis und ContinueOnFailure, und führen Sie dann eine nach der anderen aus.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
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

<span data-ttu-id="eeb4a-117">Mit diesem Befehl wird ACL zunächst rekursiv in ein Verzeichnis mit ContinueOnFailure entfernt, und einige Elemente sind fehlgeschlagen, und dann werden die fehlerhaften Elemente nacheinander fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="eeb4a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeb4a-118">PARAMETERS</span></span>

### <span data-ttu-id="eeb4a-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="eeb4a-119">-Acl</span></span>
<span data-ttu-id="eeb4a-120">Die POSIX-Zugriffssteuerungsliste, die rekursiv für die Datei oder das Verzeichnis gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="eeb4a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeb4a-121">-AsJob</span></span>
<span data-ttu-id="eeb4a-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eeb4a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eeb4a-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="eeb4a-123">-BatchSize</span></span>
<span data-ttu-id="eeb4a-124">Wenn die Datensatzgröße die Batchgröße überschreitet, wird der Vorgang in mehrere Anforderungen aufgeteilt, damit der Status nachverfolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="eeb4a-125">Die Batch Größe sollte zwischen 1 und 2000 liegen.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="eeb4a-126">Standard ist 2000.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-126">Default is 2000.</span></span>

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

### <span data-ttu-id="eeb4a-127">-Context</span><span class="sxs-lookup"><span data-stu-id="eeb4a-127">-Context</span></span>
<span data-ttu-id="eeb4a-128">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="eeb4a-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="eeb4a-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="eeb4a-129">-ContinuationToken</span></span>
<span data-ttu-id="eeb4a-130">Fortsetzungs Token.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-130">Continuation Token.</span></span>

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

### <span data-ttu-id="eeb4a-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="eeb4a-131">-ContinueOnFailure</span></span>
<span data-ttu-id="eeb4a-132">Setzen Sie diesen Parameter, um Fehler zu ignorieren, und setzen Sie proceeing mit dem Vorgang auf anderen unter Entitäten des Verzeichnisses fort.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="eeb4a-133">Standardmäßig wird der Vorgang beim Auftreten von Fehlern schnell beendet.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="eeb4a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb4a-134">-DefaultProfile</span></span>
<span data-ttu-id="eeb4a-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb4a-136">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="eeb4a-136">-FileSystem</span></span>
<span data-ttu-id="eeb4a-137">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="eeb4a-137">FileSystem name</span></span>

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

### <span data-ttu-id="eeb4a-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="eeb4a-138">-MaxBatchCount</span></span>
<span data-ttu-id="eeb4a-139">Die maximale Anzahl von Batches, die von einer Zugriffs Steuerungs Operation für einzelne Änderungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="eeb4a-140">Wenn die Datensatzgröße MaxBatchCount multiplizieren BatchSize überschreitet, wird das Fortsetzungstoken zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="eeb4a-141">-Path</span><span class="sxs-lookup"><span data-stu-id="eeb4a-141">-Path</span></span>
<span data-ttu-id="eeb4a-142">Der Pfad im angegebenen Dateisystem, in dem die ACL rekursiv geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="eeb4a-143">Kann eine Datei oder ein Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-143">Can be a file or directory.</span></span>
<span data-ttu-id="eeb4a-144">Im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="eeb4a-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="eeb4a-145">Überspringen Sie diesen Parameter festlegen, um die ACL rekursiv vom Stammverzeichnis des Dateisystems zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="eeb4a-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeb4a-146">-Confirm</span></span>
<span data-ttu-id="eeb4a-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb4a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb4a-148">-WhatIf</span></span>
<span data-ttu-id="eeb4a-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb4a-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb4a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb4a-151">CommonParameters</span></span>
<span data-ttu-id="eeb4a-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb4a-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb4a-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb4a-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eeb4a-154">INPUTS</span></span>

### <span data-ttu-id="eeb4a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb4a-155">System.String</span></span>

### <span data-ttu-id="eeb4a-156">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eeb4a-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eeb4a-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eeb4a-157">OUTPUTS</span></span>

### <span data-ttu-id="eeb4a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb4a-158">System.String</span></span>

## <span data-ttu-id="eeb4a-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="eeb4a-159">NOTES</span></span>

## <span data-ttu-id="eeb4a-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eeb4a-160">RELATED LINKS</span></span>
