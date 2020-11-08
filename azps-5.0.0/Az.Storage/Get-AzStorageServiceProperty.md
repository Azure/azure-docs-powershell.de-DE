---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176541"
---
# <span data-ttu-id="03ca0-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="03ca0-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="03ca0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="03ca0-103">Ruft Eigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="03ca0-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="03ca0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ca0-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ca0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="03ca0-106">Mit dem Cmdlet **Get-AzStorageServiceProperty werden** die Eigenschaften für Azure Storage Services abgerufen.</span><span class="sxs-lookup"><span data-stu-id="03ca0-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="03ca0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="03ca0-108">Beispiel 1: Abrufen der Azure Storage Services-Eigenschaft des BLOB-Diensts</span><span class="sxs-lookup"><span data-stu-id="03ca0-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="03ca0-109">Dieser Befehl ruft die DefaultServiceVersion-Eigenschaft des BLOB-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="03ca0-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="03ca0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ca0-110">PARAMETERS</span></span>

### <span data-ttu-id="03ca0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="03ca0-111">-Context</span></span>
<span data-ttu-id="03ca0-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="03ca0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="03ca0-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="03ca0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03ca0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ca0-114">-DefaultProfile</span></span>
<span data-ttu-id="03ca0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03ca0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ca0-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="03ca0-116">-ServiceType</span></span>
<span data-ttu-id="03ca0-117">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="03ca0-117">Specifies the storage service type.</span></span>
<span data-ttu-id="03ca0-118">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="03ca0-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="03ca0-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="03ca0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03ca0-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="03ca0-120">Blob</span></span> 
- <span data-ttu-id="03ca0-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="03ca0-121">Table</span></span>
- <span data-ttu-id="03ca0-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="03ca0-122">Queue</span></span>
- <span data-ttu-id="03ca0-123">Datei</span><span class="sxs-lookup"><span data-stu-id="03ca0-123">File</span></span>

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

### <span data-ttu-id="03ca0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ca0-124">CommonParameters</span></span>
<span data-ttu-id="03ca0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ca0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ca0-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ca0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ca0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03ca0-127">INPUTS</span></span>

### <span data-ttu-id="03ca0-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03ca0-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03ca0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03ca0-129">OUTPUTS</span></span>

### <span data-ttu-id="03ca0-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="03ca0-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="03ca0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="03ca0-131">NOTES</span></span>

## <span data-ttu-id="03ca0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03ca0-132">RELATED LINKS</span></span>
