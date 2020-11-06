---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503330"
---
# <span data-ttu-id="949e9-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="949e9-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="949e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="949e9-102">SYNOPSIS</span></span>
<span data-ttu-id="949e9-103">Ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="949e9-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="949e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="949e9-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="949e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="949e9-105">DESCRIPTION</span></span>
<span data-ttu-id="949e9-106">Das Cmdlet " **Satz-AzureStorageServiceMetricsProperty** " ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="949e9-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="949e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="949e9-107">EXAMPLES</span></span>

### <span data-ttu-id="949e9-108">Beispiel 1: Ändern von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="949e9-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="949e9-109">Mit diesem Befehl werden die Metriken der Version 1,0 für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="949e9-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="949e9-110">Für Azure Storage Service-Metriken werden die Einträge 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="949e9-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="949e9-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Metrik-Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="949e9-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="949e9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="949e9-112">PARAMETERS</span></span>

### <span data-ttu-id="949e9-113">-Context</span><span class="sxs-lookup"><span data-stu-id="949e9-113">-Context</span></span>
<span data-ttu-id="949e9-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="949e9-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="949e9-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="949e9-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="949e9-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="949e9-116">-MetricsLevel</span></span>
<span data-ttu-id="949e9-117">Gibt die metrikebene an, die der Azure-Speicher für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="949e9-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="949e9-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="949e9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="949e9-119">Keine</span><span class="sxs-lookup"><span data-stu-id="949e9-119">None</span></span>
- <span data-ttu-id="949e9-120">Dienst</span><span class="sxs-lookup"><span data-stu-id="949e9-120">Service</span></span>
- <span data-ttu-id="949e9-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="949e9-121">ServiceAndApi</span></span>

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

### <span data-ttu-id="949e9-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="949e9-122">-MetricsType</span></span>
<span data-ttu-id="949e9-123">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="949e9-123">Specifies a metrics type.</span></span>
<span data-ttu-id="949e9-124">Mit diesem cmldet wird der Typ des Azure Storage Service-Metriken auf den Wert festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="949e9-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="949e9-125">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="949e9-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="949e9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="949e9-126">-PassThru</span></span>
<span data-ttu-id="949e9-127">Gibt an, dass diese Cmdlets die aktualisierten Metriken-Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="949e9-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="949e9-128">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="949e9-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="949e9-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="949e9-129">-RetentionDays</span></span>
<span data-ttu-id="949e9-130">Gibt die Anzahl der Tage an, für die der Azure-Speicherdienst metrikinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="949e9-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="949e9-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="949e9-131">-ServiceType</span></span>
<span data-ttu-id="949e9-132">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="949e9-132">Specifies the storage service type.</span></span>
<span data-ttu-id="949e9-133">Mit diesem Cmdlet werden die Metriken-Eigenschaften für den Diensttyp geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="949e9-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="949e9-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="949e9-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="949e9-135">BLOB</span><span class="sxs-lookup"><span data-stu-id="949e9-135">Blob</span></span> 
- <span data-ttu-id="949e9-136">Tabelle</span><span class="sxs-lookup"><span data-stu-id="949e9-136">Table</span></span>
- <span data-ttu-id="949e9-137">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="949e9-137">Queue</span></span>
- <span data-ttu-id="949e9-138">Datei</span><span class="sxs-lookup"><span data-stu-id="949e9-138">File</span></span>

<span data-ttu-id="949e9-139">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="949e9-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="949e9-140">-Version</span><span class="sxs-lookup"><span data-stu-id="949e9-140">-Version</span></span>
<span data-ttu-id="949e9-141">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="949e9-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="949e9-142">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="949e9-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="949e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949e9-143">CommonParameters</span></span>
<span data-ttu-id="949e9-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949e9-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="949e9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949e9-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="949e9-146">INPUTS</span></span>

### <span data-ttu-id="949e9-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="949e9-147">IStorageContext</span></span>

<span data-ttu-id="949e9-148">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="949e9-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="949e9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="949e9-149">OUTPUTS</span></span>

### <span data-ttu-id="949e9-150">Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="949e9-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="949e9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="949e9-151">NOTES</span></span>

## <span data-ttu-id="949e9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="949e9-152">RELATED LINKS</span></span>

[<span data-ttu-id="949e9-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="949e9-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="949e9-154">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="949e9-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


