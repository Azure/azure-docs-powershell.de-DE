---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173657"
---
# <span data-ttu-id="48999-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="48999-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="48999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48999-102">SYNOPSIS</span></span>
<span data-ttu-id="48999-103">Ändert die Protokollierung für Azure Storage-Dienste.</span><span class="sxs-lookup"><span data-stu-id="48999-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="48999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48999-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48999-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48999-105">DESCRIPTION</span></span>
<span data-ttu-id="48999-106">Das **Cmdlet "Set-AzStorageServiceLoggingProperty"** ändert die Protokollierung für Azure Storage-Dienste.</span><span class="sxs-lookup"><span data-stu-id="48999-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="48999-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48999-107">EXAMPLES</span></span>

### <span data-ttu-id="48999-108">Beispiel 1: Ändern der Protokolleigenschaften für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="48999-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="48999-109">Mit diesem Befehl wird die Protokollierung in Version 1.0 für blob storage so geändert, dass Lese- und Schreibvorgänge enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48999-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="48999-110">Die Azure Storage -Dienstprotokollierung behält Einträge für 10 Tage bei.</span><span class="sxs-lookup"><span data-stu-id="48999-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="48999-111">Da dieser Befehl den Parameter *"PassThru"* angibt, zeigt der Befehl die geänderten Protokolleigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="48999-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="48999-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48999-112">PARAMETERS</span></span>

### <span data-ttu-id="48999-113">-Context</span><span class="sxs-lookup"><span data-stu-id="48999-113">-Context</span></span>
<span data-ttu-id="48999-114">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="48999-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="48999-115">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48999-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="48999-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48999-116">-DefaultProfile</span></span>
<span data-ttu-id="48999-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48999-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48999-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="48999-118">-LoggingOperations</span></span>
<span data-ttu-id="48999-119">Gibt ein Array von Azure Storage -Dienstvorgängen an.</span><span class="sxs-lookup"><span data-stu-id="48999-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="48999-120">Azure Storage Services protokolliert die Vorgänge, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="48999-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="48999-121">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="48999-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48999-122">Keine</span><span class="sxs-lookup"><span data-stu-id="48999-122">None</span></span>
- <span data-ttu-id="48999-123">Lesen</span><span class="sxs-lookup"><span data-stu-id="48999-123">Read</span></span>
- <span data-ttu-id="48999-124">Schreiben</span><span class="sxs-lookup"><span data-stu-id="48999-124">Write</span></span>
- <span data-ttu-id="48999-125">Löschen</span><span class="sxs-lookup"><span data-stu-id="48999-125">Delete</span></span>
- <span data-ttu-id="48999-126">Alle</span><span class="sxs-lookup"><span data-stu-id="48999-126">All</span></span>

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

### <span data-ttu-id="48999-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48999-127">-PassThru</span></span>
<span data-ttu-id="48999-128">Gibt an, dass dieses Cmdlet die aktualisierten Protokolleigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="48999-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="48999-129">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48999-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="48999-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="48999-130">-RetentionDays</span></span>
<span data-ttu-id="48999-131">Gibt die Anzahl der Tage an, für die der Azure Storage Service die protokollierten Informationen beibehalte.</span><span class="sxs-lookup"><span data-stu-id="48999-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="48999-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="48999-132">-ServiceType</span></span>
<span data-ttu-id="48999-133">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="48999-133">Specifies the storage service type.</span></span>
<span data-ttu-id="48999-134">Dieses Cmdlet ändert die Protokolleigenschaften für den Diensttyp, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="48999-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="48999-135">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="48999-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48999-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="48999-136">Blob</span></span> 
- <span data-ttu-id="48999-137">Tabelle</span><span class="sxs-lookup"><span data-stu-id="48999-137">Table</span></span>
- <span data-ttu-id="48999-138">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="48999-138">Queue</span></span>
- <span data-ttu-id="48999-139">Datei Der Wert von "Datei" wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48999-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="48999-140">-Version</span><span class="sxs-lookup"><span data-stu-id="48999-140">-Version</span></span>
<span data-ttu-id="48999-141">Gibt die Version der Azure Storage -Dienstprotokollierung an.</span><span class="sxs-lookup"><span data-stu-id="48999-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="48999-142">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="48999-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="48999-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48999-143">CommonParameters</span></span>
<span data-ttu-id="48999-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48999-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48999-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48999-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48999-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48999-146">INPUTS</span></span>

### <span data-ttu-id="48999-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="48999-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="48999-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48999-148">OUTPUTS</span></span>

### <span data-ttu-id="48999-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="48999-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="48999-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48999-150">NOTES</span></span>

## <span data-ttu-id="48999-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48999-151">RELATED LINKS</span></span>

[<span data-ttu-id="48999-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="48999-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="48999-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="48999-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


