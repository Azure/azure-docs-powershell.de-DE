---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 040e4e8584c29f77e6b847eea886851c41e606e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003353"
---
# <span data-ttu-id="5df76-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5df76-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="5df76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5df76-102">SYNOPSIS</span></span>
<span data-ttu-id="5df76-103">Erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="5df76-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="5df76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df76-104">SYNTAX</span></span>

### <span data-ttu-id="5df76-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="5df76-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5df76-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="5df76-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df76-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5df76-107">DESCRIPTION</span></span>
<span data-ttu-id="5df76-108">Das Cmdlet **New-AzRmStorageShare** erstellt eine Speicherdatei Freigabe.</span><span class="sxs-lookup"><span data-stu-id="5df76-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="5df76-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5df76-109">EXAMPLES</span></span>

### <span data-ttu-id="5df76-110">Beispiel 1: Erstellen einer Speicherdatei Freigabe mit Speicherkonto Name und Freigabename, mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="5df76-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="5df76-111">Dieser Befehl erstellt eine Speicherdatei Freigabe mit Metadaten und Freigabe Kontingent als 100 gib.</span><span class="sxs-lookup"><span data-stu-id="5df76-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="5df76-112">Beispiel 2: Erstellen einer Speicherdatei Freigabe mit dem Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="5df76-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="5df76-113">Dieser Befehl erstellt eine Speicherdatei Freigabe mit dem Speicherkonto Objekt und dem Freigabenamen.</span><span class="sxs-lookup"><span data-stu-id="5df76-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="5df76-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df76-114">PARAMETERS</span></span>

### <span data-ttu-id="5df76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df76-115">-DefaultProfile</span></span>
<span data-ttu-id="5df76-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5df76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df76-117">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="5df76-117">-Metadata</span></span>
<span data-ttu-id="5df76-118">Freigeben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="5df76-118">Share Metadata</span></span>

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

### <span data-ttu-id="5df76-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5df76-119">-Name</span></span>
<span data-ttu-id="5df76-120">Name der Azure-Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="5df76-120">Azure File share name</span></span>

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

### <span data-ttu-id="5df76-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="5df76-121">-QuotaGiB</span></span>
<span data-ttu-id="5df76-122">Freigabe Kontingent in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="5df76-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="5df76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df76-123">-ResourceGroupName</span></span>
<span data-ttu-id="5df76-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5df76-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="5df76-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5df76-125">-StorageAccount</span></span>
<span data-ttu-id="5df76-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="5df76-126">Storage account object</span></span>

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

### <span data-ttu-id="5df76-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5df76-127">-StorageAccountName</span></span>
<span data-ttu-id="5df76-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5df76-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="5df76-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5df76-129">-Confirm</span></span>
<span data-ttu-id="5df76-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5df76-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df76-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df76-131">-WhatIf</span></span>
<span data-ttu-id="5df76-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5df76-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df76-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5df76-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df76-134">CommonParameters</span></span>
<span data-ttu-id="5df76-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df76-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df76-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df76-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5df76-137">INPUTS</span></span>

### <span data-ttu-id="5df76-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5df76-138">System.String</span></span>

### <span data-ttu-id="5df76-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5df76-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5df76-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5df76-140">OUTPUTS</span></span>

### <span data-ttu-id="5df76-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="5df76-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5df76-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5df76-142">NOTES</span></span>

## <span data-ttu-id="5df76-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5df76-143">RELATED LINKS</span></span>
