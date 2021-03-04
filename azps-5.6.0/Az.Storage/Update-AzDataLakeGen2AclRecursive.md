---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 028489985ff7f2c6054ffe3a7b66e94823573356
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922608"
---
# <span data-ttu-id="29b02-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="29b02-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="29b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b02-102">SYNOPSIS</span></span>
<span data-ttu-id="29b02-103">Aktualisieren Sie ACL für den angegebenen Pfad rekursiv.</span><span class="sxs-lookup"><span data-stu-id="29b02-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="29b02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29b02-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29b02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29b02-105">DESCRIPTION</span></span>
<span data-ttu-id="29b02-106">Das **Update-AzDataLakeGen2AclRecursive-Cmdlet** aktualisiert ACL rekursiv auf dem angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="29b02-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="29b02-107">Die Eingabe-ACL führt die ursprüngliche ACL zusammen: Wenn der #A1 mit demselben AccessControlType/EntityId/DefaultScope vorhanden ist, aktualisieren Sie die Berechtigung; fügen Sie sonst einen neuen ACL-Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="29b02-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="29b02-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29b02-108">EXAMPLES</span></span>

### <span data-ttu-id="29b02-109">Beispiel 1: Rekursives Aktualisieren der ACL für eine Stammverzeichnisse des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="29b02-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="29b02-110">Mit diesem Befehl wird zuerst ein ACL-Objekt mit drei acl-Einträgen erstellt und dann ACL rekursiv in einem Stammverzeichnis eines Dateisystems aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="29b02-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="29b02-111">Beispiel 2: Aktualisieren der ACL rekursiv für ein Verzeichnis und Fortsetzen eines Fehlers mit ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="29b02-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="29b02-112">Mit diesem Befehl wird ACL zuerst rekursiv auf ein Verzeichnis aktualisiert und ein Fehler auftritt, und dann mit ContinuationToken fortgesetzt, nachdem der Benutzer die fehlgeschlagene Datei behoben hat.</span><span class="sxs-lookup"><span data-stu-id="29b02-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="29b02-113">Beispiel 3: Aktualisieren von ACL rekursiv chunk by chunk</span><span class="sxs-lookup"><span data-stu-id="29b02-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="29b02-114">Dieses Skript aktualisiert ACL rescursive für Verzeichnisblöcke nach Abschnitten, und die Größe des Abschnitts wird als BatchSize \* MaxBatchCount angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29b02-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="29b02-115">Die Blockgröße in diesem Skript beträgt 5000.</span><span class="sxs-lookup"><span data-stu-id="29b02-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="29b02-116">Beispiel 4: Aktualisieren Sie ACL rekursiv für ein Verzeichnis und ContinueOnFailure, und führen Sie dann die Fortsetzung von Fehlern nach und nach aus.</span><span class="sxs-lookup"><span data-stu-id="29b02-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="29b02-117">Mit diesem Befehl wird ACL zuerst rekursiv auf ein Verzeichnis mit ContinueOnFailure aktualisiert, und einige Elemente sind fehlgeschlagen, und die fehlgeschlagenen Elemente werden dann nach und nach fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="29b02-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="29b02-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29b02-118">PARAMETERS</span></span>

### <span data-ttu-id="29b02-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="29b02-119">-Acl</span></span>
<span data-ttu-id="29b02-120">Die POSIX-Zugriffssteuerungsliste, die rekursiv für die Datei oder das Verzeichnis festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b02-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="29b02-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29b02-121">-AsJob</span></span>
<span data-ttu-id="29b02-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29b02-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29b02-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="29b02-123">-BatchSize</span></span>
<span data-ttu-id="29b02-124">Wenn die Größe des Datensets die Batchgröße überschreitet, wird der Vorgang in mehrere Anforderungen aufgeteilt, sodass der Fortschritt nachverfolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="29b02-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="29b02-125">Die Batchgröße sollte zwischen 1 und 2000 liegen.</span><span class="sxs-lookup"><span data-stu-id="29b02-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="29b02-126">Der Standardwert ist 2000.</span><span class="sxs-lookup"><span data-stu-id="29b02-126">Default is 2000.</span></span>

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

### <span data-ttu-id="29b02-127">-Context</span><span class="sxs-lookup"><span data-stu-id="29b02-127">-Context</span></span>
<span data-ttu-id="29b02-128">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="29b02-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="29b02-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="29b02-129">-ContinuationToken</span></span>
<span data-ttu-id="29b02-130">Fortsetzungstoken.</span><span class="sxs-lookup"><span data-stu-id="29b02-130">Continuation Token.</span></span>

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

### <span data-ttu-id="29b02-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="29b02-131">-ContinueOnFailure</span></span>
<span data-ttu-id="29b02-132">Legen Sie diesen Parameter so ein, dass Fehler ignoriert werden, und fahren Sie mit dem Vorgang für andere Unterentitäten des Verzeichnisses fort.</span><span class="sxs-lookup"><span data-stu-id="29b02-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="29b02-133">Standardmäßig wird der Vorgang bei Auftreten von Fehlern schnell beendet.</span><span class="sxs-lookup"><span data-stu-id="29b02-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="29b02-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b02-134">-DefaultProfile</span></span>
<span data-ttu-id="29b02-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29b02-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b02-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="29b02-136">-FileSystem</span></span>
<span data-ttu-id="29b02-137">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="29b02-137">FileSystem name</span></span>

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

### <span data-ttu-id="29b02-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="29b02-138">-MaxBatchCount</span></span>
<span data-ttu-id="29b02-139">Maximale Anzahl von Batches, die durch einmaliges Ändern des Zugriffssteuerungsvorgangs ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="29b02-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="29b02-140">Wenn die Größe des Datentyps maxBatchCount multiplizieren BatchSize überschreitet, wird das Fortsetzungstoken zurückgezahlt.</span><span class="sxs-lookup"><span data-stu-id="29b02-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="29b02-141">-Path</span><span class="sxs-lookup"><span data-stu-id="29b02-141">-Path</span></span>
<span data-ttu-id="29b02-142">Der Pfad im angegebenen Dateisystem, der rekursiv geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b02-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="29b02-143">Kann eine Datei oder ein Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="29b02-143">Can be a file or directory.</span></span>
<span data-ttu-id="29b02-144">Im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/".</span><span class="sxs-lookup"><span data-stu-id="29b02-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="29b02-145">Überspringen Sie diesen Parameter, um Acl rekursiv aus dem Stammverzeichnis des Dateisystems zu ändern.</span><span class="sxs-lookup"><span data-stu-id="29b02-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="29b02-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29b02-146">-Confirm</span></span>
<span data-ttu-id="29b02-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29b02-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b02-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b02-148">-WhatIf</span></span>
<span data-ttu-id="29b02-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29b02-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b02-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29b02-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b02-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b02-151">CommonParameters</span></span>
<span data-ttu-id="29b02-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b02-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b02-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b02-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b02-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29b02-154">INPUTS</span></span>

### <span data-ttu-id="29b02-155">System.String</span><span class="sxs-lookup"><span data-stu-id="29b02-155">System.String</span></span>

### <span data-ttu-id="29b02-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29b02-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29b02-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29b02-157">OUTPUTS</span></span>

### <span data-ttu-id="29b02-158">System.String</span><span class="sxs-lookup"><span data-stu-id="29b02-158">System.String</span></span>

## <span data-ttu-id="29b02-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29b02-159">NOTES</span></span>

## <span data-ttu-id="29b02-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29b02-160">RELATED LINKS</span></span>
