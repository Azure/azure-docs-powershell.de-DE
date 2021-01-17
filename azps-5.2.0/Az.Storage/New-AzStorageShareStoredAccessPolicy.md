---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304080"
---
# <span data-ttu-id="4561e-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4561e-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4561e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4561e-102">SYNOPSIS</span></span>
<span data-ttu-id="4561e-103">Erstellt eine Richtlinie für den gespeicherten Zugriff auf einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="4561e-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="4561e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4561e-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4561e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4561e-105">DESCRIPTION</span></span>
<span data-ttu-id="4561e-106">Das **Cmdlet "New-AzStorageShareStoredAccessPolicy"** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="4561e-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="4561e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4561e-107">EXAMPLES</span></span>

### <span data-ttu-id="4561e-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="4561e-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="4561e-109">Mit diesem Befehl wird eine gespeicherte Zugriffsrichtlinie erstellt, die über die vollständigen Berechtigungen für eine Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="4561e-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="4561e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4561e-110">PARAMETERS</span></span>

### <span data-ttu-id="4561e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4561e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4561e-112">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="4561e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4561e-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4561e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4561e-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4561e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4561e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4561e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4561e-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="4561e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4561e-117">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4561e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4561e-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4561e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4561e-119">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4561e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4561e-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4561e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4561e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4561e-121">-Context</span></span>
<span data-ttu-id="4561e-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4561e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4561e-123">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="4561e-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4561e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4561e-124">-DefaultProfile</span></span>
<span data-ttu-id="4561e-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4561e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4561e-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4561e-126">-ExpiryTime</span></span>
<span data-ttu-id="4561e-127">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4561e-128">-Permission</span><span class="sxs-lookup"><span data-stu-id="4561e-128">-Permission</span></span>
<span data-ttu-id="4561e-129">Gibt Berechtigungen in der Richtlinie für gespeicherten Zugriff für den Zugriff auf die Speicherfreigabe oder die dateien unter dieser Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4561e-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="4561e-130">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="4561e-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4561e-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="4561e-131">-Policy</span></span>
<span data-ttu-id="4561e-132">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4561e-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4561e-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4561e-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4561e-134">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4561e-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4561e-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4561e-135">-ShareName</span></span>
<span data-ttu-id="4561e-136">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="4561e-136">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4561e-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4561e-137">-StartTime</span></span>
<span data-ttu-id="4561e-138">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="4561e-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4561e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4561e-139">CommonParameters</span></span>
<span data-ttu-id="4561e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4561e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4561e-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4561e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4561e-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4561e-142">INPUTS</span></span>

### <span data-ttu-id="4561e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4561e-143">System.String</span></span>

### <span data-ttu-id="4561e-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4561e-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4561e-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4561e-145">OUTPUTS</span></span>

### <span data-ttu-id="4561e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4561e-146">System.String</span></span>

## <span data-ttu-id="4561e-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4561e-147">NOTES</span></span>

## <span data-ttu-id="4561e-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4561e-148">RELATED LINKS</span></span>

[<span data-ttu-id="4561e-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4561e-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4561e-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4561e-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4561e-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4561e-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4561e-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4561e-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
