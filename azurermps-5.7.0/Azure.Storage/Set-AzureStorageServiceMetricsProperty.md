---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 3cbe0a4e0276f2b62a0e0aed5b6168a5b81f8d7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665220"
---
# <span data-ttu-id="cd57a-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cd57a-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="cd57a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd57a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd57a-103">Ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="cd57a-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd57a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd57a-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="cd57a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd57a-105">DESCRIPTION</span></span>
<span data-ttu-id="cd57a-106">Das Cmdlet " **Satz-AzureStorageServiceMetricsProperty** " ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="cd57a-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="cd57a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd57a-107">EXAMPLES</span></span>

### <span data-ttu-id="cd57a-108">Beispiel 1: Ändern von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="cd57a-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="cd57a-109">Mit diesem Befehl werden die Metriken der Version 1,0 für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="cd57a-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="cd57a-110">Für Azure Storage Service-Metriken werden die Einträge 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="cd57a-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="cd57a-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Metrik-Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="cd57a-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="cd57a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd57a-112">PARAMETERS</span></span>

### <span data-ttu-id="cd57a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="cd57a-113">-Context</span></span>
<span data-ttu-id="cd57a-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cd57a-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd57a-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd57a-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="cd57a-116">-MetricsLevel</span></span>
<span data-ttu-id="cd57a-117">Gibt die metrikebene an, die der Azure-Speicher für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd57a-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="cd57a-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd57a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd57a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="cd57a-119">None</span></span>
- <span data-ttu-id="cd57a-120">Dienst</span><span class="sxs-lookup"><span data-stu-id="cd57a-120">Service</span></span>
- <span data-ttu-id="cd57a-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="cd57a-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="cd57a-122">-MetricsType</span></span>
<span data-ttu-id="cd57a-123">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="cd57a-123">Specifies a metrics type.</span></span>
<span data-ttu-id="cd57a-124">Mit diesem cmldet wird der Typ des Azure Storage Service-Metriken auf den Wert festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cd57a-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="cd57a-125">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="cd57a-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd57a-126">-PassThru</span></span>
<span data-ttu-id="cd57a-127">Gibt an, dass diese Cmdlets die aktualisierten Metriken-Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cd57a-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="cd57a-128">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd57a-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="cd57a-129">-RetentionDays</span></span>
<span data-ttu-id="cd57a-130">Gibt die Anzahl der Tage an, für die der Azure-Speicherdienst metrikinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="cd57a-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="cd57a-131">-ServiceType</span></span>
<span data-ttu-id="cd57a-132">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="cd57a-132">Specifies the storage service type.</span></span>
<span data-ttu-id="cd57a-133">Mit diesem Cmdlet werden die Metriken-Eigenschaften für den Diensttyp geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cd57a-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="cd57a-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd57a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd57a-135">BLOB</span><span class="sxs-lookup"><span data-stu-id="cd57a-135">Blob</span></span> 
- <span data-ttu-id="cd57a-136">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd57a-136">Table</span></span>
- <span data-ttu-id="cd57a-137">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="cd57a-137">Queue</span></span>
- <span data-ttu-id="cd57a-138">Datei</span><span class="sxs-lookup"><span data-stu-id="cd57a-138">File</span></span>

<span data-ttu-id="cd57a-139">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd57a-139">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-140">-Version</span><span class="sxs-lookup"><span data-stu-id="cd57a-140">-Version</span></span>
<span data-ttu-id="cd57a-141">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="cd57a-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="cd57a-142">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="cd57a-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd57a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd57a-143">CommonParameters</span></span>
<span data-ttu-id="cd57a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd57a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd57a-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd57a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd57a-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd57a-146">INPUTS</span></span>

### <span data-ttu-id="cd57a-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd57a-147">IStorageContext</span></span>

<span data-ttu-id="cd57a-148">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd57a-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="cd57a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd57a-149">OUTPUTS</span></span>

### <span data-ttu-id="cd57a-150">Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="cd57a-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="cd57a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd57a-151">NOTES</span></span>

## <span data-ttu-id="cd57a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd57a-152">RELATED LINKS</span></span>

[<span data-ttu-id="cd57a-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cd57a-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="cd57a-154">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd57a-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


