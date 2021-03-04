---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d956dfd49e541751003d28c31285722616ab640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942048"
---
# <span data-ttu-id="560b8-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="560b8-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="560b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="560b8-102">SYNOPSIS</span></span>
<span data-ttu-id="560b8-103">Ruft Protokolleigenschaften für Azure Storage-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="560b8-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="560b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="560b8-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="560b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="560b8-105">DESCRIPTION</span></span>
<span data-ttu-id="560b8-106">Das **Get-AzStorageServiceLoggingProperty-Cmdlet** ruft Protokolleigenschaften für Azure Storage-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="560b8-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="560b8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="560b8-107">EXAMPLES</span></span>

### <span data-ttu-id="560b8-108">Beispiel 1: Protokollierungseigenschaften für den Blobdienst erhalten</span><span class="sxs-lookup"><span data-stu-id="560b8-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="560b8-109">Dieser Befehl ruft Protokolleigenschaften für den Blobspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="560b8-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="560b8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="560b8-110">PARAMETERS</span></span>

### <span data-ttu-id="560b8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="560b8-111">-Context</span></span>
<span data-ttu-id="560b8-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="560b8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="560b8-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="560b8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="560b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560b8-114">-DefaultProfile</span></span>
<span data-ttu-id="560b8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="560b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="560b8-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="560b8-116">-ServiceType</span></span>
<span data-ttu-id="560b8-117">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="560b8-117">Specifies the storage service type.</span></span>
<span data-ttu-id="560b8-118">Dieses Cmdlet ruft die Protokollierungseigenschaften für den Diensttyp ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="560b8-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="560b8-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="560b8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="560b8-120">Blob</span><span class="sxs-lookup"><span data-stu-id="560b8-120">Blob</span></span> 
- <span data-ttu-id="560b8-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="560b8-121">Table</span></span>
- <span data-ttu-id="560b8-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="560b8-122">Queue</span></span>
- <span data-ttu-id="560b8-123">Datei Der Wert von Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="560b8-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="560b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560b8-124">CommonParameters</span></span>
<span data-ttu-id="560b8-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560b8-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560b8-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="560b8-127">INPUTS</span></span>

### <span data-ttu-id="560b8-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="560b8-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="560b8-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="560b8-129">OUTPUTS</span></span>

### <span data-ttu-id="560b8-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="560b8-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="560b8-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="560b8-131">NOTES</span></span>

## <span data-ttu-id="560b8-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="560b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="560b8-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="560b8-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="560b8-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="560b8-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


