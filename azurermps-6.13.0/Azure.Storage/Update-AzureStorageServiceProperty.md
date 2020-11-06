---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: b78d0fe26d689719427bf09e5e521ad1dbe0f425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476414"
---
# <span data-ttu-id="cb244-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb244-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="cb244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb244-102">SYNOPSIS</span></span>
<span data-ttu-id="cb244-103">Ändert die Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="cb244-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb244-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb244-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb244-105">DESCRIPTION</span></span>
<span data-ttu-id="cb244-106">Das Cmdlet **Update-AzureStorageServiceProperty** ändert die Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="cb244-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="cb244-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb244-107">EXAMPLES</span></span>

### <span data-ttu-id="cb244-108">Beispiel 1: Einrichten des BLOB-Diensts DefaultServiceVersion auf 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="cb244-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="cb244-109">Dieser Befehl legt die DefaultServiceVersion des BLOB-Diensts auf 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="cb244-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="cb244-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb244-110">PARAMETERS</span></span>

### <span data-ttu-id="cb244-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cb244-111">-Context</span></span>
<span data-ttu-id="cb244-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cb244-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cb244-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cb244-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb244-114">-DefaultProfile</span></span>
<span data-ttu-id="cb244-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb244-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb244-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="cb244-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="cb244-117">DefaultServiceVersion gibt die Standard Version an, die für Anforderungen an den BLOB-Dienst verwendet werden soll, wenn die Version einer eingehenden Anforderung nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cb244-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="cb244-118">Mögliche Werte sind Version 2008-10-27 und alle neueren Versionen.</span><span class="sxs-lookup"><span data-stu-id="cb244-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="cb244-119">Weitere Details finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="cb244-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb244-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb244-120">-PassThru</span></span>
<span data-ttu-id="cb244-121">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="cb244-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="cb244-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="cb244-122">-ServiceType</span></span>
<span data-ttu-id="cb244-123">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="cb244-123">Specifies the storage service type.</span></span>
<span data-ttu-id="cb244-124">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cb244-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="cb244-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cb244-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb244-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="cb244-126">Blob</span></span> 
- <span data-ttu-id="cb244-127">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cb244-127">Table</span></span>
- <span data-ttu-id="cb244-128">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="cb244-128">Queue</span></span>
- <span data-ttu-id="cb244-129">Datei</span><span class="sxs-lookup"><span data-stu-id="cb244-129">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb244-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb244-130">-Confirm</span></span>
<span data-ttu-id="cb244-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb244-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb244-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb244-132">-WhatIf</span></span>
<span data-ttu-id="cb244-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb244-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb244-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb244-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb244-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb244-135">CommonParameters</span></span>
<span data-ttu-id="cb244-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb244-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb244-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb244-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb244-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb244-138">INPUTS</span></span>

### <span data-ttu-id="cb244-139">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb244-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cb244-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb244-140">OUTPUTS</span></span>

### <span data-ttu-id="cb244-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="cb244-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="cb244-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb244-142">NOTES</span></span>

## <span data-ttu-id="cb244-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb244-143">RELATED LINKS</span></span>
