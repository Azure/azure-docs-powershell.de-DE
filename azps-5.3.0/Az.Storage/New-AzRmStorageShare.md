---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467951"
---
# <span data-ttu-id="ae545-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ae545-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="ae545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae545-102">SYNOPSIS</span></span>
<span data-ttu-id="ae545-103">Erstellt eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="ae545-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="ae545-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae545-104">SYNTAX</span></span>

### <span data-ttu-id="ae545-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae545-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae545-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ae545-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae545-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae545-107">DESCRIPTION</span></span>
<span data-ttu-id="ae545-108">Das **Cmdlet "New-AzRmStorageShare"** erstellt eine Speicherdateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="ae545-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="ae545-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae545-109">EXAMPLES</span></span>

### <span data-ttu-id="ae545-110">Beispiel 1: Erstellen einer Speicherdateifreigabe mit dem Namen des Speicherkontos und dem Freigabenamen mit Metadaten und einem Freigabekontingent von 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="ae545-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ae545-111">Mit diesem Befehl wird eine Speicherdateifreigabe mit Metadaten und einem Freigabekontingent von 100 GIB erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae545-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="ae545-112">Beispiel 2: Erstellen einer Speicherdateifreigabe mit Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="ae545-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ae545-113">Mit diesem Befehl wird eine Speicherdateifreigabe mit dem Objekt "Speicherkonto" und dem Freigabenamen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae545-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ae545-114">Beispiel 3: Erstellen einer Speicherdateifreigabe mit "accesstier as Hot"</span><span class="sxs-lookup"><span data-stu-id="ae545-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="ae545-115">Mit diesem Befehl wird eine Speicherdateifreigabe mit "accesstier" als "Hot" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae545-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="ae545-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae545-116">PARAMETERS</span></span>

### <span data-ttu-id="ae545-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ae545-117">-AccessTier</span></span>
<span data-ttu-id="ae545-118">Zugriffsebene für bestimmte Freigaben.</span><span class="sxs-lookup"><span data-stu-id="ae545-118">Access tier for specific share.</span></span> <span data-ttu-id="ae545-119">Bei einem "StorageV2"-Konto kann zwischen TransactionOptimized (Standard), Hot und Cool ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ae545-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="ae545-120">"FileStorage"-Konto kann "Premium" auswählen.</span><span class="sxs-lookup"><span data-stu-id="ae545-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="ae545-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae545-121">-DefaultProfile</span></span>
<span data-ttu-id="ae545-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae545-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae545-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ae545-123">-Metadata</span></span>
<span data-ttu-id="ae545-124">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ae545-124">Share Metadata</span></span>

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

### <span data-ttu-id="ae545-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ae545-125">-Name</span></span>
<span data-ttu-id="ae545-126">Name der Azure-Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="ae545-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae545-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="ae545-127">-QuotaGiB</span></span>
<span data-ttu-id="ae545-128">Share Quota in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="ae545-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="ae545-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae545-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae545-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ae545-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae545-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae545-131">-StorageAccount</span></span>
<span data-ttu-id="ae545-132">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="ae545-132">Storage account object</span></span>

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

### <span data-ttu-id="ae545-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae545-133">-StorageAccountName</span></span>
<span data-ttu-id="ae545-134">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="ae545-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="ae545-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae545-135">-Confirm</span></span>
<span data-ttu-id="ae545-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae545-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae545-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae545-137">-WhatIf</span></span>
<span data-ttu-id="ae545-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae545-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae545-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae545-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae545-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae545-140">CommonParameters</span></span>
<span data-ttu-id="ae545-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae545-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae545-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae545-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae545-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae545-143">INPUTS</span></span>

### <span data-ttu-id="ae545-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ae545-144">System.String</span></span>

### <span data-ttu-id="ae545-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae545-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ae545-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae545-146">OUTPUTS</span></span>

### <span data-ttu-id="ae545-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="ae545-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ae545-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae545-148">NOTES</span></span>

## <span data-ttu-id="ae545-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae545-149">RELATED LINKS</span></span>
