---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459660"
---
# <span data-ttu-id="51952-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="51952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51952-102">SYNOPSIS</span></span>
<span data-ttu-id="51952-103">Importiert Daten aus BLOBS in den Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="51952-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="51952-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51952-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51952-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51952-105">DESCRIPTION</span></span>
<span data-ttu-id="51952-106">Das **Cmdlet "Import-AzRedisCache"** importiert Daten aus BLOBS in den Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="51952-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="51952-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51952-107">EXAMPLES</span></span>

### <span data-ttu-id="51952-108">Beispiel 1: Importieren von Daten</span><span class="sxs-lookup"><span data-stu-id="51952-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="51952-109">Mit diesem Befehl werden Daten aus dem BLOB, das durch die SAS-URL angegeben wird, in den Azure Redis Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="51952-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="51952-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51952-110">PARAMETERS</span></span>

### <span data-ttu-id="51952-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51952-111">-DefaultProfile</span></span>
<span data-ttu-id="51952-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51952-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51952-113">-Files</span><span class="sxs-lookup"><span data-stu-id="51952-113">-Files</span></span>
<span data-ttu-id="51952-114">Gibt die SAS-URLs von BLOBS an, deren Inhalt dieses Cmdlet in den Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="51952-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="51952-115">Sie können die SAS-URLs mithilfe der folgenden PowerShell-Befehle generieren: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]:Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="51952-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="51952-116">-Force</span><span class="sxs-lookup"><span data-stu-id="51952-116">-Force</span></span>
<span data-ttu-id="51952-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="51952-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51952-118">-Format</span><span class="sxs-lookup"><span data-stu-id="51952-118">-Format</span></span>
<span data-ttu-id="51952-119">Gibt das Format des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="51952-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="51952-120">Rdb ist derzeit das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="51952-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="51952-121">-Name</span><span class="sxs-lookup"><span data-stu-id="51952-121">-Name</span></span>
<span data-ttu-id="51952-122">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="51952-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="51952-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51952-123">-PassThru</span></span>
<span data-ttu-id="51952-124">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="51952-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="51952-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="51952-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51952-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51952-126">-ResourceGroupName</span></span>
<span data-ttu-id="51952-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="51952-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="51952-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51952-128">-Confirm</span></span>
<span data-ttu-id="51952-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51952-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51952-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="51952-130">-WhatIf</span></span>
<span data-ttu-id="51952-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51952-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51952-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51952-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51952-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51952-133">CommonParameters</span></span>
<span data-ttu-id="51952-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51952-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51952-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51952-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51952-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51952-136">INPUTS</span></span>

### <span data-ttu-id="51952-137">System.String</span><span class="sxs-lookup"><span data-stu-id="51952-137">System.String</span></span>

### <span data-ttu-id="51952-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="51952-138">System.String[]</span></span>

## <span data-ttu-id="51952-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51952-139">OUTPUTS</span></span>

### <span data-ttu-id="51952-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51952-140">System.Boolean</span></span>

## <span data-ttu-id="51952-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51952-141">NOTES</span></span>
* <span data-ttu-id="51952-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="51952-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="51952-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51952-143">RELATED LINKS</span></span>

[<span data-ttu-id="51952-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="51952-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="51952-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="51952-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="51952-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51952-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


