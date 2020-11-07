---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662290"
---
# <span data-ttu-id="b05e2-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b05e2-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="b05e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b05e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b05e2-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="b05e2-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b05e2-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b05e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b05e2-105">DESCRIPTION</span></span>
<span data-ttu-id="b05e2-106">Das Cmdlet " **Get-AzureStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="b05e2-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="b05e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b05e2-107">EXAMPLES</span></span>

### <span data-ttu-id="b05e2-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="b05e2-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="b05e2-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="b05e2-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="b05e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b05e2-110">PARAMETERS</span></span>

### <span data-ttu-id="b05e2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b05e2-111">-Context</span></span>
<span data-ttu-id="b05e2-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b05e2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b05e2-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b05e2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b05e2-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b05e2-114">-ServiceType</span></span>
<span data-ttu-id="b05e2-115">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="b05e2-115">Specifies the storage service type.</span></span>
<span data-ttu-id="b05e2-116">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b05e2-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b05e2-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b05e2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b05e2-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="b05e2-118">Blob</span></span> 
- <span data-ttu-id="b05e2-119">Tabelle</span><span class="sxs-lookup"><span data-stu-id="b05e2-119">Table</span></span>
- <span data-ttu-id="b05e2-120">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="b05e2-120">Queue</span></span>
- <span data-ttu-id="b05e2-121">Datei</span><span class="sxs-lookup"><span data-stu-id="b05e2-121">File</span></span>

<span data-ttu-id="b05e2-122">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b05e2-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b05e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05e2-123">CommonParameters</span></span>
<span data-ttu-id="b05e2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05e2-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05e2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b05e2-126">INPUTS</span></span>

### <span data-ttu-id="b05e2-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b05e2-127">IStorageContext</span></span>

<span data-ttu-id="b05e2-128">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b05e2-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b05e2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b05e2-129">OUTPUTS</span></span>

### <span data-ttu-id="b05e2-130">Microsoft. WindowsAzure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="b05e2-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="b05e2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b05e2-131">NOTES</span></span>

## <span data-ttu-id="b05e2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b05e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="b05e2-133">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b05e2-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b05e2-134">Satz-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b05e2-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


