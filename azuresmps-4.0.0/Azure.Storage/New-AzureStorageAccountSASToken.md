---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475642"
---
# <span data-ttu-id="a7eac-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="a7eac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7eac-102">SYNOPSIS</span></span>
<span data-ttu-id="a7eac-103">Erstellt ein SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="a7eac-103">Creates an SAS token.</span></span>

## <span data-ttu-id="a7eac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7eac-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7eac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7eac-105">DESCRIPTION</span></span>
<span data-ttu-id="a7eac-106">Das Cmdlet **New-AzureStorageSASToken** erstellt ein SAS-Token (Shared Access Signature) auf Kontoebene für ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="a7eac-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="a7eac-107">Sie können das SAS-Token verwenden, um Berechtigungen für mehrere Dienste zu delegieren oder um Berechtigungen für Dienste zu delegieren, die nicht mit einem SAS-Token auf Objektebene verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a7eac-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="a7eac-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7eac-108">EXAMPLES</span></span>

### <span data-ttu-id="a7eac-109">Beispiel 1: Erstellen eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="a7eac-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="a7eac-110">Mit diesem Befehl wird ein SAS-Token auf Kontoebene mit der vollständigen Berechtigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7eac-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="a7eac-111">Beispiel 2: Erstellen eines SAS-Tokens für einen Bereich von IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="a7eac-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="a7eac-112">Mit diesem Befehl wird ein SAS-Token für nur-HTTPS-Anforderungen aus dem angegebenen IP-Adressbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7eac-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="a7eac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7eac-113">PARAMETERS</span></span>

### <span data-ttu-id="a7eac-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a7eac-114">-Context</span></span>
<span data-ttu-id="a7eac-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a7eac-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a7eac-116">Sie können das New-AzureStorageContext-Cmdlet verwenden, um ein **AzureStorageContext** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7eac-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="a7eac-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a7eac-117">-ExpiryTime</span></span>
<span data-ttu-id="a7eac-118">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="a7eac-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a7eac-119">-IPAddressOrRange</span></span>
<span data-ttu-id="a7eac-120">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7eac-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a7eac-121">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="a7eac-121">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-122">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a7eac-122">-Permission</span></span>
<span data-ttu-id="a7eac-123">Gibt die Berechtigungen für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="a7eac-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="a7eac-124">Berechtigungen sind nur gültig, wenn Sie dem angegebenen Ressourcentyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a7eac-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="a7eac-125">Weitere Informationen zu akzeptablen Berechtigungs Werten finden Sie unter Erstellen einer Konto-SAS.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="a7eac-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a7eac-126">-Protocol</span></span>
<span data-ttu-id="a7eac-127">Gibt das Protokoll an, das für eine Anforderung mit dem Konto SAS zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a7eac-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="a7eac-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a7eac-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7eac-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a7eac-129">HttpsOnly</span></span>
- <span data-ttu-id="a7eac-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="a7eac-130">HttpsOrHttp</span></span>

<span data-ttu-id="a7eac-131">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a7eac-131">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-132">-</span><span class="sxs-lookup"><span data-stu-id="a7eac-132">-ResourceType</span></span>
<span data-ttu-id="a7eac-133">Gibt die Ressourcentypen an, die mit dem SAS-Token verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a7eac-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="a7eac-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a7eac-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7eac-135">Keine</span><span class="sxs-lookup"><span data-stu-id="a7eac-135">None</span></span>
- <span data-ttu-id="a7eac-136">Dienst</span><span class="sxs-lookup"><span data-stu-id="a7eac-136">Service</span></span>
- <span data-ttu-id="a7eac-137">Container</span><span class="sxs-lookup"><span data-stu-id="a7eac-137">Container</span></span>
- <span data-ttu-id="a7eac-138">Objekt</span><span class="sxs-lookup"><span data-stu-id="a7eac-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-139">-Service</span><span class="sxs-lookup"><span data-stu-id="a7eac-139">-Service</span></span>
<span data-ttu-id="a7eac-140">Gibt den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="a7eac-140">Specifies the service.</span></span>
<span data-ttu-id="a7eac-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a7eac-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7eac-142">Keine</span><span class="sxs-lookup"><span data-stu-id="a7eac-142">None</span></span>
- <span data-ttu-id="a7eac-143">BLOB</span><span class="sxs-lookup"><span data-stu-id="a7eac-143">Blob</span></span>
- <span data-ttu-id="a7eac-144">Datei</span><span class="sxs-lookup"><span data-stu-id="a7eac-144">File</span></span>
- <span data-ttu-id="a7eac-145">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="a7eac-145">Queue</span></span>
- <span data-ttu-id="a7eac-146">Tabelle</span><span class="sxs-lookup"><span data-stu-id="a7eac-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-147">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="a7eac-147">-StartTime</span></span>
<span data-ttu-id="a7eac-148">Gibt die Uhrzeit als **DateTime** -Objekt an, bei dem die SAS gültig wird.</span><span class="sxs-lookup"><span data-stu-id="a7eac-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="a7eac-149">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7eac-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eac-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7eac-150">CommonParameters</span></span>
<span data-ttu-id="a7eac-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7eac-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7eac-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7eac-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7eac-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7eac-153">INPUTS</span></span>

## <span data-ttu-id="a7eac-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7eac-154">OUTPUTS</span></span>

## <span data-ttu-id="a7eac-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7eac-155">NOTES</span></span>

## <span data-ttu-id="a7eac-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7eac-156">RELATED LINKS</span></span>

[<span data-ttu-id="a7eac-157">Neu – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="a7eac-158">Neu – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="a7eac-159">Neu – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="a7eac-160">Neu – AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="a7eac-161">Neu – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="a7eac-162">Neu – AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="a7eac-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


