---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460236"
---
# <span data-ttu-id="ced2f-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced2f-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="ced2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced2f-102">SYNOPSIS</span></span>
<span data-ttu-id="ced2f-103">Entfernt den angegebenen Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="ced2f-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="ced2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ced2f-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ced2f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ced2f-105">DESCRIPTION</span></span>
<span data-ttu-id="ced2f-106">Das **Cmdlet "Remove-AzStorageContainer"** entfernt den angegebenen Speichercontainer in Azure.</span><span class="sxs-lookup"><span data-stu-id="ced2f-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="ced2f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ced2f-107">EXAMPLES</span></span>

### <span data-ttu-id="ced2f-108">Beispiel 1: Entfernen eines Containers</span><span class="sxs-lookup"><span data-stu-id="ced2f-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="ced2f-109">In diesem Beispiel wird ein Container namens "MyTestContainer" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ced2f-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="ced2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced2f-110">PARAMETERS</span></span>

### <span data-ttu-id="ced2f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ced2f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ced2f-112">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="ced2f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ced2f-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ced2f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ced2f-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ced2f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced2f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ced2f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ced2f-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="ced2f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ced2f-117">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="ced2f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ced2f-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="ced2f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ced2f-119">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="ced2f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ced2f-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="ced2f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ced2f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ced2f-121">-Context</span></span>
<span data-ttu-id="ced2f-122">Gibt einen Kontext für den Container an, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="ced2f-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="ced2f-123">Sie können das cmdlet New-AzStorageContext zum Erstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ced2f-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="ced2f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced2f-124">-DefaultProfile</span></span>
<span data-ttu-id="ced2f-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ced2f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced2f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ced2f-126">-Force</span></span>
<span data-ttu-id="ced2f-127">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="ced2f-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ced2f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ced2f-128">-Name</span></span>
<span data-ttu-id="ced2f-129">Gibt den Namen des zu entfernenden Containers an.</span><span class="sxs-lookup"><span data-stu-id="ced2f-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="ced2f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ced2f-130">-PassThru</span></span>
<span data-ttu-id="ced2f-131">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="ced2f-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ced2f-132">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ced2f-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ced2f-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ced2f-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ced2f-134">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="ced2f-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ced2f-135">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ced2f-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced2f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ced2f-136">-Confirm</span></span>
<span data-ttu-id="ced2f-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ced2f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced2f-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ced2f-138">-WhatIf</span></span>
<span data-ttu-id="ced2f-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ced2f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced2f-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ced2f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced2f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced2f-141">CommonParameters</span></span>
<span data-ttu-id="ced2f-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced2f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced2f-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced2f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced2f-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ced2f-144">INPUTS</span></span>

### <span data-ttu-id="ced2f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ced2f-145">System.String</span></span>

### <span data-ttu-id="ced2f-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ced2f-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ced2f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ced2f-147">OUTPUTS</span></span>

### <span data-ttu-id="ced2f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ced2f-148">System.Boolean</span></span>

## <span data-ttu-id="ced2f-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ced2f-149">NOTES</span></span>

## <span data-ttu-id="ced2f-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ced2f-150">RELATED LINKS</span></span>

[<span data-ttu-id="ced2f-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced2f-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ced2f-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced2f-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
