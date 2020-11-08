---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179981"
---
# <span data-ttu-id="3cf63-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="3cf63-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="3cf63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cf63-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf63-103">Aktiviert die BLOB-Wiederherstellungsrichtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="3cf63-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="3cf63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf63-104">SYNTAX</span></span>

### <span data-ttu-id="3cf63-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cf63-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf63-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="3cf63-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf63-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf63-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf63-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf63-109">Das Cmdlet **enable-AzStorageBlobRestorePolicy** aktiviert die BLOB-Wiederherstellungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3cf63-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="3cf63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf63-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf63-111">Beispiel 1: aktiviert die BLOB-Wiederherstellungsrichtlinie für den Azure Storage-BLOB-Dienst auf einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3cf63-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="3cf63-112">Dieser Befehl aktiviert zunächst BLOB-softdelete und changefeed, aktiviert dann die BLOB-Wiederherstellungsrichtlinie und überprüft schließlich die Einstellung in den BLOB-Diensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cf63-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="3cf63-113">Der BLOB-Dienst RestorePolicy. Days muss kleiner als DeleteRetentionPolicy. Days sein.</span><span class="sxs-lookup"><span data-stu-id="3cf63-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="3cf63-114">BLOB-softdelete und-ChangeFeed müssen aktiviert sein, bevor die BLOB-Wiederherstellungsrichtlinie aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf63-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="3cf63-115">Wenn softdelete und changefeed gerade aktiviert sind, müssen Sie möglicherweise einige Zeit warten, bis Server die Einstellung verarbeitet, bevor Sie die BLOB-Wiederherstellungsrichtlinie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3cf63-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="3cf63-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf63-116">PARAMETERS</span></span>

### <span data-ttu-id="3cf63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf63-117">-DefaultProfile</span></span>
<span data-ttu-id="3cf63-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cf63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf63-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cf63-119">-PassThru</span></span>
<span data-ttu-id="3cf63-120">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="3cf63-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="3cf63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf63-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cf63-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cf63-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3cf63-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3cf63-123">-ResourceId</span></span>
<span data-ttu-id="3cf63-124">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für BLOB-Diensteigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3cf63-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf63-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="3cf63-125">-RestoreDays</span></span>
<span data-ttu-id="3cf63-126">Legt fest, wie viele Tage das BLOB wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf63-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf63-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cf63-127">-StorageAccount</span></span>
<span data-ttu-id="3cf63-128">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="3cf63-128">Storage account object</span></span>

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

### <span data-ttu-id="3cf63-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cf63-129">-StorageAccountName</span></span>
<span data-ttu-id="3cf63-130">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3cf63-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf63-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cf63-131">-Confirm</span></span>
<span data-ttu-id="3cf63-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cf63-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf63-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf63-133">-WhatIf</span></span>
<span data-ttu-id="3cf63-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf63-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf63-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf63-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf63-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf63-136">CommonParameters</span></span>
<span data-ttu-id="3cf63-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf63-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf63-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf63-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf63-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cf63-139">INPUTS</span></span>

### <span data-ttu-id="3cf63-140">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cf63-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3cf63-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf63-141">System.String</span></span>

## <span data-ttu-id="3cf63-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cf63-142">OUTPUTS</span></span>

### <span data-ttu-id="3cf63-143">Microsoft. Azure. Commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="3cf63-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="3cf63-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cf63-144">NOTES</span></span>

## <span data-ttu-id="3cf63-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cf63-145">RELATED LINKS</span></span>
