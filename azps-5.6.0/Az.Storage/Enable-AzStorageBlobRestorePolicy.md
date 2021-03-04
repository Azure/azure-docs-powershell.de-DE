---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929288"
---
# <span data-ttu-id="e7015-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e7015-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="e7015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7015-102">SYNOPSIS</span></span>
<span data-ttu-id="e7015-103">Aktiviert die Blobwiederherstellungsrichtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="e7015-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="e7015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7015-104">SYNTAX</span></span>

### <span data-ttu-id="e7015-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7015-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7015-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e7015-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7015-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e7015-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7015-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7015-108">DESCRIPTION</span></span>
<span data-ttu-id="e7015-109">Das **Cmdlet Enable-AzStorageBlobRestorePolicy** aktiviert die Blob Restore-Richtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="e7015-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e7015-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7015-110">EXAMPLES</span></span>

### <span data-ttu-id="e7015-111">Beispiel 1: Aktiviert blob restore policy for the Azure Storage Blob service on a Storage account</span><span class="sxs-lookup"><span data-stu-id="e7015-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="e7015-112">Mit diesem Befehl aktivieren Sie zuerst Blob softdelete und changefeed, dann blob restore policy, und überprüfen Sie schließlich die Einstellung in blob service properties.</span><span class="sxs-lookup"><span data-stu-id="e7015-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="e7015-113">Der Blobdienst RestorePolicy.Days muss kleiner als DeleteRetentionPolicy.Days sein.</span><span class="sxs-lookup"><span data-stu-id="e7015-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="e7015-114">Blob softdelete und ChangeFeed müssen aktiviert sein, bevor sie die Blobwiederherstellungsrichtlinie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e7015-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="e7015-115">Wenn softdelete und Changefeed gerade aktiviert sind, müssen Sie möglicherweise einige Zeit warten, bis der Server die Einstellung verarbeiten kann, bevor Sie die Blobwiederherstellungsrichtlinie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e7015-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="e7015-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7015-116">PARAMETERS</span></span>

### <span data-ttu-id="e7015-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7015-117">-DefaultProfile</span></span>
<span data-ttu-id="e7015-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7015-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7015-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7015-119">-PassThru</span></span>
<span data-ttu-id="e7015-120">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="e7015-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e7015-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7015-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7015-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e7015-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e7015-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7015-123">-ResourceId</span></span>
<span data-ttu-id="e7015-124">Geben Sie eine Ressourcen-ID des Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="e7015-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="e7015-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="e7015-125">-RestoreDays</span></span>
<span data-ttu-id="e7015-126">Legt die Anzahl der Tage fest, die für den Blob wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="e7015-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="e7015-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7015-127">-StorageAccount</span></span>
<span data-ttu-id="e7015-128">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e7015-128">Storage account object</span></span>

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

### <span data-ttu-id="e7015-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e7015-129">-StorageAccountName</span></span>
<span data-ttu-id="e7015-130">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="e7015-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="e7015-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7015-131">-Confirm</span></span>
<span data-ttu-id="e7015-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7015-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7015-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7015-133">-WhatIf</span></span>
<span data-ttu-id="e7015-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7015-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7015-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7015-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7015-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7015-136">CommonParameters</span></span>
<span data-ttu-id="e7015-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7015-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7015-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7015-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7015-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7015-139">INPUTS</span></span>

### <span data-ttu-id="e7015-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7015-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e7015-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e7015-141">System.String</span></span>

## <span data-ttu-id="e7015-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7015-142">OUTPUTS</span></span>

### <span data-ttu-id="e7015-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e7015-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="e7015-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7015-144">NOTES</span></span>

## <span data-ttu-id="e7015-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7015-145">RELATED LINKS</span></span>
