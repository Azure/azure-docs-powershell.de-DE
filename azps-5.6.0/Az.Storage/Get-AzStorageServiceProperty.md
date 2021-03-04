---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933307"
---
# <span data-ttu-id="17e8e-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="17e8e-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="17e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="17e8e-103">Ruft Eigenschaften für Azure Storage-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="17e8e-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="17e8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17e8e-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17e8e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="17e8e-106">Das **Get-AzStorageServiceProperty-Cmdlet** ruft die Eigenschaften für Azure Storage-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="17e8e-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="17e8e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="17e8e-108">Beispiel 1: Azure Storage Services-Eigenschaft des Blob-Diensts</span><span class="sxs-lookup"><span data-stu-id="17e8e-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="17e8e-109">Dieser Befehl ruft die DefaultServiceVersion-Eigenschaft des Blob-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="17e8e-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="17e8e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="17e8e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="17e8e-111">-Context</span></span>
<span data-ttu-id="17e8e-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="17e8e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="17e8e-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17e8e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="17e8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e8e-114">-DefaultProfile</span></span>
<span data-ttu-id="17e8e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17e8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e8e-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="17e8e-116">-ServiceType</span></span>
<span data-ttu-id="17e8e-117">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="17e8e-117">Specifies the storage service type.</span></span>
<span data-ttu-id="17e8e-118">Dieses Cmdlet ruft die Protokollierungseigenschaften für den Diensttyp ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="17e8e-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="17e8e-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="17e8e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17e8e-120">Blob</span><span class="sxs-lookup"><span data-stu-id="17e8e-120">Blob</span></span> 
- <span data-ttu-id="17e8e-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="17e8e-121">Table</span></span>
- <span data-ttu-id="17e8e-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="17e8e-122">Queue</span></span>
- <span data-ttu-id="17e8e-123">Datei</span><span class="sxs-lookup"><span data-stu-id="17e8e-123">File</span></span>

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

### <span data-ttu-id="17e8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e8e-124">CommonParameters</span></span>
<span data-ttu-id="17e8e-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e8e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e8e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e8e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17e8e-127">INPUTS</span></span>

### <span data-ttu-id="17e8e-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17e8e-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="17e8e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17e8e-129">OUTPUTS</span></span>

### <span data-ttu-id="17e8e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="17e8e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="17e8e-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17e8e-131">NOTES</span></span>

## <span data-ttu-id="17e8e-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17e8e-132">RELATED LINKS</span></span>
