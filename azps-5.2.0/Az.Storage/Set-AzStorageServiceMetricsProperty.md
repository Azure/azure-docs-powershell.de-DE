---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303248"
---
# <span data-ttu-id="4579d-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4579d-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="4579d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4579d-102">SYNOPSIS</span></span>
<span data-ttu-id="4579d-103">Ändert die Metrikeigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4579d-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4579d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4579d-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4579d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4579d-105">DESCRIPTION</span></span>
<span data-ttu-id="4579d-106">Das **Cmdlet "Set-AzStorageServiceMetricsProperty"** ändert die Metrikeigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4579d-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4579d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4579d-107">EXAMPLES</span></span>

### <span data-ttu-id="4579d-108">Beispiel 1: Ändern der Metrikeigenschaften für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="4579d-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="4579d-109">Mit diesem Befehl werden Die Version 1.0-Metriken für den BLOB-Speicher auf eine Dienstebene geändert.</span><span class="sxs-lookup"><span data-stu-id="4579d-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="4579d-110">Die Azure Storage -Dienstmetriken bewahren Einträge 10 Tage lang auf.</span><span class="sxs-lookup"><span data-stu-id="4579d-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="4579d-111">Da dieser Befehl den Parameter *"PassThru"* angibt, zeigt der Befehl die geänderten Metrikeigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="4579d-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="4579d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4579d-112">PARAMETERS</span></span>

### <span data-ttu-id="4579d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4579d-113">-Context</span></span>
<span data-ttu-id="4579d-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4579d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4579d-115">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4579d-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4579d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4579d-116">-DefaultProfile</span></span>
<span data-ttu-id="4579d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4579d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4579d-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="4579d-118">-MetricsLevel</span></span>
<span data-ttu-id="4579d-119">Gibt die Metrikebene an, die Azure Storage für den Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4579d-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="4579d-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4579d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4579d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4579d-121">None</span></span>
- <span data-ttu-id="4579d-122">Dienst</span><span class="sxs-lookup"><span data-stu-id="4579d-122">Service</span></span>
- <span data-ttu-id="4579d-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="4579d-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="4579d-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="4579d-124">-MetricsType</span></span>
<span data-ttu-id="4579d-125">Gibt einen Metriktyp an.</span><span class="sxs-lookup"><span data-stu-id="4579d-125">Specifies a metrics type.</span></span>
<span data-ttu-id="4579d-126">Dieses Cmdlet legt den Azure Storage -Dienstmetriktyp auf den Wert fest, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4579d-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="4579d-127">Die zulässigen Werte für diesen Parameter sind: "Hour" und "Minute".</span><span class="sxs-lookup"><span data-stu-id="4579d-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="4579d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4579d-128">-PassThru</span></span>
<span data-ttu-id="4579d-129">Gibt an, dass diese Cmdlets die aktualisierten Metrikeigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4579d-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="4579d-130">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4579d-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4579d-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4579d-131">-RetentionDays</span></span>
<span data-ttu-id="4579d-132">Gibt die Anzahl der Tage an, für die der Azure Storage Service Metrikinformationen beibehalte.</span><span class="sxs-lookup"><span data-stu-id="4579d-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="4579d-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4579d-133">-ServiceType</span></span>
<span data-ttu-id="4579d-134">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="4579d-134">Specifies the storage service type.</span></span>
<span data-ttu-id="4579d-135">Dieses Cmdlet ändert die Metrikeigenschaften für den Diensttyp, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4579d-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4579d-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4579d-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4579d-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="4579d-137">Blob</span></span> 
- <span data-ttu-id="4579d-138">Tabelle</span><span class="sxs-lookup"><span data-stu-id="4579d-138">Table</span></span>
- <span data-ttu-id="4579d-139">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4579d-139">Queue</span></span>
- <span data-ttu-id="4579d-140">Datei Der Wert von "Datei" wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4579d-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4579d-141">-Version</span><span class="sxs-lookup"><span data-stu-id="4579d-141">-Version</span></span>
<span data-ttu-id="4579d-142">Gibt die Version der Azure Storage-Metriken an.</span><span class="sxs-lookup"><span data-stu-id="4579d-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="4579d-143">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="4579d-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="4579d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4579d-144">CommonParameters</span></span>
<span data-ttu-id="4579d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4579d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4579d-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4579d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4579d-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4579d-147">INPUTS</span></span>

### <span data-ttu-id="4579d-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4579d-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4579d-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4579d-149">OUTPUTS</span></span>

### <span data-ttu-id="4579d-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="4579d-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="4579d-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4579d-151">NOTES</span></span>

## <span data-ttu-id="4579d-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4579d-152">RELATED LINKS</span></span>

[<span data-ttu-id="4579d-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4579d-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="4579d-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4579d-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


