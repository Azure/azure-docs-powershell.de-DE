---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663648"
---
# <span data-ttu-id="ba71f-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="ba71f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba71f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba71f-103">Exportiert Daten aus Azure-a/a-Cache in einen Container.</span><span class="sxs-lookup"><span data-stu-id="ba71f-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba71f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba71f-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba71f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba71f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba71f-106">Mit dem Cmdlet " **Export-AzureRmRedisCache** " werden Daten aus Azure-a/a-Cache in einen Container exportiert.</span><span class="sxs-lookup"><span data-stu-id="ba71f-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="ba71f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba71f-107">EXAMPLES</span></span>

### <span data-ttu-id="ba71f-108">Beispiel 1: Exportieren von Daten</span><span class="sxs-lookup"><span data-stu-id="ba71f-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="ba71f-109">Dieser Befehl exportiert Daten aus einer Azure-Member-Cache-Instanz in den Container, der von der SAS-URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba71f-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="ba71f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba71f-110">PARAMETERS</span></span>

### <span data-ttu-id="ba71f-111">-Container</span><span class="sxs-lookup"><span data-stu-id="ba71f-111">-Container</span></span>
<span data-ttu-id="ba71f-112">Gibt die Dienst-SAS-URL des Containers an, in dem dieses Cmdlet Daten exportiert.</span><span class="sxs-lookup"><span data-stu-id="ba71f-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="ba71f-113">Sie können eine Dienst-SAS-URL mit den folgenden PowerShell-Befehlen generieren: $storageAccountContext = New-AzureStorageContext-StorageAccountName "Speicher Name"-StorageAccountKey "Schlüssel" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "Containername"-Berechtigung "rwdl"-Startzeit ([System. DateTime]:: jetzt). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-context $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cachename"-Präfix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="ba71f-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="ba71f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba71f-114">-DefaultProfile</span></span>
<span data-ttu-id="ba71f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba71f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba71f-116">-Format</span><span class="sxs-lookup"><span data-stu-id="ba71f-116">-Format</span></span>
<span data-ttu-id="ba71f-117">Gibt ein Format für das BLOB an.</span><span class="sxs-lookup"><span data-stu-id="ba71f-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="ba71f-118">Derzeit ist RDB das einzige unterstützte Format.</span><span class="sxs-lookup"><span data-stu-id="ba71f-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="ba71f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ba71f-119">-Name</span></span>
<span data-ttu-id="ba71f-120">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="ba71f-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ba71f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba71f-121">-PassThru</span></span>
<span data-ttu-id="ba71f-122">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba71f-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="ba71f-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ba71f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba71f-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ba71f-124">-Prefix</span></span>
<span data-ttu-id="ba71f-125">Gibt ein Präfix an, das für BLOB-Namen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba71f-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="ba71f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba71f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba71f-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="ba71f-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ba71f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba71f-128">-Confirm</span></span>
<span data-ttu-id="ba71f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba71f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba71f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba71f-130">-WhatIf</span></span>
<span data-ttu-id="ba71f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba71f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba71f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba71f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba71f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba71f-133">CommonParameters</span></span>
<span data-ttu-id="ba71f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba71f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba71f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba71f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba71f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba71f-136">INPUTS</span></span>

### <span data-ttu-id="ba71f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ba71f-137">System.String</span></span>

## <span data-ttu-id="ba71f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba71f-138">OUTPUTS</span></span>

### <span data-ttu-id="ba71f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba71f-139">System.Boolean</span></span>

## <span data-ttu-id="ba71f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba71f-140">NOTES</span></span>
* <span data-ttu-id="ba71f-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="ba71f-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ba71f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba71f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ba71f-143">Importieren-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="ba71f-144">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ba71f-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="ba71f-146">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="ba71f-147">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ba71f-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


