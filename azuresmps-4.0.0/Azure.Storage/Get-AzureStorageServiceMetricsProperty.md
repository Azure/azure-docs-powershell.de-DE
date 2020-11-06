---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475661"
---
# <span data-ttu-id="22d1b-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="22d1b-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="22d1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="22d1b-103">Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="22d1b-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="22d1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d1b-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="22d1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="22d1b-106">Das Cmdlet " **Get-AzureStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="22d1b-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="22d1b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="22d1b-108">Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="22d1b-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="22d1b-109">Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="22d1b-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="22d1b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22d1b-110">PARAMETERS</span></span>

### <span data-ttu-id="22d1b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="22d1b-111">-Context</span></span>
<span data-ttu-id="22d1b-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="22d1b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="22d1b-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22d1b-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="22d1b-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="22d1b-114">-MetricsType</span></span>
<span data-ttu-id="22d1b-115">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="22d1b-115">Specifies a metrics type.</span></span>
<span data-ttu-id="22d1b-116">Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="22d1b-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="22d1b-117">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="22d1b-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="22d1b-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="22d1b-118">-ServiceType</span></span>
<span data-ttu-id="22d1b-119">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="22d1b-119">Specifies the storage service type.</span></span>
<span data-ttu-id="22d1b-120">Dieses Cmdlet ruft die Metrik-Eigenschaften für den Typ ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="22d1b-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="22d1b-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22d1b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22d1b-122">BLOB</span><span class="sxs-lookup"><span data-stu-id="22d1b-122">Blob</span></span> 
- <span data-ttu-id="22d1b-123">Tabelle</span><span class="sxs-lookup"><span data-stu-id="22d1b-123">Table</span></span>
- <span data-ttu-id="22d1b-124">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="22d1b-124">Queue</span></span>
- <span data-ttu-id="22d1b-125">Datei</span><span class="sxs-lookup"><span data-stu-id="22d1b-125">File</span></span> 

<span data-ttu-id="22d1b-126">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22d1b-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="22d1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d1b-127">CommonParameters</span></span>
<span data-ttu-id="22d1b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d1b-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d1b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d1b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22d1b-130">INPUTS</span></span>

## <span data-ttu-id="22d1b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22d1b-131">OUTPUTS</span></span>

## <span data-ttu-id="22d1b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="22d1b-132">NOTES</span></span>

## <span data-ttu-id="22d1b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22d1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="22d1b-134">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="22d1b-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="22d1b-135">Satz-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="22d1b-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


