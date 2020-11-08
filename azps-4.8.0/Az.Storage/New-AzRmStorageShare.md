---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 81e380f6b6d4b1c35a6cff98093dfedf94119a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008795"
---
# <span data-ttu-id="415bf-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="415bf-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="415bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="415bf-102">SYNOPSIS</span></span>
<span data-ttu-id="415bf-103">Erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="415bf-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="415bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="415bf-104">SYNTAX</span></span>

### <span data-ttu-id="415bf-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="415bf-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="415bf-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="415bf-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="415bf-107">DESCRIPTION</span></span>
<span data-ttu-id="415bf-108">Das Cmdlet **New-AzRmStorageShare** erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="415bf-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="415bf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="415bf-109">EXAMPLES</span></span>

### <span data-ttu-id="415bf-110">Beispiel 1: Erstellen einer Speicherdatei Freigabe mit Speicherkonto Name und Freigabename, mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="415bf-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="415bf-111">Dieser Befehl erstellt eine Speicherdatei Freigabe mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="415bf-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="415bf-112">Beispiel 2: Erstellen einer Speicherdatei Freigabe mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="415bf-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="415bf-113">Dieser Befehl erstellt eine Speicherdatei Freigabe mit dem Speicherkonto Objekt und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="415bf-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="415bf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="415bf-114">PARAMETERS</span></span>

### <span data-ttu-id="415bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415bf-115">-DefaultProfile</span></span>
<span data-ttu-id="415bf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="415bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="415bf-117">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="415bf-117">-Metadata</span></span>
<span data-ttu-id="415bf-118">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="415bf-118">Share Metadata</span></span>

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

### <span data-ttu-id="415bf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="415bf-119">-Name</span></span>
<span data-ttu-id="415bf-120">Name der Azure-Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="415bf-120">Azure File share name</span></span>

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

### <span data-ttu-id="415bf-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="415bf-121">-QuotaGiB</span></span>
<span data-ttu-id="415bf-122">Freigabe Kontingent in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="415bf-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="415bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="415bf-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="415bf-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="415bf-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="415bf-125">-StorageAccount</span></span>
<span data-ttu-id="415bf-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="415bf-126">Storage account object</span></span>

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

### <span data-ttu-id="415bf-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="415bf-127">-StorageAccountName</span></span>
<span data-ttu-id="415bf-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="415bf-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="415bf-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="415bf-129">-Confirm</span></span>
<span data-ttu-id="415bf-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="415bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415bf-131">-WhatIf</span></span>
<span data-ttu-id="415bf-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="415bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415bf-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="415bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415bf-134">CommonParameters</span></span>
<span data-ttu-id="415bf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415bf-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415bf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415bf-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="415bf-137">INPUTS</span></span>

### <span data-ttu-id="415bf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="415bf-138">System.String</span></span>

### <span data-ttu-id="415bf-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="415bf-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="415bf-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="415bf-140">OUTPUTS</span></span>

### <span data-ttu-id="415bf-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="415bf-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="415bf-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="415bf-142">NOTES</span></span>

## <span data-ttu-id="415bf-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="415bf-143">RELATED LINKS</span></span>
