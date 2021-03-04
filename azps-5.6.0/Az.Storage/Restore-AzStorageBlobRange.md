---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: 0d742c257927c06686dc9ce799cdc3e4a5b92340
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950536"
---
# <span data-ttu-id="7db5b-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="7db5b-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="7db5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7db5b-103">Stellt ein Speicherkonto für bestimmte Blobbereiche wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7db5b-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="7db5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7db5b-104">SYNTAX</span></span>

### <span data-ttu-id="7db5b-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7db5b-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db5b-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7db5b-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db5b-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7db5b-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7db5b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7db5b-108">DESCRIPTION</span></span>
<span data-ttu-id="7db5b-109">Das **Cmdlet Restore-AzStorageBlobRange** stellt Blobs in einem Speicherkonto für bestimmte Blobbereiche wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7db5b-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="7db5b-110">Der Startbereich wird einbezogen, und der Endbereich wird in der Blobwiederherstellung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7db5b-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="7db5b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7db5b-111">EXAMPLES</span></span>

### <span data-ttu-id="7db5b-112">Beispiel 1: Start stellt Blobs in einem Speicherkonto mit bestimmten Blobbereichen wieder zur Verfügung</span><span class="sxs-lookup"><span data-stu-id="7db5b-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="7db5b-113">Mit diesem Befehl werden zuerst zwei Blobbereiche erstellt und anschließend blobs in einem Speicherkonto mit den 2 Blobbereichen von vor einem Tag wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="7db5b-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="7db5b-114">Der Benutzer kann Get-AzStorageAccount verwenden, um den Wiederherstellungsstatus zu einem späteren Zeitpunkt nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="7db5b-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="7db5b-115">Beispiel 2: Wiederherstellen aller Blobs in einem Speicherkonto im Back-End</span><span class="sxs-lookup"><span data-stu-id="7db5b-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="7db5b-116">Mit diesem Befehl werden alle Blobs in einem Speicherkonto vor 30 Minuten wiederhergestellt, und warten Sie, bis die Wiederherstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7db5b-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="7db5b-117">Da das Wiederherstellen von Blobs sehr lange dauern kann, führen Sie sie im Back-End mit dem Parameter -Asjob aus, warten Sie dann, bis der Auftrag abgeschlossen ist, und zeigen Sie das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="7db5b-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="7db5b-118">Beispiel 3: Stellt Blobs nach Eingabeblobbereichen direkt wieder her, und warten Sie auf den Abschluss.</span><span class="sxs-lookup"><span data-stu-id="7db5b-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="7db5b-119">Mit diesem Befehl werden Blobs in einem Speicherkonto von vor 1 Tag wiederhergestellt, indem 2 Blobbereiche direkt in das cmdlet Restore-AzStorageBlobRange werden.</span><span class="sxs-lookup"><span data-stu-id="7db5b-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="7db5b-120">Dieser Befehl wartet, bis die Wiederherstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7db5b-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="7db5b-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7db5b-121">PARAMETERS</span></span>

### <span data-ttu-id="7db5b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7db5b-122">-AsJob</span></span>
<span data-ttu-id="7db5b-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7db5b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7db5b-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="7db5b-124">-BlobRestoreRange</span></span>
<span data-ttu-id="7db5b-125">Der Blobbereich, der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7db5b-125">The blob range to Restore.</span></span>
<span data-ttu-id="7db5b-126">Wenn Sie diesen Parameter nicht angeben, werden alle Blobs wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="7db5b-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db5b-127">-DefaultProfile</span></span>
<span data-ttu-id="7db5b-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7db5b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db5b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db5b-129">-ResourceGroupName</span></span>
<span data-ttu-id="7db5b-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7db5b-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7db5b-131">-ResourceId</span></span>
<span data-ttu-id="7db5b-132">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="7db5b-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7db5b-133">-StorageAccount</span></span>
<span data-ttu-id="7db5b-134">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7db5b-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7db5b-135">-StorageAccountName</span></span>
<span data-ttu-id="7db5b-136">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="7db5b-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="7db5b-137">-TimeToRestore</span></span>
<span data-ttu-id="7db5b-138">Die Zeit zum Wiederherstellen des Blobs.</span><span class="sxs-lookup"><span data-stu-id="7db5b-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db5b-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7db5b-139">-WaitForComplete</span></span>
<span data-ttu-id="7db5b-140">Warten, bis die Wiederherstellungsaufgabe abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="7db5b-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="7db5b-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7db5b-141">-Confirm</span></span>
<span data-ttu-id="7db5b-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7db5b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db5b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db5b-143">-WhatIf</span></span>
<span data-ttu-id="7db5b-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7db5b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7db5b-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7db5b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db5b-146">CommonParameters</span></span>
<span data-ttu-id="7db5b-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db5b-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db5b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db5b-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7db5b-149">INPUTS</span></span>

### <span data-ttu-id="7db5b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7db5b-150">System.String</span></span>

### <span data-ttu-id="7db5b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7db5b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7db5b-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7db5b-152">OUTPUTS</span></span>

### <span data-ttu-id="7db5b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="7db5b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="7db5b-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7db5b-154">NOTES</span></span>

## <span data-ttu-id="7db5b-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7db5b-155">RELATED LINKS</span></span>
