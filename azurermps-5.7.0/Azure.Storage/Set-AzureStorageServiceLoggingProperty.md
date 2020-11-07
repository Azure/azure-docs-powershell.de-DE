---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fbd7c691e2cfbef58bc59429f68740af00288906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664948"
---
# <span data-ttu-id="81ccd-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="81ccd-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="81ccd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="81ccd-103">Ändert die Protokollierung für Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="81ccd-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ccd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81ccd-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="81ccd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="81ccd-106">Das Cmdlet " **Satz-AzureStorageServiceLoggingProperty** " ändert die Protokollierung für Azure Storage-Dienste.</span><span class="sxs-lookup"><span data-stu-id="81ccd-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="81ccd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81ccd-107">EXAMPLES</span></span>

### <span data-ttu-id="81ccd-108">Beispiel 1: Ändern der Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="81ccd-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="81ccd-109">Mit diesem Befehl wird die Version 1,0-Protokollierung für den BLOB-Speicher geändert, um Lese-und Schreibvorgänge einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="81ccd-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="81ccd-110">Die Azure-Speicherdienst Protokollierung speichert Einträge für 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="81ccd-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="81ccd-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Protokollierungseigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="81ccd-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="81ccd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="81ccd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="81ccd-113">-Context</span></span>
<span data-ttu-id="81ccd-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="81ccd-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="81ccd-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="81ccd-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="81ccd-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="81ccd-116">-LoggingOperations</span></span>
<span data-ttu-id="81ccd-117">Gibt ein Array von Azure-Speicherdienst Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="81ccd-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="81ccd-118">Azure Storage Services protokolliert die Vorgänge, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="81ccd-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="81ccd-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="81ccd-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81ccd-120">Keine</span><span class="sxs-lookup"><span data-stu-id="81ccd-120">None</span></span>
- <span data-ttu-id="81ccd-121">Lesen</span><span class="sxs-lookup"><span data-stu-id="81ccd-121">Read</span></span>
- <span data-ttu-id="81ccd-122">Schreiben</span><span class="sxs-lookup"><span data-stu-id="81ccd-122">Write</span></span>
- <span data-ttu-id="81ccd-123">Löschen</span><span class="sxs-lookup"><span data-stu-id="81ccd-123">Delete</span></span>
- <span data-ttu-id="81ccd-124">Alle</span><span class="sxs-lookup"><span data-stu-id="81ccd-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ccd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81ccd-125">-PassThru</span></span>
<span data-ttu-id="81ccd-126">Gibt an, dass dieses Cmdlet die aktualisierten Protokollierungseigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="81ccd-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="81ccd-127">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81ccd-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="81ccd-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="81ccd-128">-RetentionDays</span></span>
<span data-ttu-id="81ccd-129">Gibt die Anzahl der Tage an, die der Azure-Speicherdienst protokollierte Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="81ccd-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="81ccd-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="81ccd-130">-ServiceType</span></span>
<span data-ttu-id="81ccd-131">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="81ccd-131">Specifies the storage service type.</span></span>
<span data-ttu-id="81ccd-132">Mit diesem Cmdlet werden die Protokollierungseigenschaften des Diensttyps geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="81ccd-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="81ccd-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="81ccd-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81ccd-134">BLOB</span><span class="sxs-lookup"><span data-stu-id="81ccd-134">Blob</span></span> 
- <span data-ttu-id="81ccd-135">Tabelle</span><span class="sxs-lookup"><span data-stu-id="81ccd-135">Table</span></span>
- <span data-ttu-id="81ccd-136">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="81ccd-136">Queue</span></span>
- <span data-ttu-id="81ccd-137">Datei</span><span class="sxs-lookup"><span data-stu-id="81ccd-137">File</span></span>

<span data-ttu-id="81ccd-138">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81ccd-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="81ccd-139">-Version</span><span class="sxs-lookup"><span data-stu-id="81ccd-139">-Version</span></span>
<span data-ttu-id="81ccd-140">Gibt die Version der Azure-Speicherdienst Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="81ccd-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="81ccd-141">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="81ccd-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="81ccd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ccd-142">CommonParameters</span></span>
<span data-ttu-id="81ccd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ccd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ccd-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ccd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ccd-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81ccd-145">INPUTS</span></span>

### <span data-ttu-id="81ccd-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="81ccd-146">IStorageContext</span></span>

<span data-ttu-id="81ccd-147">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="81ccd-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="81ccd-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81ccd-148">OUTPUTS</span></span>

### <span data-ttu-id="81ccd-149">Microsoft. WindowsAzure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="81ccd-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="81ccd-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="81ccd-150">NOTES</span></span>

## <span data-ttu-id="81ccd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81ccd-151">RELATED LINKS</span></span>

[<span data-ttu-id="81ccd-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="81ccd-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="81ccd-153">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="81ccd-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


