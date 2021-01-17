---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303392"
---
# <span data-ttu-id="2434d-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2434d-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="2434d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2434d-102">SYNOPSIS</span></span>
<span data-ttu-id="2434d-103">Eine gelöschte Dateifreigabe wird wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="2434d-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="2434d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2434d-104">SYNTAX</span></span>

### <span data-ttu-id="2434d-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2434d-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2434d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2434d-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2434d-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="2434d-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2434d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2434d-108">DESCRIPTION</span></span>
<span data-ttu-id="2434d-109">Das **Cmdlet "Restore-AzRmStorageShare"** stellt eine gelöschte Dateifreigabe innerhalb eines gültigen Aufbewahrungstages wieder zurück, wenn das teilende weiche Löschen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2434d-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="2434d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2434d-110">EXAMPLES</span></span>

### <span data-ttu-id="2434d-111">Beispiel 1: Entfernen und Wiederherstellen einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="2434d-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="2434d-112">Mit diesem Befehl wird zuerst eine Dateifreigabe gelöscht, dann Freigaben auflistet, die gelöschte Freigabeversion angezeigt und schließlich wieder auf eine normale Freigabe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="2434d-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="2434d-113">Vor dem Löschen der Freigabe muss die weiche Löschfreigabe mit "Update-AzStorageFileServiceProperty" aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="2434d-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="2434d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2434d-114">PARAMETERS</span></span>

### <span data-ttu-id="2434d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2434d-115">-DefaultProfile</span></span>
<span data-ttu-id="2434d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2434d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2434d-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="2434d-117">-DeletedShareVersion</span></span>
<span data-ttu-id="2434d-118">"Freigabeversion" gelöscht, aus der wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2434d-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2434d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2434d-119">-InputObject</span></span>
<span data-ttu-id="2434d-120">Gelöschtes Freigabeobjekt</span><span class="sxs-lookup"><span data-stu-id="2434d-120">Deleted Share object</span></span>

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

### <span data-ttu-id="2434d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2434d-121">-Name</span></span>
<span data-ttu-id="2434d-122">Gelöschter Freigabename, der wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2434d-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="2434d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2434d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2434d-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2434d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2434d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2434d-125">-StorageAccount</span></span>
<span data-ttu-id="2434d-126">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="2434d-126">Storage account object</span></span>

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

### <span data-ttu-id="2434d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2434d-127">-StorageAccountName</span></span>
<span data-ttu-id="2434d-128">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="2434d-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="2434d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2434d-129">-Confirm</span></span>
<span data-ttu-id="2434d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2434d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2434d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2434d-131">-WhatIf</span></span>
<span data-ttu-id="2434d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2434d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2434d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2434d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2434d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2434d-134">CommonParameters</span></span>
<span data-ttu-id="2434d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2434d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2434d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2434d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2434d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2434d-137">INPUTS</span></span>

### <span data-ttu-id="2434d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2434d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2434d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="2434d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="2434d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2434d-140">OUTPUTS</span></span>

### <span data-ttu-id="2434d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="2434d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="2434d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2434d-142">NOTES</span></span>

## <span data-ttu-id="2434d-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2434d-143">RELATED LINKS</span></span>
