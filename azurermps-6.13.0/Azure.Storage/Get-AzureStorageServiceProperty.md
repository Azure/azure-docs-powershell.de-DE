---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: a36b1f13f08cd94339f9791512d764a872019672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498649"
---
# <span data-ttu-id="f351b-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f351b-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="f351b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f351b-102">SYNOPSIS</span></span>
<span data-ttu-id="f351b-103">Ruft Eigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="f351b-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f351b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f351b-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f351b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f351b-105">DESCRIPTION</span></span>
<span data-ttu-id="f351b-106">Mit dem Cmdlet **Get-AzureStorageServiceProperty werden** die Eigenschaften für Azure Storage Services abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f351b-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="f351b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f351b-107">EXAMPLES</span></span>

### <span data-ttu-id="f351b-108">Beispiel 1: Abrufen der Azure Storage Services-Eigenschaft des BLOB-Diensts</span><span class="sxs-lookup"><span data-stu-id="f351b-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="f351b-109">Dieser Befehl ruft die DefaultServiceVersion-Eigenschaft des BLOB-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="f351b-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="f351b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f351b-110">PARAMETERS</span></span>

### <span data-ttu-id="f351b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f351b-111">-Context</span></span>
<span data-ttu-id="f351b-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f351b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f351b-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f351b-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f351b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f351b-114">-DefaultProfile</span></span>
<span data-ttu-id="f351b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f351b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f351b-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f351b-116">-ServiceType</span></span>
<span data-ttu-id="f351b-117">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="f351b-117">Specifies the storage service type.</span></span>
<span data-ttu-id="f351b-118">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f351b-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f351b-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f351b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f351b-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="f351b-120">Blob</span></span> 
- <span data-ttu-id="f351b-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="f351b-121">Table</span></span>
- <span data-ttu-id="f351b-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f351b-122">Queue</span></span>
- <span data-ttu-id="f351b-123">Datei</span><span class="sxs-lookup"><span data-stu-id="f351b-123">File</span></span>

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

### <span data-ttu-id="f351b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f351b-124">CommonParameters</span></span>
<span data-ttu-id="f351b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f351b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f351b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f351b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f351b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f351b-127">INPUTS</span></span>

### <span data-ttu-id="f351b-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f351b-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f351b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f351b-129">OUTPUTS</span></span>

### <span data-ttu-id="f351b-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="f351b-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="f351b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f351b-131">NOTES</span></span>

## <span data-ttu-id="f351b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f351b-132">RELATED LINKS</span></span>
