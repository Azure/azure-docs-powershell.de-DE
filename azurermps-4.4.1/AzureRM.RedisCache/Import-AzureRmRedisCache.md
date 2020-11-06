---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 792a76d024b34dd90fd8818303c61daafeb4f46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481666"
---
# <span data-ttu-id="0f820-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="0f820-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f820-102">SYNOPSIS</span></span>
<span data-ttu-id="0f820-103">Importiert Daten aus BLOB-Dateien in den Azure-Cache mit einem anderen Speicher.</span><span class="sxs-lookup"><span data-stu-id="0f820-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f820-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f820-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f820-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f820-105">DESCRIPTION</span></span>
<span data-ttu-id="0f820-106">Mit dem Cmdlet " **Import-AzureRmRedisCache** " werden Daten aus BLOBs in den Azure-a-a-Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="0f820-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="0f820-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f820-107">EXAMPLES</span></span>

### <span data-ttu-id="0f820-108">Beispiel 1: Importieren von Daten</span><span class="sxs-lookup"><span data-stu-id="0f820-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="0f820-109">Dieser Befehl importiert Daten aus dem BLOB, das von der SAS-URL in Azure-a-a-Cache festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0f820-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="0f820-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f820-110">PARAMETERS</span></span>

### <span data-ttu-id="0f820-111">-Dateien</span><span class="sxs-lookup"><span data-stu-id="0f820-111">-Files</span></span>
<span data-ttu-id="0f820-112">Gibt die SAS-URLs von BLOBs an, deren Inhalt dieses Cmdlet in den Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="0f820-112">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="0f820-113">Sie können die SAS-URLs mithilfe der folgenden PowerShell-Befehle generieren:</span><span class="sxs-lookup"><span data-stu-id="0f820-113">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="0f820-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "Speichername"-StorageAccountKey "Schlüssel"</span><span class="sxs-lookup"><span data-stu-id="0f820-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="0f820-115">$sasKeyForBlob = New-AzureStorageBlobSASToken-Container "Containername"-BLOB "blobname"-Berechtigung "rwdl"-Startzeit ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Kontext $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="0f820-115">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="0f820-116">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cachename"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="0f820-116">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="0f820-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f820-117">-Force</span></span>
<span data-ttu-id="0f820-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0f820-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f820-119">-Format</span><span class="sxs-lookup"><span data-stu-id="0f820-119">-Format</span></span>
<span data-ttu-id="0f820-120">Gibt das Format des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="0f820-120">Specifies the format of the blob.</span></span>
<span data-ttu-id="0f820-121">Derzeit ist RDB das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="0f820-121">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="0f820-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f820-122">-Name</span></span>
<span data-ttu-id="0f820-123">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="0f820-123">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="0f820-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f820-124">-PassThru</span></span>
<span data-ttu-id="0f820-125">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f820-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="0f820-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0f820-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f820-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f820-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f820-128">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="0f820-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="0f820-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f820-129">-Confirm</span></span>
<span data-ttu-id="0f820-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f820-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f820-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f820-131">-WhatIf</span></span>
<span data-ttu-id="0f820-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f820-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f820-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f820-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f820-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f820-134">-DefaultProfile</span></span>
<span data-ttu-id="0f820-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f820-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f820-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f820-136">CommonParameters</span></span>
<span data-ttu-id="0f820-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f820-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f820-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f820-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f820-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f820-139">INPUTS</span></span>

### <span data-ttu-id="0f820-140">Keine</span><span class="sxs-lookup"><span data-stu-id="0f820-140">None</span></span>
<span data-ttu-id="0f820-141">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f820-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0f820-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f820-142">OUTPUTS</span></span>

### <span data-ttu-id="0f820-143">Keine</span><span class="sxs-lookup"><span data-stu-id="0f820-143">None</span></span>

## <span data-ttu-id="0f820-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f820-144">NOTES</span></span>
* <span data-ttu-id="0f820-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="0f820-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0f820-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f820-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f820-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="0f820-148">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0f820-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="0f820-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="0f820-151">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0f820-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


