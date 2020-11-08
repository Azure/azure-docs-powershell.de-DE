---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996986"
---
# <span data-ttu-id="e81c1-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e81c1-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e81c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e81c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e81c1-103">Ruft Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="e81c1-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="e81c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e81c1-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e81c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e81c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e81c1-106">Das Cmdlet " **Get-AzStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="e81c1-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="e81c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e81c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e81c1-108">Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="e81c1-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="e81c1-109">Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="e81c1-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="e81c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e81c1-110">PARAMETERS</span></span>

### <span data-ttu-id="e81c1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e81c1-111">-Context</span></span>
<span data-ttu-id="e81c1-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e81c1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e81c1-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e81c1-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e81c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81c1-114">-DefaultProfile</span></span>
<span data-ttu-id="e81c1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e81c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81c1-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e81c1-116">-ServiceType</span></span>
<span data-ttu-id="e81c1-117">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="e81c1-117">Specifies the storage service type.</span></span>
<span data-ttu-id="e81c1-118">Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e81c1-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e81c1-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e81c1-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e81c1-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="e81c1-120">Blob</span></span> 
- <span data-ttu-id="e81c1-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="e81c1-121">Table</span></span>
- <span data-ttu-id="e81c1-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e81c1-122">Queue</span></span>
- <span data-ttu-id="e81c1-123">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e81c1-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e81c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81c1-124">CommonParameters</span></span>
<span data-ttu-id="e81c1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81c1-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81c1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81c1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e81c1-127">INPUTS</span></span>

### <span data-ttu-id="e81c1-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e81c1-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e81c1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e81c1-129">OUTPUTS</span></span>

### <span data-ttu-id="e81c1-130">Microsoft. Azure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="e81c1-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e81c1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e81c1-131">NOTES</span></span>

## <span data-ttu-id="e81c1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e81c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="e81c1-133">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e81c1-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e81c1-134">Satz-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e81c1-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


