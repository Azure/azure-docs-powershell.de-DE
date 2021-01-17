---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304192"
---
# <span data-ttu-id="c6f39-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c6f39-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="c6f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f39-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f39-103">Ruft Metrikeigenschaften für den Azure Storage-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="c6f39-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c6f39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6f39-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6f39-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f39-106">Das **Cmdlet "Get-AzStorageServiceMetricsProperty"** ruft Metrikeigenschaften für den Azure Storage Service ab.</span><span class="sxs-lookup"><span data-stu-id="c6f39-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c6f39-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6f39-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f39-108">Beispiel 1: Erhalten von Metrikeigenschaften für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="c6f39-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="c6f39-109">Dieser Befehl ruft Metrikeigenschaften für den BLOB-Speicher für den Metriktyp "Stunde" ab.</span><span class="sxs-lookup"><span data-stu-id="c6f39-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="c6f39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6f39-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f39-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c6f39-111">-Context</span></span>
<span data-ttu-id="c6f39-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c6f39-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c6f39-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6f39-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6f39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f39-114">-DefaultProfile</span></span>
<span data-ttu-id="c6f39-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6f39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f39-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="c6f39-116">-MetricsType</span></span>
<span data-ttu-id="c6f39-117">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="c6f39-117">Specifies a metrics type.</span></span>
<span data-ttu-id="c6f39-118">Dieses Cmdlet ruft die Metrikeigenschaften des Azure Storage Diensts für den von diesem Parameter angegebenen Metriktyp ab.</span><span class="sxs-lookup"><span data-stu-id="c6f39-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="c6f39-119">Die zulässigen Werte für diesen Parameter sind: "Hour" und "Minute".</span><span class="sxs-lookup"><span data-stu-id="c6f39-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="c6f39-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c6f39-120">-ServiceType</span></span>
<span data-ttu-id="c6f39-121">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="c6f39-121">Specifies the storage service type.</span></span>
<span data-ttu-id="c6f39-122">Dieses Cmdlet ruft die Metrikeigenschaften für den Typ ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c6f39-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="c6f39-123">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="c6f39-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6f39-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="c6f39-124">Blob</span></span> 
- <span data-ttu-id="c6f39-125">Tabelle</span><span class="sxs-lookup"><span data-stu-id="c6f39-125">Table</span></span>
- <span data-ttu-id="c6f39-126">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="c6f39-126">Queue</span></span>
- <span data-ttu-id="c6f39-127">Datei Der Wert von "Datei" wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f39-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c6f39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f39-128">CommonParameters</span></span>
<span data-ttu-id="c6f39-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f39-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f39-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f39-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6f39-131">INPUTS</span></span>

### <span data-ttu-id="c6f39-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6f39-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6f39-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6f39-133">OUTPUTS</span></span>

### <span data-ttu-id="c6f39-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="c6f39-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="c6f39-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6f39-135">NOTES</span></span>

## <span data-ttu-id="c6f39-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6f39-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6f39-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6f39-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c6f39-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c6f39-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


