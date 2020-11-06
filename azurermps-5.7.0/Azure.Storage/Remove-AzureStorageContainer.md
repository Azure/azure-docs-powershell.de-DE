---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
ms.openlocfilehash: 23ea79879b7b194b9f761c585087a931f9373886
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481373"
---
# <span data-ttu-id="1eb18-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1eb18-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="1eb18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1eb18-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb18-103">Entfernt den angegebenen Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="1eb18-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb18-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb18-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1eb18-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb18-106">Das Cmdlet **Remove-AzureStorageContainer** entfernt den angegebenen Speichercontainer in Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb18-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="1eb18-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1eb18-107">EXAMPLES</span></span>

### <span data-ttu-id="1eb18-108">Beispiel 1: Entfernen eines Containers</span><span class="sxs-lookup"><span data-stu-id="1eb18-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="1eb18-109">In diesem Beispiel wird ein Container mit dem Namen MyTestContainer entfernt.</span><span class="sxs-lookup"><span data-stu-id="1eb18-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="1eb18-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1eb18-110">PARAMETERS</span></span>

### <span data-ttu-id="1eb18-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1eb18-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1eb18-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1eb18-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1eb18-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="1eb18-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1eb18-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1eb18-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1eb18-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1eb18-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1eb18-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="1eb18-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1eb18-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="1eb18-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1eb18-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="1eb18-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1eb18-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="1eb18-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1eb18-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1eb18-120">The default value is 10.</span></span>

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

### <span data-ttu-id="1eb18-121">-Context</span><span class="sxs-lookup"><span data-stu-id="1eb18-121">-Context</span></span>
<span data-ttu-id="1eb18-122">Gibt einen Kontext für den Container an, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="1eb18-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="1eb18-123">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb18-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="1eb18-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1eb18-124">-Force</span></span>
<span data-ttu-id="1eb18-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1eb18-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1eb18-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb18-126">-Name</span></span>
<span data-ttu-id="1eb18-127">Gibt den Namen des zu entfernenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="1eb18-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb18-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eb18-128">-PassThru</span></span>
<span data-ttu-id="1eb18-129">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="1eb18-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1eb18-130">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1eb18-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1eb18-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1eb18-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1eb18-132">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1eb18-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1eb18-133">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1eb18-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1eb18-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1eb18-134">-Confirm</span></span>
<span data-ttu-id="1eb18-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1eb18-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb18-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb18-136">-WhatIf</span></span>
<span data-ttu-id="1eb18-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1eb18-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb18-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1eb18-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb18-139">CommonParameters</span></span>
<span data-ttu-id="1eb18-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb18-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb18-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb18-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1eb18-142">INPUTS</span></span>

### <span data-ttu-id="1eb18-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1eb18-143">IStorageContext</span></span>

<span data-ttu-id="1eb18-144">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1eb18-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1eb18-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1eb18-145">String</span></span>

<span data-ttu-id="1eb18-146">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1eb18-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1eb18-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1eb18-147">OUTPUTS</span></span>

### <span data-ttu-id="1eb18-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1eb18-148">System.Boolean</span></span>

## <span data-ttu-id="1eb18-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="1eb18-149">NOTES</span></span>

## <span data-ttu-id="1eb18-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1eb18-150">RELATED LINKS</span></span>

[<span data-ttu-id="1eb18-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1eb18-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="1eb18-152">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1eb18-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
