---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 34ea5ccc662514b3a2807924c932fb2e11b5b214
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943942"
---
# <span data-ttu-id="a0069-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="a0069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0069-102">SYNOPSIS</span></span>
<span data-ttu-id="a0069-103">Importiert Daten aus Blobs in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="a0069-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="a0069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0069-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0069-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0069-105">DESCRIPTION</span></span>
<span data-ttu-id="a0069-106">Das **Import-AzRedisCache-Cmdlet** importiert Daten aus Blobs in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="a0069-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="a0069-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0069-107">EXAMPLES</span></span>

### <span data-ttu-id="a0069-108">Beispiel 1: Importieren von Daten</span><span class="sxs-lookup"><span data-stu-id="a0069-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="a0069-109">Mit diesem Befehl werden Daten aus dem Blob importiert, der von der SAS-URL in Azure Redis Cache angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0069-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="a0069-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0069-110">PARAMETERS</span></span>

### <span data-ttu-id="a0069-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0069-111">-DefaultProfile</span></span>
<span data-ttu-id="a0069-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0069-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0069-113">-Dateien</span><span class="sxs-lookup"><span data-stu-id="a0069-113">-Files</span></span>
<span data-ttu-id="a0069-114">Gibt die SAS-URLs von Blobs an, deren Inhalt dieses Cmdlet in den Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="a0069-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="a0069-115">Sie können die SAS-URLs mithilfe der folgenden PowerShell-Befehle generieren: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="a0069-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a0069-116">-Force</span></span>
<span data-ttu-id="a0069-117">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="a0069-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0069-118">-Format</span><span class="sxs-lookup"><span data-stu-id="a0069-118">-Format</span></span>
<span data-ttu-id="a0069-119">Gibt das Format des Blobs an.</span><span class="sxs-lookup"><span data-stu-id="a0069-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="a0069-120">Derzeit ist rdb das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="a0069-120">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0069-121">-Name</span></span>
<span data-ttu-id="a0069-122">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="a0069-122">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0069-123">-PassThru</span></span>
<span data-ttu-id="a0069-124">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a0069-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="a0069-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a0069-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0069-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0069-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0069-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="a0069-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0069-128">-Confirm</span></span>
<span data-ttu-id="a0069-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0069-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0069-130">-WhatIf</span></span>
<span data-ttu-id="a0069-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0069-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0069-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0069-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0069-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0069-133">CommonParameters</span></span>
<span data-ttu-id="a0069-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0069-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0069-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0069-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0069-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0069-136">INPUTS</span></span>

### <span data-ttu-id="a0069-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a0069-137">System.String</span></span>

### <span data-ttu-id="a0069-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a0069-138">System.String[]</span></span>

## <span data-ttu-id="a0069-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0069-139">OUTPUTS</span></span>

### <span data-ttu-id="a0069-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0069-140">System.Boolean</span></span>

## <span data-ttu-id="a0069-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0069-141">NOTES</span></span>
* <span data-ttu-id="a0069-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="a0069-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a0069-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0069-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0069-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="a0069-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="a0069-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a0069-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="a0069-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0069-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


