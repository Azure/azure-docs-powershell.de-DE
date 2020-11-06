---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: d0edbcc3b519f9600a2ad36832dee0305ce49be7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481385"
---
# <span data-ttu-id="91cb5-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="91cb5-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="91cb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="91cb5-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="91cb5-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91cb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91cb5-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="91cb5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="91cb5-106">Das Cmdlet " **Get-AzureStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="91cb5-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="91cb5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="91cb5-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="91cb5-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="91cb5-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="91cb5-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="91cb5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91cb5-110">PARAMETERS</span></span>

### <span data-ttu-id="91cb5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="91cb5-111">-Context</span></span>
<span data-ttu-id="91cb5-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="91cb5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="91cb5-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91cb5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="91cb5-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="91cb5-114">-ServiceType</span></span>
<span data-ttu-id="91cb5-115">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="91cb5-115">Specifies the storage service type.</span></span>
<span data-ttu-id="91cb5-116">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="91cb5-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="91cb5-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91cb5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91cb5-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="91cb5-118">Blob</span></span> 
- <span data-ttu-id="91cb5-119">Tabelle</span><span class="sxs-lookup"><span data-stu-id="91cb5-119">Table</span></span>
- <span data-ttu-id="91cb5-120">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="91cb5-120">Queue</span></span>
- <span data-ttu-id="91cb5-121">Datei</span><span class="sxs-lookup"><span data-stu-id="91cb5-121">File</span></span>

<span data-ttu-id="91cb5-122">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91cb5-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="91cb5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cb5-123">CommonParameters</span></span>
<span data-ttu-id="91cb5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cb5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cb5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cb5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cb5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91cb5-126">INPUTS</span></span>

### <span data-ttu-id="91cb5-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="91cb5-127">IStorageContext</span></span>

<span data-ttu-id="91cb5-128">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="91cb5-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="91cb5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91cb5-129">OUTPUTS</span></span>

### <span data-ttu-id="91cb5-130">Microsoft. WindowsAzure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="91cb5-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="91cb5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="91cb5-131">NOTES</span></span>

## <span data-ttu-id="91cb5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91cb5-132">RELATED LINKS</span></span>

[<span data-ttu-id="91cb5-133">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="91cb5-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="91cb5-134">Satz-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="91cb5-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


