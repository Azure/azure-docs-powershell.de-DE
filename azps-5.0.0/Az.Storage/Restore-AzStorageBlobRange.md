---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175993"
---
# <span data-ttu-id="522f9-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="522f9-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="522f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="522f9-102">SYNOPSIS</span></span>
<span data-ttu-id="522f9-103">Stellt ein Speicherkonto für bestimmte BLOB-Bereiche wieder her.</span><span class="sxs-lookup"><span data-stu-id="522f9-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="522f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="522f9-104">SYNTAX</span></span>

### <span data-ttu-id="522f9-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="522f9-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522f9-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="522f9-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522f9-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="522f9-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522f9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="522f9-108">DESCRIPTION</span></span>
<span data-ttu-id="522f9-109">Das Cmdlet **Restore-AzStorageBlobRange** stellt BLOBs in einem Speicherkonto für bestimmte BLOB-Bereiche wieder her.</span><span class="sxs-lookup"><span data-stu-id="522f9-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="522f9-110">Der Startbereich ist enthalten, und der Endbereich wird in der BLOB-Wiederherstellung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="522f9-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="522f9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="522f9-111">EXAMPLES</span></span>

### <span data-ttu-id="522f9-112">Beispiel 1: Starten der Wiederherstellung von BLOBs in einem Speicherkonto mit bestimmten BLOB-Bereichen</span><span class="sxs-lookup"><span data-stu-id="522f9-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="522f9-113">Mit diesem Befehl werden zunächst zwei BLOB-Bereiche erstellt, und anschließend werden die BLOB-Daten in einem Speicherkonto mit den 2 BLOB-Bereichen von vor einem Tag wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="522f9-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="522f9-114">Der Benutzer kann Get-AzStorageAccount verwenden, um den Wiederherstellungsstatus später nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="522f9-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="522f9-115">Beispiel 2: stellt alle BLOBs in einem Speicherkonto im Back-End wieder her</span><span class="sxs-lookup"><span data-stu-id="522f9-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="522f9-116">Mit diesem Befehl werden alle BLOBs in einem Speicherkonto vor 30 Minuten wiederhergestellt, und es wird gewartet, bis die Wiederherstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="522f9-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="522f9-117">Da die BLOB-Wiederherstellung lange Zeit in Anspruch nehmen kann, führen Sie Sie im Back-End-Parameter mit-AsJob aus, und warten Sie, bis der Vorgang abgeschlossen ist, und zeigen Sie das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="522f9-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="522f9-118">Beispiel 3: Wiederherstellung von BLOBs durch Eingabe von BLOB-Bereichen direkt und warten auf "abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="522f9-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="522f9-119">Dieser Befehl stellt BLOB-Daten in einem Speicherkonto ab 1 Tag wieder her, indem 2 BLOB-Bereiche direkt in das Restore-AzStorageBlobRange-Cmdlet eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="522f9-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="522f9-120">Dieser Befehl wartet darauf, dass die Wiederherstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="522f9-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="522f9-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="522f9-121">PARAMETERS</span></span>

### <span data-ttu-id="522f9-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="522f9-122">-AsJob</span></span>
<span data-ttu-id="522f9-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="522f9-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="522f9-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="522f9-124">-BlobRestoreRange</span></span>
<span data-ttu-id="522f9-125">Der wiederherzustellende BLOB-Bereich.</span><span class="sxs-lookup"><span data-stu-id="522f9-125">The blob range to Restore.</span></span>
<span data-ttu-id="522f9-126">Wenn Sie diesen Parameter nicht angeben, werden alle Blobs wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="522f9-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="522f9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522f9-127">-DefaultProfile</span></span>
<span data-ttu-id="522f9-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="522f9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="522f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="522f9-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="522f9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="522f9-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="522f9-131">-ResourceId</span></span>
<span data-ttu-id="522f9-132">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="522f9-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="522f9-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="522f9-133">-StorageAccount</span></span>
<span data-ttu-id="522f9-134">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="522f9-134">Storage account object</span></span>

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

### <span data-ttu-id="522f9-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="522f9-135">-StorageAccountName</span></span>
<span data-ttu-id="522f9-136">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="522f9-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="522f9-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="522f9-137">-TimeToRestore</span></span>
<span data-ttu-id="522f9-138">Der Zeitpunkt, zu dem BLOB wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="522f9-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="522f9-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="522f9-139">-WaitForComplete</span></span>
<span data-ttu-id="522f9-140">Warten Sie, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="522f9-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="522f9-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="522f9-141">-Confirm</span></span>
<span data-ttu-id="522f9-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="522f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="522f9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522f9-143">-WhatIf</span></span>
<span data-ttu-id="522f9-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="522f9-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="522f9-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="522f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="522f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522f9-146">CommonParameters</span></span>
<span data-ttu-id="522f9-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522f9-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522f9-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522f9-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="522f9-149">INPUTS</span></span>

### <span data-ttu-id="522f9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="522f9-150">System.String</span></span>

### <span data-ttu-id="522f9-151">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="522f9-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="522f9-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="522f9-152">OUTPUTS</span></span>

### <span data-ttu-id="522f9-153">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="522f9-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="522f9-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="522f9-154">NOTES</span></span>

## <span data-ttu-id="522f9-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="522f9-155">RELATED LINKS</span></span>
