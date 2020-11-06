---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: fdd7a7c655b46eb3fc1ca8673fb8fb5f36dcd850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480717"
---
# <span data-ttu-id="fd7b9-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fd7b9-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="fd7b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7b9-103">Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd7b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7b9-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd7b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7b9-106">Das Cmdlet " **Get-AzureStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fd7b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd7b9-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7b9-108">Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="fd7b9-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="fd7b9-109">Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="fd7b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7b9-110">PARAMETERS</span></span>

### <span data-ttu-id="fd7b9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fd7b9-111">-Context</span></span>
<span data-ttu-id="fd7b9-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd7b9-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd7b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7b9-114">-DefaultProfile</span></span>
<span data-ttu-id="fd7b9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7b9-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="fd7b9-116">-MetricsType</span></span>
<span data-ttu-id="fd7b9-117">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-117">Specifies a metrics type.</span></span>
<span data-ttu-id="fd7b9-118">Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="fd7b9-119">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7b9-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fd7b9-120">-ServiceType</span></span>
<span data-ttu-id="fd7b9-121">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-121">Specifies the storage service type.</span></span>
<span data-ttu-id="fd7b9-122">Dieses Cmdlet ruft die Metrik-Eigenschaften für den Typ ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="fd7b9-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fd7b9-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd7b9-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="fd7b9-124">Blob</span></span> 
- <span data-ttu-id="fd7b9-125">Tabelle</span><span class="sxs-lookup"><span data-stu-id="fd7b9-125">Table</span></span>
- <span data-ttu-id="fd7b9-126">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="fd7b9-126">Queue</span></span>
- <span data-ttu-id="fd7b9-127">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="fd7b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7b9-128">CommonParameters</span></span>
<span data-ttu-id="fd7b9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7b9-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7b9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd7b9-131">INPUTS</span></span>

### <span data-ttu-id="fd7b9-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd7b9-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd7b9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd7b9-133">OUTPUTS</span></span>

### <span data-ttu-id="fd7b9-134">Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="fd7b9-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="fd7b9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd7b9-135">NOTES</span></span>

## <span data-ttu-id="fd7b9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd7b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd7b9-137">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd7b9-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fd7b9-138">Satz-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fd7b9-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


