---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475666"
---
# <span data-ttu-id="ad8c3-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ad8c3-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ad8c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8c3-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ad8c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad8c3-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad8c3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ad8c3-106">Das Cmdlet " **Get-AzureStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ad8c3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ad8c3-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="ad8c3-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ad8c3-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ad8c3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="ad8c3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ad8c3-111">-Context</span></span>
<span data-ttu-id="ad8c3-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ad8c3-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ad8c3-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ad8c3-114">-ServiceType</span></span>
<span data-ttu-id="ad8c3-115">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-115">Specifies the storage service type.</span></span>
<span data-ttu-id="ad8c3-116">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ad8c3-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ad8c3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad8c3-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="ad8c3-118">Blob</span></span> 
- <span data-ttu-id="ad8c3-119">Tabelle</span><span class="sxs-lookup"><span data-stu-id="ad8c3-119">Table</span></span>
- <span data-ttu-id="ad8c3-120">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ad8c3-120">Queue</span></span>
- <span data-ttu-id="ad8c3-121">Datei</span><span class="sxs-lookup"><span data-stu-id="ad8c3-121">File</span></span>

<span data-ttu-id="ad8c3-122">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ad8c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8c3-123">CommonParameters</span></span>
<span data-ttu-id="ad8c3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad8c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8c3-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad8c3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8c3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad8c3-126">INPUTS</span></span>

## <span data-ttu-id="ad8c3-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad8c3-127">OUTPUTS</span></span>

## <span data-ttu-id="ad8c3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad8c3-128">NOTES</span></span>

## <span data-ttu-id="ad8c3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad8c3-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad8c3-130">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad8c3-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ad8c3-131">Satz-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ad8c3-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


