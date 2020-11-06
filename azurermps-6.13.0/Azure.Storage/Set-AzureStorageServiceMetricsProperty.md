---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 1b32fbf01b22c365384190c6530a649a06664219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498589"
---
# <span data-ttu-id="c9b00-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c9b00-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="c9b00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9b00-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b00-103">Ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="c9b00-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9b00-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9b00-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b00-106">Das Cmdlet " **Satz-AzureStorageServiceMetricsProperty** " ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="c9b00-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c9b00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9b00-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b00-108">Beispiel 1: Ändern von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="c9b00-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c9b00-109">Mit diesem Befehl werden die Metriken der Version 1,0 für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="c9b00-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="c9b00-110">Für Azure Storage Service-Metriken werden die Einträge 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="c9b00-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="c9b00-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Metrik-Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c9b00-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="c9b00-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9b00-112">PARAMETERS</span></span>

### <span data-ttu-id="c9b00-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c9b00-113">-Context</span></span>
<span data-ttu-id="c9b00-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c9b00-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c9b00-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9b00-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c9b00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b00-116">-DefaultProfile</span></span>
<span data-ttu-id="c9b00-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9b00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b00-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="c9b00-118">-MetricsLevel</span></span>
<span data-ttu-id="c9b00-119">Gibt die metrikebene an, die der Azure-Speicher für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9b00-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="c9b00-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c9b00-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9b00-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c9b00-121">None</span></span>
- <span data-ttu-id="c9b00-122">Dienst</span><span class="sxs-lookup"><span data-stu-id="c9b00-122">Service</span></span>
- <span data-ttu-id="c9b00-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="c9b00-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b00-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="c9b00-124">-MetricsType</span></span>
<span data-ttu-id="c9b00-125">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="c9b00-125">Specifies a metrics type.</span></span>
<span data-ttu-id="c9b00-126">Mit diesem cmldet wird der Typ des Azure Storage Service-Metriken auf den Wert festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c9b00-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="c9b00-127">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="c9b00-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="c9b00-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9b00-128">-PassThru</span></span>
<span data-ttu-id="c9b00-129">Gibt an, dass diese Cmdlets die aktualisierten Metriken-Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9b00-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="c9b00-130">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c9b00-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b00-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c9b00-131">-RetentionDays</span></span>
<span data-ttu-id="c9b00-132">Gibt die Anzahl der Tage an, für die der Azure-Speicherdienst metrikinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="c9b00-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b00-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c9b00-133">-ServiceType</span></span>
<span data-ttu-id="c9b00-134">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="c9b00-134">Specifies the storage service type.</span></span>
<span data-ttu-id="c9b00-135">Mit diesem Cmdlet werden die Metriken-Eigenschaften für den Diensttyp geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c9b00-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c9b00-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c9b00-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9b00-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="c9b00-137">Blob</span></span> 
- <span data-ttu-id="c9b00-138">Tabelle</span><span class="sxs-lookup"><span data-stu-id="c9b00-138">Table</span></span>
- <span data-ttu-id="c9b00-139">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="c9b00-139">Queue</span></span>
- <span data-ttu-id="c9b00-140">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9b00-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c9b00-141">-Version</span><span class="sxs-lookup"><span data-stu-id="c9b00-141">-Version</span></span>
<span data-ttu-id="c9b00-142">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="c9b00-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="c9b00-143">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="c9b00-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b00-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b00-144">CommonParameters</span></span>
<span data-ttu-id="c9b00-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b00-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b00-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b00-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b00-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9b00-147">INPUTS</span></span>

### <span data-ttu-id="c9b00-148">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9b00-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c9b00-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9b00-149">OUTPUTS</span></span>

### <span data-ttu-id="c9b00-150">Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="c9b00-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="c9b00-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9b00-151">NOTES</span></span>

## <span data-ttu-id="c9b00-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9b00-152">RELATED LINKS</span></span>

[<span data-ttu-id="c9b00-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c9b00-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="c9b00-154">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9b00-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


