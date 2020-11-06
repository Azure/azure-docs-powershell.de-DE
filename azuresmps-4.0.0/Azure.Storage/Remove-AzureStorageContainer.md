---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ccaa0ef1ce2a29851d6e90235e4564df3bde876
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474669"
---
# <span data-ttu-id="a76cd-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a76cd-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="a76cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a76cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a76cd-103">Entfernt den angegebenen Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="a76cd-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="a76cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a76cd-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a76cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a76cd-106">Das Cmdlet **Remove-AzureStorageContainer** entfernt den angegebenen Speichercontainer in Azure.</span><span class="sxs-lookup"><span data-stu-id="a76cd-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="a76cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a76cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a76cd-108">Beispiel 1: Entfernen eines Containers</span><span class="sxs-lookup"><span data-stu-id="a76cd-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="a76cd-109">In diesem Beispiel wird ein Container mit dem Namen MyTestContainer entfernt.</span><span class="sxs-lookup"><span data-stu-id="a76cd-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="a76cd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a76cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a76cd-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a76cd-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a76cd-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a76cd-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a76cd-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="a76cd-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a76cd-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a76cd-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a76cd-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a76cd-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a76cd-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="a76cd-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a76cd-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="a76cd-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a76cd-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a76cd-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a76cd-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a76cd-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a76cd-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a76cd-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a76cd-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a76cd-121">-Context</span></span>
<span data-ttu-id="a76cd-122">Gibt einen Kontext für den Container an, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="a76cd-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="a76cd-123">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a76cd-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="a76cd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a76cd-124">-Force</span></span>
<span data-ttu-id="a76cd-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a76cd-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a76cd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a76cd-126">-Name</span></span>
<span data-ttu-id="a76cd-127">Gibt den Namen des zu entfernenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="a76cd-127">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="a76cd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a76cd-128">-PassThru</span></span>
<span data-ttu-id="a76cd-129">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a76cd-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a76cd-130">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a76cd-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a76cd-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a76cd-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a76cd-132">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a76cd-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a76cd-133">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a76cd-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a76cd-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a76cd-134">-Confirm</span></span>
<span data-ttu-id="a76cd-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a76cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76cd-136">-WhatIf</span></span>
<span data-ttu-id="a76cd-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a76cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76cd-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a76cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76cd-139">CommonParameters</span></span>
<span data-ttu-id="a76cd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76cd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76cd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a76cd-142">INPUTS</span></span>

## <span data-ttu-id="a76cd-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a76cd-143">OUTPUTS</span></span>

## <span data-ttu-id="a76cd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a76cd-144">NOTES</span></span>

## <span data-ttu-id="a76cd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a76cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="a76cd-146">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a76cd-146">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="a76cd-147">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a76cd-147">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
