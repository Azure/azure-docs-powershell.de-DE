---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157961"
---
# <span data-ttu-id="21eba-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="21eba-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="21eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21eba-102">SYNOPSIS</span></span>
<span data-ttu-id="21eba-103">Stellt ein Speicherkonto für bestimmte BLOB-Bereiche wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="21eba-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="21eba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21eba-104">SYNTAX</span></span>

### <span data-ttu-id="21eba-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="21eba-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21eba-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="21eba-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21eba-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="21eba-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21eba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21eba-108">DESCRIPTION</span></span>
<span data-ttu-id="21eba-109">Das **Cmdlet "Restore-AzStorageBlobRange"** stellt blobs in einem Speicherkonto für bestimmte BLOB-Bereiche wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="21eba-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="21eba-110">Der Startbereich wird einbezogen, und der Endbereich wird beim Blob Restore ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="21eba-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="21eba-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21eba-111">EXAMPLES</span></span>

### <span data-ttu-id="21eba-112">Beispiel 1: Starten der Wiederherstellung von BLOBS in einem Speicherkonto mit bestimmten BLOB-Bereichen</span><span class="sxs-lookup"><span data-stu-id="21eba-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="21eba-113">Dieser Befehl erstellt zuerst zwei BLOB-Bereiche und startet dann die Wiederherstellung von Blobs in einem Speicherkonto mit den 2 BLOB-Bereichen von vor 1 Tag.</span><span class="sxs-lookup"><span data-stu-id="21eba-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="21eba-114">Der Benutzer kann Get-AzStorageAccount, um den Wiederherstellungsstatus zu einem späteren Zeitpunkt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="21eba-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="21eba-115">Beispiel 2: Wiederherstellen aller BLOBs in einem Speicherkonto im Back-End</span><span class="sxs-lookup"><span data-stu-id="21eba-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="21eba-116">Dieser Befehl stellt alle BLOBs in einem Speicherkonto vor 30 Minuten wieder her, und warten Sie, bis die Wiederherstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="21eba-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="21eba-117">Da das Wiederherstellen von BLOBs sehr lange dauern kann, führen Sie es im Back-End mit dem Parameter "-Asjob" aus, und warten Sie dann, bis der Auftrag abgeschlossen ist, und zeigen Sie das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="21eba-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="21eba-118">Beispiel 3: Stellt BLOB-BloBs direkt durch Eingabe-BLOB-Bereiche wieder her, und warten Sie, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="21eba-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="21eba-119">Mit diesem Befehl werden BLOBs in einem Speicherkonto vor einem Tag wiederhergestellt, indem 2 BLOB-Bereiche direkt in das Restore-AzStorageBlobRange eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="21eba-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="21eba-120">Dieser Befehl wartet auf den Abschluss der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="21eba-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="21eba-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21eba-121">PARAMETERS</span></span>

### <span data-ttu-id="21eba-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21eba-122">-AsJob</span></span>
<span data-ttu-id="21eba-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="21eba-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21eba-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="21eba-124">-BlobRestoreRange</span></span>
<span data-ttu-id="21eba-125">Der BLOB-Bereich, der wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21eba-125">The blob range to Restore.</span></span>
<span data-ttu-id="21eba-126">Wenn Sie diesen Parameter nicht angeben, werden alle BLOBs wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="21eba-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="21eba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21eba-127">-DefaultProfile</span></span>
<span data-ttu-id="21eba-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21eba-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21eba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21eba-129">-ResourceGroupName</span></span>
<span data-ttu-id="21eba-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="21eba-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="21eba-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21eba-131">-ResourceId</span></span>
<span data-ttu-id="21eba-132">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="21eba-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="21eba-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21eba-133">-StorageAccount</span></span>
<span data-ttu-id="21eba-134">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="21eba-134">Storage account object</span></span>

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

### <span data-ttu-id="21eba-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21eba-135">-StorageAccountName</span></span>
<span data-ttu-id="21eba-136">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="21eba-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="21eba-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="21eba-137">-TimeToRestore</span></span>
<span data-ttu-id="21eba-138">Die Zeit zum Wiederherstellen des BLOB.</span><span class="sxs-lookup"><span data-stu-id="21eba-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="21eba-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="21eba-139">-WaitForComplete</span></span>
<span data-ttu-id="21eba-140">Warten, bis die Wiederherstellungsaufgabe abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="21eba-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="21eba-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21eba-141">-Confirm</span></span>
<span data-ttu-id="21eba-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21eba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21eba-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21eba-143">-WhatIf</span></span>
<span data-ttu-id="21eba-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21eba-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21eba-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21eba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21eba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21eba-146">CommonParameters</span></span>
<span data-ttu-id="21eba-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21eba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21eba-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21eba-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21eba-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21eba-149">INPUTS</span></span>

### <span data-ttu-id="21eba-150">System.String</span><span class="sxs-lookup"><span data-stu-id="21eba-150">System.String</span></span>

### <span data-ttu-id="21eba-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21eba-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="21eba-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21eba-152">OUTPUTS</span></span>

### <span data-ttu-id="21eba-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="21eba-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="21eba-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21eba-154">NOTES</span></span>

## <span data-ttu-id="21eba-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21eba-155">RELATED LINKS</span></span>
