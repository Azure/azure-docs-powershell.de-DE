---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 9d7e8f5d69d2f0e570cd7ce7fb21b29eb7f11648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496757"
---
# <span data-ttu-id="9bae5-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9bae5-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="9bae5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bae5-102">SYNOPSIS</span></span>
<span data-ttu-id="9bae5-103">Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="9bae5-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bae5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bae5-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9bae5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bae5-105">DESCRIPTION</span></span>
<span data-ttu-id="9bae5-106">Das Cmdlet " **Get-AzureStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="9bae5-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9bae5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bae5-107">EXAMPLES</span></span>

### <span data-ttu-id="9bae5-108">Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="9bae5-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="9bae5-109">Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="9bae5-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="9bae5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bae5-110">PARAMETERS</span></span>

### <span data-ttu-id="9bae5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9bae5-111">-Context</span></span>
<span data-ttu-id="9bae5-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9bae5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9bae5-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bae5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9bae5-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="9bae5-114">-MetricsType</span></span>
<span data-ttu-id="9bae5-115">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="9bae5-115">Specifies a metrics type.</span></span>
<span data-ttu-id="9bae5-116">Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9bae5-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="9bae5-117">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="9bae5-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bae5-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9bae5-118">-ServiceType</span></span>
<span data-ttu-id="9bae5-119">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9bae5-119">Specifies the storage service type.</span></span>
<span data-ttu-id="9bae5-120">Dieses Cmdlet ruft die Metrik-Eigenschaften für den Typ ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9bae5-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="9bae5-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9bae5-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bae5-122">BLOB</span><span class="sxs-lookup"><span data-stu-id="9bae5-122">Blob</span></span> 
- <span data-ttu-id="9bae5-123">Tabelle</span><span class="sxs-lookup"><span data-stu-id="9bae5-123">Table</span></span>
- <span data-ttu-id="9bae5-124">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9bae5-124">Queue</span></span>
- <span data-ttu-id="9bae5-125">Datei</span><span class="sxs-lookup"><span data-stu-id="9bae5-125">File</span></span> 

<span data-ttu-id="9bae5-126">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bae5-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="9bae5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bae5-127">CommonParameters</span></span>
<span data-ttu-id="9bae5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bae5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bae5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bae5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bae5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bae5-130">INPUTS</span></span>

### <span data-ttu-id="9bae5-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bae5-131">IStorageContext</span></span>

<span data-ttu-id="9bae5-132">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9bae5-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9bae5-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bae5-133">OUTPUTS</span></span>

### <span data-ttu-id="9bae5-134">Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="9bae5-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="9bae5-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bae5-135">NOTES</span></span>

## <span data-ttu-id="9bae5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bae5-136">RELATED LINKS</span></span>

[<span data-ttu-id="9bae5-137">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bae5-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9bae5-138">Satz-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9bae5-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


