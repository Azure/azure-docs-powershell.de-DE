---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301737"
---
# <span data-ttu-id="50fac-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50fac-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="50fac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50fac-102">SYNOPSIS</span></span>
<span data-ttu-id="50fac-103">Erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="50fac-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="50fac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50fac-104">SYNTAX</span></span>

### <span data-ttu-id="50fac-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="50fac-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fac-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="50fac-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50fac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50fac-107">DESCRIPTION</span></span>
<span data-ttu-id="50fac-108">Das Cmdlet **New-AzRmStorageShare** erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="50fac-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="50fac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50fac-109">EXAMPLES</span></span>

### <span data-ttu-id="50fac-110">Beispiel 1: Erstellen einer Speicherdatei Freigabe mit Speicherkonto Name und Freigabename, mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="50fac-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="50fac-111">Dieser Befehl erstellt eine Speicherdatei Freigabe mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="50fac-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="50fac-112">Beispiel 2: Erstellen einer Speicherdatei Freigabe mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="50fac-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="50fac-113">Dieser Befehl erstellt eine Speicherdatei Freigabe mit dem Speicherkonto Objekt und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="50fac-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="50fac-114">Beispiel 3: Erstellen einer Speicherdatei Freigabe mit accesstier als "heiß"</span><span class="sxs-lookup"><span data-stu-id="50fac-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="50fac-115">Mit diesem Befehl wird eine Speicherdatei Freigabe für accesstier als "heiß" erstellt.</span><span class="sxs-lookup"><span data-stu-id="50fac-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="50fac-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="50fac-116">PARAMETERS</span></span>

### <span data-ttu-id="50fac-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="50fac-117">-AccessTier</span></span>
<span data-ttu-id="50fac-118">Zugriffsebene für eine bestimmte Freigabe.</span><span class="sxs-lookup"><span data-stu-id="50fac-118">Access tier for specific share.</span></span> <span data-ttu-id="50fac-119">StorageV2-Konto kann zwischen TransactionOptimized (Standard), Hot und cool wählen.</span><span class="sxs-lookup"><span data-stu-id="50fac-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="50fac-120">Das FileStorage-Konto kann Premium wählen.</span><span class="sxs-lookup"><span data-stu-id="50fac-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="50fac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fac-121">-DefaultProfile</span></span>
<span data-ttu-id="50fac-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50fac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50fac-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="50fac-123">-Metadata</span></span>
<span data-ttu-id="50fac-124">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="50fac-124">Share Metadata</span></span>

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

### <span data-ttu-id="50fac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="50fac-125">-Name</span></span>
<span data-ttu-id="50fac-126">Name der Azure-Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="50fac-126">Azure File share name</span></span>

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

### <span data-ttu-id="50fac-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="50fac-127">-QuotaGiB</span></span>
<span data-ttu-id="50fac-128">Freigabe Kontingent in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="50fac-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="50fac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50fac-129">-ResourceGroupName</span></span>
<span data-ttu-id="50fac-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50fac-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="50fac-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="50fac-131">-StorageAccount</span></span>
<span data-ttu-id="50fac-132">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="50fac-132">Storage account object</span></span>

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

### <span data-ttu-id="50fac-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="50fac-133">-StorageAccountName</span></span>
<span data-ttu-id="50fac-134">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="50fac-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="50fac-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50fac-135">-Confirm</span></span>
<span data-ttu-id="50fac-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50fac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fac-137">-WhatIf</span></span>
<span data-ttu-id="50fac-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50fac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fac-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50fac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fac-140">CommonParameters</span></span>
<span data-ttu-id="50fac-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fac-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50fac-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fac-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50fac-143">INPUTS</span></span>

### <span data-ttu-id="50fac-144">System. String</span><span class="sxs-lookup"><span data-stu-id="50fac-144">System.String</span></span>

### <span data-ttu-id="50fac-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50fac-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="50fac-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50fac-146">OUTPUTS</span></span>

### <span data-ttu-id="50fac-147">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="50fac-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="50fac-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="50fac-148">NOTES</span></span>

## <span data-ttu-id="50fac-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50fac-149">RELATED LINKS</span></span>
