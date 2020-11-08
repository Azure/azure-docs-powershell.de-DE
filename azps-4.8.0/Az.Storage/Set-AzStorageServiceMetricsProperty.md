---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165958"
---
# <span data-ttu-id="ca44a-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ca44a-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="ca44a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca44a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca44a-103">Ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="ca44a-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ca44a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca44a-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca44a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca44a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca44a-106">Das Cmdlet " **Satz-AzStorageServiceMetricsProperty** " ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="ca44a-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ca44a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca44a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca44a-108">Beispiel 1: Ändern von Metriken Eigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="ca44a-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="ca44a-109">Mit diesem Befehl werden die Metriken der Version 1,0 für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="ca44a-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="ca44a-110">Für Azure Storage Service-Metriken werden die Einträge 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="ca44a-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Metrik-Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="ca44a-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="ca44a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca44a-112">PARAMETERS</span></span>

### <span data-ttu-id="ca44a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ca44a-113">-Context</span></span>
<span data-ttu-id="ca44a-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ca44a-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca44a-115">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca44a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca44a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca44a-116">-DefaultProfile</span></span>
<span data-ttu-id="ca44a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca44a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca44a-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="ca44a-118">-MetricsLevel</span></span>
<span data-ttu-id="ca44a-119">Gibt die metrikebene an, die der Azure-Speicher für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca44a-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="ca44a-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca44a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca44a-121">Keine</span><span class="sxs-lookup"><span data-stu-id="ca44a-121">None</span></span>
- <span data-ttu-id="ca44a-122">Dienst</span><span class="sxs-lookup"><span data-stu-id="ca44a-122">Service</span></span>
- <span data-ttu-id="ca44a-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="ca44a-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca44a-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="ca44a-124">-MetricsType</span></span>
<span data-ttu-id="ca44a-125">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="ca44a-125">Specifies a metrics type.</span></span>
<span data-ttu-id="ca44a-126">Mit diesem Cmdlet wird der Typ des Azure Storage Service-Metriken auf den Wert festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="ca44a-127">Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.</span><span class="sxs-lookup"><span data-stu-id="ca44a-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="ca44a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca44a-128">-PassThru</span></span>
<span data-ttu-id="ca44a-129">Gibt an, dass diese Cmdlets die aktualisierten Metriken-Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ca44a-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="ca44a-130">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca44a-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ca44a-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="ca44a-131">-RetentionDays</span></span>
<span data-ttu-id="ca44a-132">Gibt die Anzahl der Tage an, für die der Azure-Speicherdienst metrikinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="ca44a-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="ca44a-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ca44a-133">-ServiceType</span></span>
<span data-ttu-id="ca44a-134">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="ca44a-134">Specifies the storage service type.</span></span>
<span data-ttu-id="ca44a-135">Mit diesem Cmdlet werden die Metriken-Eigenschaften für den Diensttyp geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ca44a-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca44a-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca44a-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="ca44a-137">Blob</span></span> 
- <span data-ttu-id="ca44a-138">Tabelle</span><span class="sxs-lookup"><span data-stu-id="ca44a-138">Table</span></span>
- <span data-ttu-id="ca44a-139">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ca44a-139">Queue</span></span>
- <span data-ttu-id="ca44a-140">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ca44a-141">-Version</span><span class="sxs-lookup"><span data-stu-id="ca44a-141">-Version</span></span>
<span data-ttu-id="ca44a-142">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="ca44a-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="ca44a-143">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="ca44a-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="ca44a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca44a-144">CommonParameters</span></span>
<span data-ttu-id="ca44a-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca44a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca44a-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca44a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca44a-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca44a-147">INPUTS</span></span>

### <span data-ttu-id="ca44a-148">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca44a-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca44a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca44a-149">OUTPUTS</span></span>

### <span data-ttu-id="ca44a-150">Microsoft. Azure. Storage. shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="ca44a-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="ca44a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca44a-151">NOTES</span></span>

## <span data-ttu-id="ca44a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca44a-152">RELATED LINKS</span></span>

[<span data-ttu-id="ca44a-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ca44a-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="ca44a-154">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca44a-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


