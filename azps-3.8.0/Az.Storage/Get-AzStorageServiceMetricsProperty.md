---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996984"
---
# <span data-ttu-id="f0561-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f0561-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="f0561-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0561-102">SYNOPSIS</span></span>
<span data-ttu-id="f0561-103">Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="f0561-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f0561-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0561-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0561-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0561-105">DESCRIPTION</span></span>
<span data-ttu-id="f0561-106">Das Cmdlet " **Get-AzStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.</span><span class="sxs-lookup"><span data-stu-id="f0561-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f0561-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0561-107">EXAMPLES</span></span>

### <span data-ttu-id="f0561-108">Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="f0561-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="f0561-109">Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="f0561-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="f0561-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0561-110">PARAMETERS</span></span>

### <span data-ttu-id="f0561-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f0561-111">-Context</span></span>
<span data-ttu-id="f0561-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f0561-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f0561-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0561-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f0561-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0561-114">-DefaultProfile</span></span>
<span data-ttu-id="f0561-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0561-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0561-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="f0561-116">-MetricsType</span></span>
<span data-ttu-id="f0561-117">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="f0561-117">Specifies a metrics type.</span></span>
<span data-ttu-id="f0561-118">Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f0561-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="f0561-119">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="f0561-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="f0561-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f0561-120">-ServiceType</span></span>
<span data-ttu-id="f0561-121">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="f0561-121">Specifies the storage service type.</span></span>
<span data-ttu-id="f0561-122">Dieses Cmdlet ruft die Metrik-Eigenschaften für den Typ ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f0561-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="f0561-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f0561-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0561-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="f0561-124">Blob</span></span> 
- <span data-ttu-id="f0561-125">Tabelle</span><span class="sxs-lookup"><span data-stu-id="f0561-125">Table</span></span>
- <span data-ttu-id="f0561-126">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f0561-126">Queue</span></span>
- <span data-ttu-id="f0561-127">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0561-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="f0561-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0561-128">CommonParameters</span></span>
<span data-ttu-id="f0561-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0561-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0561-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0561-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0561-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0561-131">INPUTS</span></span>

### <span data-ttu-id="f0561-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0561-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f0561-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0561-133">OUTPUTS</span></span>

### <span data-ttu-id="f0561-134">Microsoft. Azure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="f0561-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="f0561-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0561-135">NOTES</span></span>

## <span data-ttu-id="f0561-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0561-136">RELATED LINKS</span></span>

[<span data-ttu-id="f0561-137">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0561-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f0561-138">Satz-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f0561-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


