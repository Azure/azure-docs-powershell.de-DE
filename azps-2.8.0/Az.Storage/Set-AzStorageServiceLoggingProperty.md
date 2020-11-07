---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 43b8c6426fe2d4eceab65fc1b103e62cdb1eb346
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650540"
---
# <span data-ttu-id="66c0b-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="66c0b-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="66c0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="66c0b-103">Ändert die Protokollierung für Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="66c0b-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="66c0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66c0b-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="66c0b-106">Das Cmdlet " **Satz-AzStorageServiceLoggingProperty** " ändert die Protokollierung für Azure Storage-Dienste.</span><span class="sxs-lookup"><span data-stu-id="66c0b-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="66c0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="66c0b-108">Beispiel 1: Ändern der Protokollierungseigenschaften für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="66c0b-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="66c0b-109">Mit diesem Befehl wird die Version 1,0-Protokollierung für den BLOB-Speicher geändert, um Lese-und Schreibvorgänge einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="66c0b-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="66c0b-110">Die Azure-Speicherdienst Protokollierung speichert Einträge für 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="66c0b-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="66c0b-111">Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Protokollierungseigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="66c0b-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="66c0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="66c0b-112">PARAMETERS</span></span>

### <span data-ttu-id="66c0b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="66c0b-113">-Context</span></span>
<span data-ttu-id="66c0b-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="66c0b-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="66c0b-115">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="66c0b-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="66c0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c0b-116">-DefaultProfile</span></span>
<span data-ttu-id="66c0b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66c0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c0b-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="66c0b-118">-LoggingOperations</span></span>
<span data-ttu-id="66c0b-119">Gibt ein Array von Azure-Speicherdienst Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="66c0b-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="66c0b-120">Azure Storage Services protokolliert die Vorgänge, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="66c0b-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="66c0b-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="66c0b-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66c0b-122">Keine</span><span class="sxs-lookup"><span data-stu-id="66c0b-122">None</span></span>
- <span data-ttu-id="66c0b-123">Lesen</span><span class="sxs-lookup"><span data-stu-id="66c0b-123">Read</span></span>
- <span data-ttu-id="66c0b-124">Schreiben</span><span class="sxs-lookup"><span data-stu-id="66c0b-124">Write</span></span>
- <span data-ttu-id="66c0b-125">Löschen</span><span class="sxs-lookup"><span data-stu-id="66c0b-125">Delete</span></span>
- <span data-ttu-id="66c0b-126">Alle</span><span class="sxs-lookup"><span data-stu-id="66c0b-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c0b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c0b-127">-PassThru</span></span>
<span data-ttu-id="66c0b-128">Gibt an, dass dieses Cmdlet die aktualisierten Protokollierungseigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="66c0b-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="66c0b-129">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="66c0b-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="66c0b-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="66c0b-130">-RetentionDays</span></span>
<span data-ttu-id="66c0b-131">Gibt die Anzahl der Tage an, die der Azure-Speicherdienst protokollierte Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="66c0b-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="66c0b-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="66c0b-132">-ServiceType</span></span>
<span data-ttu-id="66c0b-133">Gibt den Typ des Speicher Diensts an.</span><span class="sxs-lookup"><span data-stu-id="66c0b-133">Specifies the storage service type.</span></span>
<span data-ttu-id="66c0b-134">Mit diesem Cmdlet werden die Protokollierungseigenschaften des Diensttyps geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="66c0b-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="66c0b-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="66c0b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66c0b-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="66c0b-136">Blob</span></span> 
- <span data-ttu-id="66c0b-137">Tabelle</span><span class="sxs-lookup"><span data-stu-id="66c0b-137">Table</span></span>
- <span data-ttu-id="66c0b-138">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="66c0b-138">Queue</span></span>
- <span data-ttu-id="66c0b-139">Datei der Wert der Datei wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66c0b-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="66c0b-140">-Version</span><span class="sxs-lookup"><span data-stu-id="66c0b-140">-Version</span></span>
<span data-ttu-id="66c0b-141">Gibt die Version der Azure-Speicherdienst Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="66c0b-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="66c0b-142">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="66c0b-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="66c0b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c0b-143">CommonParameters</span></span>
<span data-ttu-id="66c0b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c0b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c0b-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c0b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c0b-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66c0b-146">INPUTS</span></span>

### <span data-ttu-id="66c0b-147">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66c0b-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66c0b-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66c0b-148">OUTPUTS</span></span>

### <span data-ttu-id="66c0b-149">Microsoft. Azure. Storage. shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="66c0b-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="66c0b-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="66c0b-150">NOTES</span></span>

## <span data-ttu-id="66c0b-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66c0b-151">RELATED LINKS</span></span>

[<span data-ttu-id="66c0b-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="66c0b-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="66c0b-153">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="66c0b-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


