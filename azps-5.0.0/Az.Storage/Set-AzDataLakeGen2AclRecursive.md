---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 1d2a4bc1dd9dab05e56f8b69c92d98985cf98e15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175989"
---
# <span data-ttu-id="beaf2-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="beaf2-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="beaf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="beaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="beaf2-103">Setzen Sie ACL rekursiv für den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="beaf2-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="beaf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="beaf2-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beaf2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beaf2-105">DESCRIPTION</span></span>
<span data-ttu-id="beaf2-106">Das Cmdlet " **Set-AzDataLakeGen2AclRecursive** " legt ACL rekursiv für den angegebenen Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="beaf2-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="beaf2-107">Die Eingabe-ACL ersetzt die ursprüngliche ACL vollständig.</span><span class="sxs-lookup"><span data-stu-id="beaf2-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="beaf2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beaf2-108">EXAMPLES</span></span>

### <span data-ttu-id="beaf2-109">Beispiel 1: setzen Sie ACL rekursiv auf einem directiry</span><span class="sxs-lookup"><span data-stu-id="beaf2-109">Example 1: Set ACL recursively on a directiry</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="beaf2-110">Mit diesem Befehl wird zunächst ein ACL-Objekt mit 3 ACL-Einträgen erstellt und dann ACL rekursiv für ein Verzeichnis festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beaf2-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="beaf2-111">Beispiel 2: Einrichten von ACL rekursiv auf einem root-directiry von Dateisystem</span><span class="sxs-lookup"><span data-stu-id="beaf2-111">Example 2: Set ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="beaf2-112">Mit diesem Befehl wird ACL zunächst rekursiv auf ein Stammverzeichnis festgelegt und ist fehlgeschlagen, und dann mit ContinuationToken fortgesetzt, nachdem der Benutzer die fehlerhafte Datei repariert hat.</span><span class="sxs-lookup"><span data-stu-id="beaf2-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="beaf2-113">Beispiel 3: Einrichten von ACL rekursiv Chunk nach Chunk</span><span class="sxs-lookup"><span data-stu-id="beaf2-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

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

<span data-ttu-id="beaf2-114">Dieses Skript legt ACL-rescursively für Verzeichnis Chunk nach Chunk fest, wobei die Chunkgröße als BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="beaf2-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="beaf2-115">Chunk Size ist 200 in diesem Skript.</span><span class="sxs-lookup"><span data-stu-id="beaf2-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="beaf2-116">Beispiel 4: setzen Sie ACL rekursiv auf ein Verzeichnis und ContinueOnFailure, und führen Sie dann eine nach dem anderen aus Fehlern fort.</span><span class="sxs-lookup"><span data-stu-id="beaf2-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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

<span data-ttu-id="beaf2-117">Mit diesem Befehl wird ACL zunächst rekursiv auf ein Verzeichnis mit ContinueOnFailure festgelegt, und einige Elemente sind fehlgeschlagen, und dann werden die fehlerhaften Elemente nacheinander fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="beaf2-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="beaf2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="beaf2-118">PARAMETERS</span></span>

### <span data-ttu-id="beaf2-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="beaf2-119">-Acl</span></span>
<span data-ttu-id="beaf2-120">Die POSIX-Zugriffssteuerungsliste, die rekursiv für die Datei oder das Verzeichnis gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="beaf2-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="beaf2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beaf2-121">-AsJob</span></span>
<span data-ttu-id="beaf2-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="beaf2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="beaf2-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="beaf2-123">-BatchSize</span></span>
<span data-ttu-id="beaf2-124">Wenn die Datensatzgröße die Batchgröße überschreitet, wird der Vorgang in mehrere Anforderungen aufgeteilt, damit der Status nachverfolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="beaf2-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="beaf2-125">Die Batch Größe sollte zwischen 1 und 2000 liegen.</span><span class="sxs-lookup"><span data-stu-id="beaf2-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="beaf2-126">Standard ist 2000.</span><span class="sxs-lookup"><span data-stu-id="beaf2-126">Default is 2000.</span></span>

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

### <span data-ttu-id="beaf2-127">-Context</span><span class="sxs-lookup"><span data-stu-id="beaf2-127">-Context</span></span>
<span data-ttu-id="beaf2-128">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="beaf2-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="beaf2-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="beaf2-129">-ContinuationToken</span></span>
<span data-ttu-id="beaf2-130">Fortsetzungs Token.</span><span class="sxs-lookup"><span data-stu-id="beaf2-130">Continuation Token.</span></span>

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

### <span data-ttu-id="beaf2-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="beaf2-131">-ContinueOnFailure</span></span>
<span data-ttu-id="beaf2-132">Setzen Sie diesen Parameter, um Fehler zu ignorieren, und setzen Sie proceeing mit dem Vorgang auf anderen unter Entitäten des Verzeichnisses fort.</span><span class="sxs-lookup"><span data-stu-id="beaf2-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="beaf2-133">Standardmäßig wird der Vorgang beim Auftreten von Fehlern schnell beendet.</span><span class="sxs-lookup"><span data-stu-id="beaf2-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="beaf2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaf2-134">-DefaultProfile</span></span>
<span data-ttu-id="beaf2-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="beaf2-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beaf2-136">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="beaf2-136">-FileSystem</span></span>
<span data-ttu-id="beaf2-137">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="beaf2-137">FileSystem name</span></span>

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

### <span data-ttu-id="beaf2-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="beaf2-138">-MaxBatchCount</span></span>
<span data-ttu-id="beaf2-139">Die maximale Anzahl von Batches, die von einer Zugriffs Steuerungs Operation für einzelne Änderungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="beaf2-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="beaf2-140">Wenn die Datensatzgröße MaxBatchCount multiplizieren BatchSize überschreitet, wird das Fortsetzungstoken zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="beaf2-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="beaf2-141">-Path</span><span class="sxs-lookup"><span data-stu-id="beaf2-141">-Path</span></span>
<span data-ttu-id="beaf2-142">Der Pfad im angegebenen Dateisystem, in dem die ACL rekursiv geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="beaf2-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="beaf2-143">Kann eine Datei oder ein Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="beaf2-143">Can be a file or directory.</span></span>
<span data-ttu-id="beaf2-144">Im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="beaf2-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="beaf2-145">Überspringen Sie diesen Parameter festlegen, um die ACL rekursiv vom Stammverzeichnis des Dateisystems zu ändern.</span><span class="sxs-lookup"><span data-stu-id="beaf2-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="beaf2-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beaf2-146">-Confirm</span></span>
<span data-ttu-id="beaf2-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beaf2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaf2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaf2-148">-WhatIf</span></span>
<span data-ttu-id="beaf2-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beaf2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaf2-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beaf2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaf2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaf2-151">CommonParameters</span></span>
<span data-ttu-id="beaf2-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beaf2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaf2-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beaf2-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaf2-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="beaf2-154">INPUTS</span></span>

### <span data-ttu-id="beaf2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="beaf2-155">System.String</span></span>

### <span data-ttu-id="beaf2-156">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="beaf2-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="beaf2-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="beaf2-157">OUTPUTS</span></span>

### <span data-ttu-id="beaf2-158">System. String</span><span class="sxs-lookup"><span data-stu-id="beaf2-158">System.String</span></span>

## <span data-ttu-id="beaf2-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="beaf2-159">NOTES</span></span>

## <span data-ttu-id="beaf2-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="beaf2-160">RELATED LINKS</span></span>
