---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475781"
---
# <span data-ttu-id="5702b-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5702b-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="5702b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5702b-102">SYNOPSIS</span></span>
<span data-ttu-id="5702b-103">Ändert die Protokollierung für Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="5702b-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="5702b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5702b-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="5702b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5702b-105">DESCRIPTION</span></span>
<span data-ttu-id="5702b-106">Das Cmdlet " **Satz-AzureStorageServiceLoggingProperty** " ändert die Protokollierung für Azure Storage-Dienste.</span><span class="sxs-lookup"><span data-stu-id="5702b-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="5702b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5702b-107">EXAMPLES</span></span>

### <span data-ttu-id="5702b-108">Beispiel 1: Ändern der Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="5702b-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="5702b-109">Mit diesem Befehl wird die Version 1,0-Protokollierung für den BLOB-Speicher geändert, um Lese-und Schreibvorgänge einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="5702b-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="5702b-110">Die Azure-Speicherdienst Protokollierung speichert Einträge für 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="5702b-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="5702b-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Protokollierungseigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="5702b-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="5702b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5702b-112">PARAMETERS</span></span>

### <span data-ttu-id="5702b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5702b-113">-Context</span></span>
<span data-ttu-id="5702b-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5702b-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5702b-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5702b-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5702b-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="5702b-116">-LoggingOperations</span></span>
<span data-ttu-id="5702b-117">Gibt ein Array von Azure-Speicherdienst Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="5702b-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="5702b-118">Azure Storage Services protokolliert die Vorgänge, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5702b-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="5702b-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5702b-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5702b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="5702b-120">None</span></span>
- <span data-ttu-id="5702b-121">Lesen</span><span class="sxs-lookup"><span data-stu-id="5702b-121">Read</span></span>
- <span data-ttu-id="5702b-122">Schreiben</span><span class="sxs-lookup"><span data-stu-id="5702b-122">Write</span></span>
- <span data-ttu-id="5702b-123">Löschen</span><span class="sxs-lookup"><span data-stu-id="5702b-123">Delete</span></span>
- <span data-ttu-id="5702b-124">Alle</span><span class="sxs-lookup"><span data-stu-id="5702b-124">All</span></span>

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

### <span data-ttu-id="5702b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5702b-125">-PassThru</span></span>
<span data-ttu-id="5702b-126">Gibt an, dass dieses Cmdlet die aktualisierten Protokollierungseigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5702b-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="5702b-127">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5702b-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5702b-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5702b-128">-RetentionDays</span></span>
<span data-ttu-id="5702b-129">Gibt die Anzahl der Tage an, die der Azure-Speicherdienst protokollierte Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="5702b-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="5702b-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5702b-130">-ServiceType</span></span>
<span data-ttu-id="5702b-131">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="5702b-131">Specifies the storage service type.</span></span>
<span data-ttu-id="5702b-132">Mit diesem Cmdlet werden die Protokollierungseigenschaften des Diensttyps geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5702b-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5702b-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5702b-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5702b-134">BLOB</span><span class="sxs-lookup"><span data-stu-id="5702b-134">Blob</span></span> 
- <span data-ttu-id="5702b-135">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5702b-135">Table</span></span>
- <span data-ttu-id="5702b-136">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5702b-136">Queue</span></span>
- <span data-ttu-id="5702b-137">Datei</span><span class="sxs-lookup"><span data-stu-id="5702b-137">File</span></span>

<span data-ttu-id="5702b-138">Der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5702b-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5702b-139">-Version</span><span class="sxs-lookup"><span data-stu-id="5702b-139">-Version</span></span>
<span data-ttu-id="5702b-140">Gibt die Version der Azure-Speicherdienst Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="5702b-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="5702b-141">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="5702b-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="5702b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5702b-142">CommonParameters</span></span>
<span data-ttu-id="5702b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5702b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5702b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5702b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5702b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5702b-145">INPUTS</span></span>

## <span data-ttu-id="5702b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5702b-146">OUTPUTS</span></span>

## <span data-ttu-id="5702b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5702b-147">NOTES</span></span>

## <span data-ttu-id="5702b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5702b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5702b-149">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5702b-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="5702b-150">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5702b-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


