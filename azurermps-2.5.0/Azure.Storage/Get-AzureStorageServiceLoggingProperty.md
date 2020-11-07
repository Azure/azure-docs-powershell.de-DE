---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848572"
---
# <span data-ttu-id="4e0e9-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4e0e9-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="4e0e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0e9-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e0e9-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e0e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0e9-106">Das Cmdlet " **Get-AzureStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="4e0e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="4e0e9-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="4e0e9-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="4e0e9-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="4e0e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e0e9-110">PARAMETERS</span></span>

### <span data-ttu-id="4e0e9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4e0e9-111">-Context</span></span>
<span data-ttu-id="4e0e9-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e0e9-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4e0e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0e9-114">-DefaultProfile</span></span>
<span data-ttu-id="4e0e9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e0e9-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4e0e9-116">-ServiceType</span></span>
<span data-ttu-id="4e0e9-117">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-117">Specifies the storage service type.</span></span>
<span data-ttu-id="4e0e9-118">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4e0e9-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e0e9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e0e9-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="4e0e9-120">Blob</span></span> 
- <span data-ttu-id="4e0e9-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="4e0e9-121">Table</span></span>
- <span data-ttu-id="4e0e9-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4e0e9-122">Queue</span></span>
- <span data-ttu-id="4e0e9-123">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4e0e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0e9-124">CommonParameters</span></span>
<span data-ttu-id="4e0e9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0e9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0e9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e0e9-127">INPUTS</span></span>

### <span data-ttu-id="4e0e9-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e0e9-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e0e9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e0e9-129">OUTPUTS</span></span>

### <span data-ttu-id="4e0e9-130">Microsoft. WindowsAzure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="4e0e9-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="4e0e9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e0e9-131">NOTES</span></span>

## <span data-ttu-id="4e0e9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e0e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e0e9-133">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e0e9-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4e0e9-134">Satz-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4e0e9-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


