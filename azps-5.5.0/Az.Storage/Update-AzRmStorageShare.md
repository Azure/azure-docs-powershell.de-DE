---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175017"
---
# <span data-ttu-id="51016-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="51016-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="51016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51016-102">SYNOPSIS</span></span>
<span data-ttu-id="51016-103">Ändert eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="51016-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="51016-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51016-104">SYNTAX</span></span>

### <span data-ttu-id="51016-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="51016-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51016-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="51016-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51016-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="51016-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51016-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="51016-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51016-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51016-109">DESCRIPTION</span></span>
<span data-ttu-id="51016-110">Das **Cmdlet "New-AzRmStorageShare"** ändert eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="51016-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="51016-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51016-111">EXAMPLES</span></span>

### <span data-ttu-id="51016-112">Beispiel 1: Ändert die Metadaten einer Speicherdateifreigabe und das Freigabekontingent mit dem Namen des Speicherkontos und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="51016-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="51016-113">Dieser Befehl ändert die Metadaten und das Freigabekontingent einer Speicherdatei mit dem Namen des Speicherkontos und dem Freigabenamen und zeigt das Änderungsergebnis mit dem zurückgegebenen Dateifreigabeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="51016-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="51016-114">Beispiel 2: Ändert Metadaten für eine Speicherdateifreigabe mit Speicherkontoobjekt und Freigabename</span><span class="sxs-lookup"><span data-stu-id="51016-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="51016-115">Mit diesem Befehl werden Die Metadaten einer Speicherdateifreigabe mit Speicherkontoobjekt und Freigabename geändert.</span><span class="sxs-lookup"><span data-stu-id="51016-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="51016-116">Beispiel 3: Ändert das Freigabekontingent für alle Speicherdateifreigaben in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="51016-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="51016-117">Mit diesem Befehl wird das Freigabekontingent für alle Speicherdateifreigaben in einem Speicherkonto mit Pipeline als 5.000 GIB geändert.</span><span class="sxs-lookup"><span data-stu-id="51016-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="51016-118">Beispiel 4: Ändern einer Speicherdateifreigabe mit "accesstier" als cool</span><span class="sxs-lookup"><span data-stu-id="51016-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="51016-119">Mit diesem Befehl wird eine Speicherdateifreigabe mit Accesstier als cool geändert.</span><span class="sxs-lookup"><span data-stu-id="51016-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="51016-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51016-120">PARAMETERS</span></span>

### <span data-ttu-id="51016-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="51016-121">-AccessTier</span></span>
<span data-ttu-id="51016-122">Zugriffsebene für bestimmte Freigaben.</span><span class="sxs-lookup"><span data-stu-id="51016-122">Access tier for specific share.</span></span> <span data-ttu-id="51016-123">Bei einem "StorageV2"-Konto kann zwischen TransactionOptimized (Standard), Hot und Cool ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="51016-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="51016-124">"FileStorage"-Konto kann "Premium" auswählen.</span><span class="sxs-lookup"><span data-stu-id="51016-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51016-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51016-125">-DefaultProfile</span></span>
<span data-ttu-id="51016-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51016-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51016-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51016-127">-InputObject</span></span>
<span data-ttu-id="51016-128">Speicherfreigabeobjekt</span><span class="sxs-lookup"><span data-stu-id="51016-128">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51016-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="51016-129">-Metadata</span></span>
<span data-ttu-id="51016-130">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="51016-130">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51016-131">-Name</span><span class="sxs-lookup"><span data-stu-id="51016-131">-Name</span></span>
<span data-ttu-id="51016-132">Freigabename</span><span class="sxs-lookup"><span data-stu-id="51016-132">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51016-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="51016-133">-QuotaGiB</span></span>
<span data-ttu-id="51016-134">Share Quota in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="51016-134">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51016-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51016-135">-ResourceGroupName</span></span>
<span data-ttu-id="51016-136">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="51016-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="51016-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51016-137">-ResourceId</span></span>
<span data-ttu-id="51016-138">Geben Sie eine Dateifreigaberessourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="51016-138">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51016-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="51016-139">-StorageAccount</span></span>
<span data-ttu-id="51016-140">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="51016-140">Storage account object</span></span>

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

### <span data-ttu-id="51016-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51016-141">-StorageAccountName</span></span>
<span data-ttu-id="51016-142">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="51016-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="51016-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51016-143">-Confirm</span></span>
<span data-ttu-id="51016-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51016-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51016-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="51016-145">-WhatIf</span></span>
<span data-ttu-id="51016-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51016-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51016-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51016-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51016-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51016-148">CommonParameters</span></span>
<span data-ttu-id="51016-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51016-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51016-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51016-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51016-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51016-151">INPUTS</span></span>

### <span data-ttu-id="51016-152">System.String</span><span class="sxs-lookup"><span data-stu-id="51016-152">System.String</span></span>

### <span data-ttu-id="51016-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51016-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="51016-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="51016-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="51016-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51016-155">OUTPUTS</span></span>

### <span data-ttu-id="51016-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="51016-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="51016-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51016-157">NOTES</span></span>

## <span data-ttu-id="51016-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51016-158">RELATED LINKS</span></span>
