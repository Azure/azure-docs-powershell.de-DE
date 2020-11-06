---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496753"
---
# <span data-ttu-id="90a1c-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="90a1c-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="90a1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="90a1c-103">Ruft Eigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="90a1c-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90a1c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="90a1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="90a1c-106">Mit dem Cmdlet **Get-AzureStorageServiceProperty werden** die Eigenschaften für Azure Storage Services abgerufen.</span><span class="sxs-lookup"><span data-stu-id="90a1c-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="90a1c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="90a1c-108">Beispiel 1: Abrufen der Azure Storage Services-Eigenschaft des BLOB-Diensts</span><span class="sxs-lookup"><span data-stu-id="90a1c-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="90a1c-109">Dieser Befehl ruft die DefaultServiceVersion-Eigenschaft des BLOB-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="90a1c-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="90a1c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="90a1c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="90a1c-111">-Context</span></span>
<span data-ttu-id="90a1c-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="90a1c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90a1c-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90a1c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90a1c-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="90a1c-114">-ServiceType</span></span>
<span data-ttu-id="90a1c-115">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="90a1c-115">Specifies the storage service type.</span></span>
<span data-ttu-id="90a1c-116">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="90a1c-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="90a1c-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="90a1c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90a1c-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="90a1c-118">Blob</span></span> 
- <span data-ttu-id="90a1c-119">Tabelle</span><span class="sxs-lookup"><span data-stu-id="90a1c-119">Table</span></span>
- <span data-ttu-id="90a1c-120">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="90a1c-120">Queue</span></span>
- <span data-ttu-id="90a1c-121">Datei</span><span class="sxs-lookup"><span data-stu-id="90a1c-121">File</span></span>

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

### <span data-ttu-id="90a1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a1c-122">CommonParameters</span></span>
<span data-ttu-id="90a1c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a1c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a1c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a1c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90a1c-125">INPUTS</span></span>

### <span data-ttu-id="90a1c-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90a1c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90a1c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90a1c-127">OUTPUTS</span></span>

### <span data-ttu-id="90a1c-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="90a1c-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="90a1c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="90a1c-129">NOTES</span></span>

## <span data-ttu-id="90a1c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90a1c-130">RELATED LINKS</span></span>

