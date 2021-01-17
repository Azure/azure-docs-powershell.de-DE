---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471732"
---
# <span data-ttu-id="dfaff-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dfaff-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="dfaff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfaff-102">SYNOPSIS</span></span>
<span data-ttu-id="dfaff-103">Ruft Protokolleigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="dfaff-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="dfaff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfaff-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfaff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfaff-105">DESCRIPTION</span></span>
<span data-ttu-id="dfaff-106">Das **Cmdlet "Get-AzStorageServiceLoggingProperty"** ruft Protokolleigenschaften für Azure Storage Services ab.</span><span class="sxs-lookup"><span data-stu-id="dfaff-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="dfaff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfaff-107">EXAMPLES</span></span>

### <span data-ttu-id="dfaff-108">Beispiel 1: Protokollierungseigenschaften für den Blob Service erhalten</span><span class="sxs-lookup"><span data-stu-id="dfaff-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="dfaff-109">Dieser Befehl ruft Protokolleigenschaften für blob storage ab.</span><span class="sxs-lookup"><span data-stu-id="dfaff-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="dfaff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfaff-110">PARAMETERS</span></span>

### <span data-ttu-id="dfaff-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dfaff-111">-Context</span></span>
<span data-ttu-id="dfaff-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="dfaff-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dfaff-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfaff-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dfaff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfaff-114">-DefaultProfile</span></span>
<span data-ttu-id="dfaff-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfaff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfaff-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="dfaff-116">-ServiceType</span></span>
<span data-ttu-id="dfaff-117">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="dfaff-117">Specifies the storage service type.</span></span>
<span data-ttu-id="dfaff-118">Dieses Cmdlet ruft die Protokolleigenschaften für den Diensttyp ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="dfaff-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="dfaff-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="dfaff-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfaff-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="dfaff-120">Blob</span></span> 
- <span data-ttu-id="dfaff-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="dfaff-121">Table</span></span>
- <span data-ttu-id="dfaff-122">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="dfaff-122">Queue</span></span>
- <span data-ttu-id="dfaff-123">Datei Der Wert von "Datei" wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dfaff-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="dfaff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfaff-124">CommonParameters</span></span>
<span data-ttu-id="dfaff-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfaff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfaff-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfaff-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfaff-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfaff-127">INPUTS</span></span>

### <span data-ttu-id="dfaff-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dfaff-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dfaff-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfaff-129">OUTPUTS</span></span>

### <span data-ttu-id="dfaff-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="dfaff-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="dfaff-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dfaff-131">NOTES</span></span>

## <span data-ttu-id="dfaff-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dfaff-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfaff-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dfaff-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="dfaff-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dfaff-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


