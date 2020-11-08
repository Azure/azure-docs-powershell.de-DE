---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996194"
---
# <span data-ttu-id="fbfc9-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fbfc9-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="fbfc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfc9-103">Ändert eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="fbfc9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbfc9-104">SYNTAX</span></span>

### <span data-ttu-id="fbfc9-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbfc9-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbfc9-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="fbfc9-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfc9-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="fbfc9-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfc9-108">Freigebenobjekt</span><span class="sxs-lookup"><span data-stu-id="fbfc9-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbfc9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbfc9-109">DESCRIPTION</span></span>
<span data-ttu-id="fbfc9-110">Das Cmdlet **New-AzRmStorageShare** ändert eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="fbfc9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbfc9-111">EXAMPLES</span></span>

### <span data-ttu-id="fbfc9-112">Beispiel 1: ändert die Metadaten und das Freigabe Kontingent einer Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="fbfc9-113">Mit diesem Befehl werden die Metadaten und das Freigabe Kontingent einer Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen geändert, und das änderungsergebnis wird mit dem zurückgegebenen Dateifreigabe Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="fbfc9-114">Beispiel 2: ändert Metadaten für eine Speicherdatei Freigabe mit dem Speicherkonto Objekt und dem Freigabenamen</span><span class="sxs-lookup"><span data-stu-id="fbfc9-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="fbfc9-115">Dieser Befehl ändert Metadaten für eine Speicherdatei Freigabe mit dem Speicherkonto Objekt und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="fbfc9-116">Beispiel 3: ändert das Freigabe Kontingent für alle Speicherdatei Freigaben in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="fbfc9-117">Dieser Befehl ändert das Freigabe Kontingent als 5000 gib für alle Speicherdatei Freigaben in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fbfc9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbfc9-118">PARAMETERS</span></span>

### <span data-ttu-id="fbfc9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfc9-119">-DefaultProfile</span></span>
<span data-ttu-id="fbfc9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbfc9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fbfc9-121">-InputObject</span></span>
<span data-ttu-id="fbfc9-122">Speicherfreigabe Objekt</span><span class="sxs-lookup"><span data-stu-id="fbfc9-122">Storage Share object</span></span>

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

### <span data-ttu-id="fbfc9-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fbfc9-123">-Metadata</span></span>
<span data-ttu-id="fbfc9-124">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="fbfc9-124">Share Metadata</span></span>

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

### <span data-ttu-id="fbfc9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fbfc9-125">-Name</span></span>
<span data-ttu-id="fbfc9-126">Freigabe Name</span><span class="sxs-lookup"><span data-stu-id="fbfc9-126">Share Name</span></span>

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

### <span data-ttu-id="fbfc9-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="fbfc9-127">-QuotaGiB</span></span>
<span data-ttu-id="fbfc9-128">Freigabe Kontingent in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="fbfc9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfc9-129">-ResourceGroupName</span></span>
<span data-ttu-id="fbfc9-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="fbfc9-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fbfc9-131">-ResourceId</span></span>
<span data-ttu-id="fbfc9-132">Geben Sie eine Dateifreigabe-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="fbfc9-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbfc9-133">-StorageAccount</span></span>
<span data-ttu-id="fbfc9-134">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="fbfc9-134">Storage account object</span></span>

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

### <span data-ttu-id="fbfc9-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fbfc9-135">-StorageAccountName</span></span>
<span data-ttu-id="fbfc9-136">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fbfc9-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="fbfc9-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbfc9-137">-Confirm</span></span>
<span data-ttu-id="fbfc9-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbfc9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbfc9-139">-WhatIf</span></span>
<span data-ttu-id="fbfc9-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbfc9-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbfc9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfc9-142">CommonParameters</span></span>
<span data-ttu-id="fbfc9-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfc9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfc9-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfc9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfc9-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbfc9-145">INPUTS</span></span>

### <span data-ttu-id="fbfc9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fbfc9-146">System.String</span></span>

### <span data-ttu-id="fbfc9-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbfc9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fbfc9-148">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="fbfc9-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="fbfc9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbfc9-149">OUTPUTS</span></span>

### <span data-ttu-id="fbfc9-150">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="fbfc9-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="fbfc9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbfc9-151">NOTES</span></span>

## <span data-ttu-id="fbfc9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbfc9-152">RELATED LINKS</span></span>
