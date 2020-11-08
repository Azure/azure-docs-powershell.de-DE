---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007713"
---
# <span data-ttu-id="e9a4c-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9a4c-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="e9a4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a4c-103">Stellt eine gelöschte Dateifreigabe wieder her.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="e9a4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a4c-104">SYNTAX</span></span>

### <span data-ttu-id="e9a4c-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9a4c-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9a4c-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="e9a4c-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a4c-107">Freigebenobjekt</span><span class="sxs-lookup"><span data-stu-id="e9a4c-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9a4c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9a4c-108">DESCRIPTION</span></span>
<span data-ttu-id="e9a4c-109">Das Cmdlet **Restore-AzRmStorageShare** stellt eine gelöschte Dateifreigabe innerhalb einer gültigen Aufbewahrungstage wieder her, wenn die Option "Soft Delete freigeben" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="e9a4c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9a4c-110">EXAMPLES</span></span>

### <span data-ttu-id="e9a4c-111">Beispiel 1: entfernen und Wiederherstellen einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="e9a4c-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="e9a4c-112">Mit diesem Befehl Löschen Sie zunächst eine Dateifreigabe, Listen Freigaben auf und sehen die gelöschte Freigabeversion und stellen Sie schließlich wieder auf eine normale Freigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="e9a4c-113">Sie müssen die Freigabe von Soft Delete mit Update-AzStorageFileServiceProperty aktivieren, bevor Sie die Freigabe löschen.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="e9a4c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9a4c-114">PARAMETERS</span></span>

### <span data-ttu-id="e9a4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a4c-115">-DefaultProfile</span></span>
<span data-ttu-id="e9a4c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a4c-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="e9a4c-117">-DeletedShareVersion</span></span>
<span data-ttu-id="e9a4c-118">Gelöschte Freigabe Version, die von wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="e9a4c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9a4c-119">-InputObject</span></span>
<span data-ttu-id="e9a4c-120">Gelöschtes Freigabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e9a4c-120">Deleted Share object</span></span>

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

### <span data-ttu-id="e9a4c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a4c-121">-Name</span></span>
<span data-ttu-id="e9a4c-122">Gelöschter Freigabe Name, der wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="e9a4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9a4c-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9a4c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9a4c-125">-StorageAccount</span></span>
<span data-ttu-id="e9a4c-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="e9a4c-126">Storage account object</span></span>

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

### <span data-ttu-id="e9a4c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9a4c-127">-StorageAccountName</span></span>
<span data-ttu-id="e9a4c-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e9a4c-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="e9a4c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9a4c-129">-Confirm</span></span>
<span data-ttu-id="e9a4c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a4c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a4c-131">-WhatIf</span></span>
<span data-ttu-id="e9a4c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a4c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a4c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a4c-134">CommonParameters</span></span>
<span data-ttu-id="e9a4c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a4c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a4c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a4c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a4c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9a4c-137">INPUTS</span></span>

### <span data-ttu-id="e9a4c-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9a4c-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e9a4c-139">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="e9a4c-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e9a4c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9a4c-140">OUTPUTS</span></span>

### <span data-ttu-id="e9a4c-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="e9a4c-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e9a4c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9a4c-142">NOTES</span></span>

## <span data-ttu-id="e9a4c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9a4c-143">RELATED LINKS</span></span>
