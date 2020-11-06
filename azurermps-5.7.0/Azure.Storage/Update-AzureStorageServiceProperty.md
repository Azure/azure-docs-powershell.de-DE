---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501578"
---
# <span data-ttu-id="59fc1-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="59fc1-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="59fc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="59fc1-103">Ändert die Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="59fc1-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59fc1-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="59fc1-106">Das Cmdlet **Update-AzureStorageServiceProperty** ändert die Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="59fc1-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="59fc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="59fc1-108">Beispiel 1: Einrichten des BLOB-Diensts DefaultServiceVersion auf 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="59fc1-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="59fc1-109">Dieser Befehl legt die DefaultServiceVersion des BLOB-Diensts auf 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="59fc1-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="59fc1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="59fc1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="59fc1-111">-Context</span></span>
<span data-ttu-id="59fc1-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="59fc1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="59fc1-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="59fc1-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc1-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="59fc1-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="59fc1-115">DefaultServiceVersion gibt die Standard Version an, die für Anforderungen an den BLOB-Dienst verwendet werden soll, wenn die Version einer eingehenden Anforderung nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="59fc1-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="59fc1-116">Mögliche Werte sind Version 2008-10-27 und alle neueren Versionen.</span><span class="sxs-lookup"><span data-stu-id="59fc1-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="59fc1-117">Weitere Details finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="59fc1-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59fc1-118">-PassThru</span></span>
<span data-ttu-id="59fc1-119">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="59fc1-119">Display ServiceProperties</span></span>

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

### <span data-ttu-id="59fc1-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="59fc1-120">-ServiceType</span></span>
<span data-ttu-id="59fc1-121">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="59fc1-121">Specifies the storage service type.</span></span>
<span data-ttu-id="59fc1-122">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="59fc1-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="59fc1-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="59fc1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59fc1-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="59fc1-124">Blob</span></span> 
- <span data-ttu-id="59fc1-125">Tabelle</span><span class="sxs-lookup"><span data-stu-id="59fc1-125">Table</span></span>
- <span data-ttu-id="59fc1-126">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="59fc1-126">Queue</span></span>
- <span data-ttu-id="59fc1-127">Datei</span><span class="sxs-lookup"><span data-stu-id="59fc1-127">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc1-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59fc1-128">-Confirm</span></span>
<span data-ttu-id="59fc1-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59fc1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fc1-130">-WhatIf</span></span>
<span data-ttu-id="59fc1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59fc1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59fc1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59fc1-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fc1-133">CommonParameters</span></span>
<span data-ttu-id="59fc1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fc1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fc1-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fc1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fc1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59fc1-136">INPUTS</span></span>

### <span data-ttu-id="59fc1-137">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59fc1-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59fc1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59fc1-138">OUTPUTS</span></span>

### <span data-ttu-id="59fc1-139">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="59fc1-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="59fc1-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="59fc1-140">NOTES</span></span>

## <span data-ttu-id="59fc1-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59fc1-141">RELATED LINKS</span></span>

