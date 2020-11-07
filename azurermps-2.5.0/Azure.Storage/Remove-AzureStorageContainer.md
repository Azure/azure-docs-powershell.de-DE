---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 24eba8b6aeedb2f240fbd7da16b1b7a76ee9d759
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850495"
---
# <span data-ttu-id="46cee-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46cee-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="46cee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46cee-102">SYNOPSIS</span></span>
<span data-ttu-id="46cee-103">Entfernt den angegebenen Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="46cee-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46cee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46cee-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46cee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46cee-105">DESCRIPTION</span></span>
<span data-ttu-id="46cee-106">Das Cmdlet **Remove-AzureStorageContainer** entfernt den angegebenen Speichercontainer in Azure.</span><span class="sxs-lookup"><span data-stu-id="46cee-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="46cee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46cee-107">EXAMPLES</span></span>

### <span data-ttu-id="46cee-108">Beispiel 1: Entfernen eines Containers</span><span class="sxs-lookup"><span data-stu-id="46cee-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="46cee-109">In diesem Beispiel wird ein Container mit dem Namen MyTestContainer entfernt.</span><span class="sxs-lookup"><span data-stu-id="46cee-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="46cee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46cee-110">PARAMETERS</span></span>

### <span data-ttu-id="46cee-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46cee-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="46cee-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="46cee-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="46cee-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="46cee-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="46cee-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="46cee-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="46cee-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="46cee-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="46cee-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="46cee-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="46cee-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="46cee-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="46cee-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="46cee-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="46cee-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="46cee-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="46cee-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="46cee-120">The default value is 10.</span></span>

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

### <span data-ttu-id="46cee-121">-Context</span><span class="sxs-lookup"><span data-stu-id="46cee-121">-Context</span></span>
<span data-ttu-id="46cee-122">Gibt einen Kontext für den Container an, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="46cee-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="46cee-123">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46cee-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="46cee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46cee-124">-DefaultProfile</span></span>
<span data-ttu-id="46cee-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46cee-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cee-126">-Force</span><span class="sxs-lookup"><span data-stu-id="46cee-126">-Force</span></span>
<span data-ttu-id="46cee-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="46cee-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46cee-128">-Name</span><span class="sxs-lookup"><span data-stu-id="46cee-128">-Name</span></span>
<span data-ttu-id="46cee-129">Gibt den Namen des zu entfernenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="46cee-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46cee-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46cee-130">-PassThru</span></span>
<span data-ttu-id="46cee-131">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="46cee-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="46cee-132">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46cee-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="46cee-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46cee-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="46cee-134">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="46cee-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="46cee-135">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="46cee-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="46cee-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46cee-136">-Confirm</span></span>
<span data-ttu-id="46cee-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46cee-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cee-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46cee-138">-WhatIf</span></span>
<span data-ttu-id="46cee-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46cee-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46cee-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46cee-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cee-141">CommonParameters</span></span>
<span data-ttu-id="46cee-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46cee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cee-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46cee-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cee-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46cee-144">INPUTS</span></span>

### <span data-ttu-id="46cee-145">System. String</span><span class="sxs-lookup"><span data-stu-id="46cee-145">System.String</span></span>

### <span data-ttu-id="46cee-146">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46cee-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46cee-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46cee-147">OUTPUTS</span></span>

### <span data-ttu-id="46cee-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46cee-148">System.Boolean</span></span>

## <span data-ttu-id="46cee-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="46cee-149">NOTES</span></span>

## <span data-ttu-id="46cee-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46cee-150">RELATED LINKS</span></span>

[<span data-ttu-id="46cee-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46cee-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="46cee-152">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46cee-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
