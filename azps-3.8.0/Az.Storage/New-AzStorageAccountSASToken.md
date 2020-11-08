---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003344"
---
# <span data-ttu-id="222f3-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="222f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="222f3-102">SYNOPSIS</span></span>
<span data-ttu-id="222f3-103">Erstellt ein SAS-Token auf Kontoebene.</span><span class="sxs-lookup"><span data-stu-id="222f3-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="222f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="222f3-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="222f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="222f3-105">DESCRIPTION</span></span>
<span data-ttu-id="222f3-106">Das Cmdlet **New-AzStorageSASToken** erstellt ein SAS-Token (Shared Access Signature) auf Kontoebene für ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="222f3-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="222f3-107">Sie können das SAS-Token verwenden, um Berechtigungen für mehrere Dienste zu delegieren oder um Berechtigungen für Dienste zu delegieren, die nicht mit einem SAS-Token auf Objektebene verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="222f3-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="222f3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="222f3-108">EXAMPLES</span></span>

### <span data-ttu-id="222f3-109">Beispiel 1: Erstellen eines SAS-Tokens auf Kontoebene mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="222f3-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="222f3-110">Mit diesem Befehl wird ein SAS-Token auf Kontoebene mit der vollständigen Berechtigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="222f3-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="222f3-111">Beispiel 2: Erstellen eines SAS-Tokens auf Kontoebene für einen Bereich von IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="222f3-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="222f3-112">Mit diesem Befehl wird ein SAS-Token auf Kontoebene für reine HTTPS-Anforderungen aus dem angegebenen Bereich von IP-Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="222f3-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="222f3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="222f3-113">PARAMETERS</span></span>

### <span data-ttu-id="222f3-114">-Context</span><span class="sxs-lookup"><span data-stu-id="222f3-114">-Context</span></span>
<span data-ttu-id="222f3-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="222f3-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="222f3-116">Sie können das New-AzStorageContext-Cmdlet verwenden, um ein **AzureStorageContext** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="222f3-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="222f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222f3-117">-DefaultProfile</span></span>
<span data-ttu-id="222f3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="222f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="222f3-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="222f3-119">-ExpiryTime</span></span>
<span data-ttu-id="222f3-120">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="222f3-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="222f3-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="222f3-121">-IPAddressOrRange</span></span>
<span data-ttu-id="222f3-122">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="222f3-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="222f3-123">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="222f3-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="222f3-124">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="222f3-124">-Permission</span></span>
<span data-ttu-id="222f3-125">Gibt die Berechtigungen für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="222f3-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="222f3-126">Berechtigungen sind nur gültig, wenn Sie dem angegebenen Ressourcentyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="222f3-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="222f3-127">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="222f3-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="222f3-128">Weitere Informationen zu akzeptablen Berechtigungs Werten finden Sie unter Erstellen einer Konto-SAS. http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="222f3-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="222f3-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="222f3-129">-Protocol</span></span>
<span data-ttu-id="222f3-130">Gibt das Protokoll an, das für eine Anforderung mit dem Konto SAS zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="222f3-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="222f3-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="222f3-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="222f3-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="222f3-132">HttpsOnly</span></span>
- <span data-ttu-id="222f3-133">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="222f3-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222f3-134">-</span><span class="sxs-lookup"><span data-stu-id="222f3-134">-ResourceType</span></span>
<span data-ttu-id="222f3-135">Gibt die Ressourcentypen an, die mit dem SAS-Token verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="222f3-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="222f3-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="222f3-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="222f3-137">Keine</span><span class="sxs-lookup"><span data-stu-id="222f3-137">None</span></span>
- <span data-ttu-id="222f3-138">Dienst</span><span class="sxs-lookup"><span data-stu-id="222f3-138">Service</span></span>
- <span data-ttu-id="222f3-139">Container</span><span class="sxs-lookup"><span data-stu-id="222f3-139">Container</span></span>
- <span data-ttu-id="222f3-140">Objekt</span><span class="sxs-lookup"><span data-stu-id="222f3-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222f3-141">-Service</span><span class="sxs-lookup"><span data-stu-id="222f3-141">-Service</span></span>
<span data-ttu-id="222f3-142">Gibt den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="222f3-142">Specifies the service.</span></span>
<span data-ttu-id="222f3-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="222f3-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="222f3-144">Keine</span><span class="sxs-lookup"><span data-stu-id="222f3-144">None</span></span>
- <span data-ttu-id="222f3-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="222f3-145">Blob</span></span>
- <span data-ttu-id="222f3-146">Datei</span><span class="sxs-lookup"><span data-stu-id="222f3-146">File</span></span>
- <span data-ttu-id="222f3-147">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="222f3-147">Queue</span></span>
- <span data-ttu-id="222f3-148">Tabelle</span><span class="sxs-lookup"><span data-stu-id="222f3-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222f3-149">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="222f3-149">-StartTime</span></span>
<span data-ttu-id="222f3-150">Gibt die Uhrzeit als **DateTime** -Objekt an, bei dem die SAS gültig wird.</span><span class="sxs-lookup"><span data-stu-id="222f3-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="222f3-151">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="222f3-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="222f3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222f3-152">CommonParameters</span></span>
<span data-ttu-id="222f3-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="222f3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222f3-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222f3-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222f3-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="222f3-155">INPUTS</span></span>

### <span data-ttu-id="222f3-156">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="222f3-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="222f3-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="222f3-157">OUTPUTS</span></span>

### <span data-ttu-id="222f3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="222f3-158">System.String</span></span>

## <span data-ttu-id="222f3-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="222f3-159">NOTES</span></span>

## <span data-ttu-id="222f3-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="222f3-160">RELATED LINKS</span></span>

[<span data-ttu-id="222f3-161">Neu – AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="222f3-162">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="222f3-163">Neu – AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="222f3-164">Neu – AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="222f3-165">Neu – AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="222f3-166">Neu – AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="222f3-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


