---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: ff7ac13080d3d5cb717cf7efbff322cabf83cc3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481005"
---
# <span data-ttu-id="8f2ca-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="8f2ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2ca-103">Importiert Daten aus BLOB-Dateien in den Azure-Cache mit einem anderen Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f2ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f2ca-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f2ca-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2ca-106">Mit dem Cmdlet " **Import-AzureRmRedisCache** " werden Daten aus BLOBs in den Azure-a-a-Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="8f2ca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f2ca-107">EXAMPLES</span></span>

### <span data-ttu-id="8f2ca-108">Beispiel 1: Importieren von Daten</span><span class="sxs-lookup"><span data-stu-id="8f2ca-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="8f2ca-109">Dieser Befehl importiert Daten aus dem BLOB, das von der SAS-URL in Azure-a-a-Cache festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="8f2ca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f2ca-110">PARAMETERS</span></span>

### <span data-ttu-id="8f2ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2ca-111">-DefaultProfile</span></span>
<span data-ttu-id="8f2ca-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-113">-Dateien</span><span class="sxs-lookup"><span data-stu-id="8f2ca-113">-Files</span></span>
<span data-ttu-id="8f2ca-114">Gibt die SAS-URLs von BLOBs an, deren Inhalt dieses Cmdlet in den Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="8f2ca-115">Sie können die SAS-URLs mithilfe der folgenden PowerShell-Befehle generieren:</span><span class="sxs-lookup"><span data-stu-id="8f2ca-115">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="8f2ca-116">$storageAccountContext = New-AzureStorageContext-StorageAccountName "Speichername"-StorageAccountKey "Schlüssel"</span><span class="sxs-lookup"><span data-stu-id="8f2ca-116">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="8f2ca-117">$sasKeyForBlob = New-AzureStorageBlobSASToken-Container "Containername"-BLOB "blobname"-Berechtigung "rwdl"-Startzeit ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Kontext $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="8f2ca-117">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="8f2ca-118">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cachename"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="8f2ca-118">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8f2ca-119">-Force</span></span>
<span data-ttu-id="8f2ca-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-121">-Format</span><span class="sxs-lookup"><span data-stu-id="8f2ca-121">-Format</span></span>
<span data-ttu-id="8f2ca-122">Gibt das Format des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-122">Specifies the format of the blob.</span></span>
<span data-ttu-id="8f2ca-123">Derzeit ist RDB das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-123">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8f2ca-124">-Name</span></span>
<span data-ttu-id="8f2ca-125">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-125">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f2ca-126">-PassThru</span></span>
<span data-ttu-id="8f2ca-127">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-127">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="8f2ca-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2ca-129">-ResourceGroupName</span></span>
<span data-ttu-id="8f2ca-130">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f2ca-131">-Confirm</span></span>
<span data-ttu-id="8f2ca-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2ca-133">-WhatIf</span></span>
<span data-ttu-id="8f2ca-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2ca-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2ca-136">CommonParameters</span></span>
<span data-ttu-id="8f2ca-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2ca-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2ca-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f2ca-139">INPUTS</span></span>

### <span data-ttu-id="8f2ca-140">Keine</span><span class="sxs-lookup"><span data-stu-id="8f2ca-140">None</span></span>
<span data-ttu-id="8f2ca-141">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="8f2ca-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="8f2ca-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f2ca-142">OUTPUTS</span></span>

### <span data-ttu-id="8f2ca-143">Keine</span><span class="sxs-lookup"><span data-stu-id="8f2ca-143">None</span></span>

## <span data-ttu-id="8f2ca-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f2ca-144">NOTES</span></span>
* <span data-ttu-id="8f2ca-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="8f2ca-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8f2ca-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f2ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="8f2ca-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="8f2ca-148">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="8f2ca-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="8f2ca-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="8f2ca-151">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8f2ca-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


