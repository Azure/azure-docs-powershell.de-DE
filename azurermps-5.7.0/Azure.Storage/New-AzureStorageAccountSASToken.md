---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500666"
---
# <span data-ttu-id="077e5-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="077e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="077e5-102">SYNOPSIS</span></span>
<span data-ttu-id="077e5-103">Erstellt ein SAS-Token auf Kontoebene.</span><span class="sxs-lookup"><span data-stu-id="077e5-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="077e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="077e5-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="077e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="077e5-105">DESCRIPTION</span></span>
<span data-ttu-id="077e5-106">Das Cmdlet **New-AzureStorageSASToken** erstellt ein SAS-Token (Shared Access Signature) auf Kontoebene für ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="077e5-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="077e5-107">Sie können das SAS-Token verwenden, um Berechtigungen für mehrere Dienste zu delegieren oder um Berechtigungen für Dienste zu delegieren, die nicht mit einem SAS-Token auf Objektebene verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="077e5-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="077e5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="077e5-108">EXAMPLES</span></span>

### <span data-ttu-id="077e5-109">Beispiel 1: Erstellen eines SAS-Tokens auf Kontoebene mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="077e5-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="077e5-110">Mit diesem Befehl wird ein SAS-Token auf Kontoebene mit der vollständigen Berechtigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="077e5-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="077e5-111">Beispiel 2: Erstellen eines SAS-Tokens auf Kontoebene für einen Bereich von IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="077e5-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="077e5-112">Mit diesem Befehl wird ein SAS-Token auf Kontoebene für reine HTTPS-Anforderungen aus dem angegebenen Bereich von IP-Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="077e5-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="077e5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="077e5-113">PARAMETERS</span></span>

### <span data-ttu-id="077e5-114">-Context</span><span class="sxs-lookup"><span data-stu-id="077e5-114">-Context</span></span>
<span data-ttu-id="077e5-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="077e5-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="077e5-116">Sie können das New-AzureStorageContext-Cmdlet verwenden, um ein **AzureStorageContext** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="077e5-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="077e5-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="077e5-117">-ExpiryTime</span></span>
<span data-ttu-id="077e5-118">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="077e5-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="077e5-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="077e5-119">-IPAddressOrRange</span></span>
<span data-ttu-id="077e5-120">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="077e5-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="077e5-121">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="077e5-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="077e5-122">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="077e5-122">-Permission</span></span>
<span data-ttu-id="077e5-123">Gibt die Berechtigungen für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="077e5-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="077e5-124">Berechtigungen sind nur gültig, wenn Sie dem angegebenen Ressourcentyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="077e5-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="077e5-125">Weitere Informationen zu akzeptablen Berechtigungs Werten finden Sie unter Erstellen einer Konto-SAS.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="077e5-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="077e5-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="077e5-126">-Protocol</span></span>
<span data-ttu-id="077e5-127">Gibt das Protokoll an, das für eine Anforderung mit dem Konto SAS zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="077e5-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="077e5-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="077e5-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="077e5-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="077e5-129">HttpsOnly</span></span>
- <span data-ttu-id="077e5-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="077e5-130">HttpsOrHttp</span></span>

<span data-ttu-id="077e5-131">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="077e5-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="077e5-132">-</span><span class="sxs-lookup"><span data-stu-id="077e5-132">-ResourceType</span></span>
<span data-ttu-id="077e5-133">Gibt die Ressourcentypen an, die mit dem SAS-Token verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="077e5-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="077e5-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="077e5-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="077e5-135">Keine</span><span class="sxs-lookup"><span data-stu-id="077e5-135">None</span></span>
- <span data-ttu-id="077e5-136">Dienst</span><span class="sxs-lookup"><span data-stu-id="077e5-136">Service</span></span>
- <span data-ttu-id="077e5-137">Container</span><span class="sxs-lookup"><span data-stu-id="077e5-137">Container</span></span>
- <span data-ttu-id="077e5-138">Objekt</span><span class="sxs-lookup"><span data-stu-id="077e5-138">Object</span></span>

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

### <span data-ttu-id="077e5-139">-Service</span><span class="sxs-lookup"><span data-stu-id="077e5-139">-Service</span></span>
<span data-ttu-id="077e5-140">Gibt den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="077e5-140">Specifies the service.</span></span>
<span data-ttu-id="077e5-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="077e5-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="077e5-142">Keine</span><span class="sxs-lookup"><span data-stu-id="077e5-142">None</span></span>
- <span data-ttu-id="077e5-143">BLOB</span><span class="sxs-lookup"><span data-stu-id="077e5-143">Blob</span></span>
- <span data-ttu-id="077e5-144">Datei</span><span class="sxs-lookup"><span data-stu-id="077e5-144">File</span></span>
- <span data-ttu-id="077e5-145">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="077e5-145">Queue</span></span>
- <span data-ttu-id="077e5-146">Tabelle</span><span class="sxs-lookup"><span data-stu-id="077e5-146">Table</span></span>

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

### <span data-ttu-id="077e5-147">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="077e5-147">-StartTime</span></span>
<span data-ttu-id="077e5-148">Gibt die Uhrzeit als **DateTime** -Objekt an, bei dem die SAS gültig wird.</span><span class="sxs-lookup"><span data-stu-id="077e5-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="077e5-149">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="077e5-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="077e5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077e5-150">CommonParameters</span></span>
<span data-ttu-id="077e5-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077e5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077e5-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077e5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077e5-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="077e5-153">INPUTS</span></span>

### <span data-ttu-id="077e5-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="077e5-154">IStorageContext</span></span>

<span data-ttu-id="077e5-155">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="077e5-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="077e5-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="077e5-156">OUTPUTS</span></span>

### <span data-ttu-id="077e5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="077e5-157">System.String</span></span>

## <span data-ttu-id="077e5-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="077e5-158">NOTES</span></span>

## <span data-ttu-id="077e5-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="077e5-159">RELATED LINKS</span></span>

[<span data-ttu-id="077e5-160">Neu – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="077e5-161">Neu – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="077e5-162">Neu – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="077e5-163">Neu – AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="077e5-164">Neu – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="077e5-165">Neu – AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="077e5-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


