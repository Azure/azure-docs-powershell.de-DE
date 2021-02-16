---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150433"
---
# <span data-ttu-id="f9dbd-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f9dbd-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="f9dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dbd-103">Aktiviert die Blob Restore-Richtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="f9dbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9dbd-104">SYNTAX</span></span>

### <span data-ttu-id="f9dbd-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9dbd-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9dbd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f9dbd-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9dbd-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f9dbd-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9dbd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="f9dbd-109">Das **Cmdlet "Enable-AzStorageBlobRestorePolicy"** aktiviert die Blob Restore Policy für den Azure Storage BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f9dbd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="f9dbd-111">Beispiel 1: Aktiviert die Blob Restore-Richtlinie für den Azure Storage -BLOB-Dienst für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="f9dbd-112">Dieser Befehl aktiviert zuerst BLOB softdelete und changefeed, aktiviert dann die Blob Restore Policy und überprüft schließlich die Einstellung in den Eigenschaften des BLOB-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="f9dbd-113">Der Blob-Dienst RestorePolicy.Days muss kleiner als DeleteRetentionPolicy.Days sein.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="f9dbd-114">Blob softdelete und ChangeFeed müssen aktiviert sein, bevor die Blob Restore Policy aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="f9dbd-115">Wenn Softdelete und Changefeed gerade aktiviert sind, müssen Sie möglicherweise einige Zeit warten, bis der Server die Einstellung behandeln kann, bevor die Blob Restore-Richtlinie aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="f9dbd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9dbd-116">PARAMETERS</span></span>

### <span data-ttu-id="f9dbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dbd-117">-DefaultProfile</span></span>
<span data-ttu-id="f9dbd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9dbd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9dbd-119">-PassThru</span></span>
<span data-ttu-id="f9dbd-120">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f9dbd-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f9dbd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dbd-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9dbd-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9dbd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9dbd-123">-ResourceId</span></span>
<span data-ttu-id="f9dbd-124">Geben Sie die Ressourcen-ID eines Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f9dbd-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="f9dbd-125">-RestoreDays</span></span>
<span data-ttu-id="f9dbd-126">Legt die Anzahl der Tage fest, für die das BLOB wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="f9dbd-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9dbd-127">-StorageAccount</span></span>
<span data-ttu-id="f9dbd-128">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="f9dbd-128">Storage account object</span></span>

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

### <span data-ttu-id="f9dbd-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9dbd-129">-StorageAccountName</span></span>
<span data-ttu-id="f9dbd-130">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="f9dbd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9dbd-131">-Confirm</span></span>
<span data-ttu-id="f9dbd-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9dbd-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f9dbd-133">-WhatIf</span></span>
<span data-ttu-id="f9dbd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9dbd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9dbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dbd-136">CommonParameters</span></span>
<span data-ttu-id="f9dbd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dbd-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9dbd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dbd-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9dbd-139">INPUTS</span></span>

### <span data-ttu-id="f9dbd-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9dbd-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f9dbd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f9dbd-141">System.String</span></span>

## <span data-ttu-id="f9dbd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9dbd-142">OUTPUTS</span></span>

### <span data-ttu-id="f9dbd-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f9dbd-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="f9dbd-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f9dbd-144">NOTES</span></span>

## <span data-ttu-id="f9dbd-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f9dbd-145">RELATED LINKS</span></span>
