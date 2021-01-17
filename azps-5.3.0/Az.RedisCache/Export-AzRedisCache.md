---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459671"
---
# <span data-ttu-id="54d58-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="54d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d58-102">SYNOPSIS</span></span>
<span data-ttu-id="54d58-103">Exportiert Daten aus Azure Redis Cache in einen Container.</span><span class="sxs-lookup"><span data-stu-id="54d58-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="54d58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54d58-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54d58-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54d58-105">DESCRIPTION</span></span>
<span data-ttu-id="54d58-106">Das **Cmdlet "Export-AzRedisCache"** exportiert Daten aus dem Azure Redis Cache in einen Container.</span><span class="sxs-lookup"><span data-stu-id="54d58-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="54d58-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54d58-107">EXAMPLES</span></span>

### <span data-ttu-id="54d58-108">Beispiel 1: Exportieren von Daten</span><span class="sxs-lookup"><span data-stu-id="54d58-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="54d58-109">Mit diesem Befehl werden Daten aus einer Azure Redis-Cache-Instanz in den Container exportiert, der von der SAS-URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54d58-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="54d58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d58-110">PARAMETERS</span></span>

### <span data-ttu-id="54d58-111">-Container</span><span class="sxs-lookup"><span data-stu-id="54d58-111">-Container</span></span>
<span data-ttu-id="54d58-112">Gibt die DIENST-SAS-URL des Containers an, in den dieses Cmdlet Daten exportiert.</span><span class="sxs-lookup"><span data-stu-id="54d58-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="54d58-113">Sie können eine Dienst-SAS-URL mithilfe der folgenden PowerShell-Befehle generieren: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]:Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="54d58-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="54d58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d58-114">-DefaultProfile</span></span>
<span data-ttu-id="54d58-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54d58-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d58-116">-Format</span><span class="sxs-lookup"><span data-stu-id="54d58-116">-Format</span></span>
<span data-ttu-id="54d58-117">Gibt ein Format für das BLOB an.</span><span class="sxs-lookup"><span data-stu-id="54d58-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="54d58-118">Rdb ist derzeit das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="54d58-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="54d58-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54d58-119">-Name</span></span>
<span data-ttu-id="54d58-120">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="54d58-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="54d58-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d58-121">-PassThru</span></span>
<span data-ttu-id="54d58-122">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="54d58-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="54d58-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="54d58-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54d58-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="54d58-124">-Prefix</span></span>
<span data-ttu-id="54d58-125">Gibt ein Präfix an, das für BLOB-Namen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54d58-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="54d58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d58-126">-ResourceGroupName</span></span>
<span data-ttu-id="54d58-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="54d58-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="54d58-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54d58-128">-Confirm</span></span>
<span data-ttu-id="54d58-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54d58-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d58-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="54d58-130">-WhatIf</span></span>
<span data-ttu-id="54d58-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d58-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d58-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54d58-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d58-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d58-133">CommonParameters</span></span>
<span data-ttu-id="54d58-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d58-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d58-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d58-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d58-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54d58-136">INPUTS</span></span>

### <span data-ttu-id="54d58-137">System.String</span><span class="sxs-lookup"><span data-stu-id="54d58-137">System.String</span></span>

## <span data-ttu-id="54d58-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54d58-138">OUTPUTS</span></span>

### <span data-ttu-id="54d58-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54d58-139">System.Boolean</span></span>

## <span data-ttu-id="54d58-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54d58-140">NOTES</span></span>
* <span data-ttu-id="54d58-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="54d58-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="54d58-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54d58-142">RELATED LINKS</span></span>

[<span data-ttu-id="54d58-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="54d58-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="54d58-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="54d58-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="54d58-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="54d58-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


