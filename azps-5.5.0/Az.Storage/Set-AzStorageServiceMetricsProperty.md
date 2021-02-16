---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156081"
---
# <span data-ttu-id="1f6c8-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1f6c8-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="1f6c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6c8-103">Ändert die Metrikeigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="1f6c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f6c8-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6c8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f6c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6c8-106">Das **Cmdlet "Set-AzStorageServiceMetricsProperty"** ändert die Metrikeigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="1f6c8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1f6c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6c8-108">Beispiel 1: Ändern der Metrikeigenschaften für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="1f6c8-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="1f6c8-109">Mit diesem Befehl werden Die Version 1.0-Metriken für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="1f6c8-110">Die Azure Storage -Dienstmetriken bewahren Einträge 10 Tage lang auf.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="1f6c8-111">Da dieser Befehl den Parameter *"PassThru"* angibt, zeigt der Befehl die geänderten Metrikeigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="1f6c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f6c8-112">PARAMETERS</span></span>

### <span data-ttu-id="1f6c8-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1f6c8-113">-Context</span></span>
<span data-ttu-id="1f6c8-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1f6c8-115">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1f6c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6c8-116">-DefaultProfile</span></span>
<span data-ttu-id="1f6c8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f6c8-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="1f6c8-118">-MetricsLevel</span></span>
<span data-ttu-id="1f6c8-119">Gibt die Metriksstufe an, die Azure Storage für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="1f6c8-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1f6c8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f6c8-121">Keine</span><span class="sxs-lookup"><span data-stu-id="1f6c8-121">None</span></span>
- <span data-ttu-id="1f6c8-122">Dienst</span><span class="sxs-lookup"><span data-stu-id="1f6c8-122">Service</span></span>
- <span data-ttu-id="1f6c8-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="1f6c8-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="1f6c8-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="1f6c8-124">-MetricsType</span></span>
<span data-ttu-id="1f6c8-125">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-125">Specifies a metrics type.</span></span>
<span data-ttu-id="1f6c8-126">Dieses Cmdlet legt den Azure Storage -Dienstmetriktyp auf den Wert fest, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="1f6c8-127">Die zulässigen Werte für diesen Parameter sind: "Hour" und "Minute".</span><span class="sxs-lookup"><span data-stu-id="1f6c8-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="1f6c8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f6c8-128">-PassThru</span></span>
<span data-ttu-id="1f6c8-129">Gibt an, dass diese Cmdlets die aktualisierten Metrikeigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="1f6c8-130">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1f6c8-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="1f6c8-131">-RetentionDays</span></span>
<span data-ttu-id="1f6c8-132">Gibt die Anzahl der Tage an, für die der Azure Storage Service Metrikinformationen beibehalte.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="1f6c8-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1f6c8-133">-ServiceType</span></span>
<span data-ttu-id="1f6c8-134">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-134">Specifies the storage service type.</span></span>
<span data-ttu-id="1f6c8-135">Dieses Cmdlet ändert die Metrikeigenschaften für den Diensttyp, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1f6c8-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1f6c8-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f6c8-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="1f6c8-137">Blob</span></span> 
- <span data-ttu-id="1f6c8-138">Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f6c8-138">Table</span></span>
- <span data-ttu-id="1f6c8-139">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="1f6c8-139">Queue</span></span>
- <span data-ttu-id="1f6c8-140">Datei Der Wert von "Datei" wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="1f6c8-141">-Version</span><span class="sxs-lookup"><span data-stu-id="1f6c8-141">-Version</span></span>
<span data-ttu-id="1f6c8-142">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="1f6c8-143">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="1f6c8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6c8-144">CommonParameters</span></span>
<span data-ttu-id="1f6c8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6c8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6c8-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6c8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6c8-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1f6c8-147">INPUTS</span></span>

### <span data-ttu-id="1f6c8-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f6c8-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f6c8-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1f6c8-149">OUTPUTS</span></span>

### <span data-ttu-id="1f6c8-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="1f6c8-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="1f6c8-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1f6c8-151">NOTES</span></span>

## <span data-ttu-id="1f6c8-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1f6c8-152">RELATED LINKS</span></span>

[<span data-ttu-id="1f6c8-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1f6c8-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="1f6c8-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f6c8-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


