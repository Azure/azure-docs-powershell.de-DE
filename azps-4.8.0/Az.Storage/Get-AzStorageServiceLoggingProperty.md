---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165483"
---
# <span data-ttu-id="19c9c-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="19c9c-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="19c9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="19c9c-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="19c9c-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="19c9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c9c-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="19c9c-106">Das Cmdlet " **Get-AzStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="19c9c-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="19c9c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="19c9c-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="19c9c-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="19c9c-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="19c9c-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="19c9c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="19c9c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="19c9c-111">-Context</span></span>
<span data-ttu-id="19c9c-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="19c9c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19c9c-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="19c9c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="19c9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c9c-114">-DefaultProfile</span></span>
<span data-ttu-id="19c9c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19c9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c9c-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="19c9c-116">-ServiceType</span></span>
<span data-ttu-id="19c9c-117">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="19c9c-117">Specifies the storage service type.</span></span>
<span data-ttu-id="19c9c-118">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="19c9c-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="19c9c-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="19c9c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19c9c-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="19c9c-120">Blob</span></span> 
- <span data-ttu-id="19c9c-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="19c9c-121">Table</span></span>
- <span data-ttu-id="19c9c-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="19c9c-122">Queue</span></span>
- <span data-ttu-id="19c9c-123">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19c9c-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="19c9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c9c-124">CommonParameters</span></span>
<span data-ttu-id="19c9c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c9c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c9c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c9c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19c9c-127">INPUTS</span></span>

### <span data-ttu-id="19c9c-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19c9c-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="19c9c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19c9c-129">OUTPUTS</span></span>

### <span data-ttu-id="19c9c-130">Microsoft. Azure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="19c9c-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="19c9c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="19c9c-131">NOTES</span></span>

## <span data-ttu-id="19c9c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19c9c-132">RELATED LINKS</span></span>

[<span data-ttu-id="19c9c-133">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19c9c-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="19c9c-134">Satz-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="19c9c-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


