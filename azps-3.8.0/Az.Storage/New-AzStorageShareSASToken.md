---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003664"
---
# <span data-ttu-id="0062d-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="0062d-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="0062d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0062d-102">SYNOPSIS</span></span>
<span data-ttu-id="0062d-103">Generieren des Shared Access-Signaturtokens für die Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0062d-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="0062d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0062d-104">SYNTAX</span></span>

### <span data-ttu-id="0062d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="0062d-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0062d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="0062d-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0062d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0062d-107">DESCRIPTION</span></span>
<span data-ttu-id="0062d-108">Das Cmdlet **New-AzStorageShareSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0062d-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="0062d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0062d-109">EXAMPLES</span></span>

### <span data-ttu-id="0062d-110">Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens für eine Freigabe</span><span class="sxs-lookup"><span data-stu-id="0062d-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="0062d-111">Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Freigabe mit dem Namen ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="0062d-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="0062d-112">Beispiel 2: generieren mehrerer freigegebener zugriffssignatur Token mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="0062d-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="0062d-113">Dieser Befehl ruft alle Speicherfreigaben ab, die dem Präfix Test entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0062d-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="0062d-114">Der Befehl übergibt Sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0062d-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0062d-115">Das aktuelle Cmdlet erstellt ein freigegebenes Zugriffstoken für jede Speicherfreigabe, die über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0062d-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="0062d-116">Beispiel 3: Generieren eines freigegebenen zugriffssignatur Tokens, das eine freigegebene Zugriffsrichtlinie verwendet</span><span class="sxs-lookup"><span data-stu-id="0062d-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="0062d-117">Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Speicherfreigabe mit dem Namen ContosoShare, die die Richtlinie mit dem Namen ContosoPolicy03 hat.</span><span class="sxs-lookup"><span data-stu-id="0062d-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="0062d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0062d-118">PARAMETERS</span></span>

### <span data-ttu-id="0062d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="0062d-119">-Context</span></span>
<span data-ttu-id="0062d-120">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="0062d-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0062d-121">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0062d-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0062d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0062d-122">-DefaultProfile</span></span>
<span data-ttu-id="0062d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0062d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0062d-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0062d-124">-ExpiryTime</span></span>
<span data-ttu-id="0062d-125">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="0062d-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="0062d-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="0062d-126">-FullUri</span></span>
<span data-ttu-id="0062d-127">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0062d-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="0062d-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0062d-128">-IPAddressOrRange</span></span>
<span data-ttu-id="0062d-129">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="0062d-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0062d-130">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="0062d-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="0062d-131">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="0062d-131">-Permission</span></span>
<span data-ttu-id="0062d-132">Gibt die Berechtigungen im Token an, um auf die Freigabe und die Dateien unter der Freigabe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0062d-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="0062d-133">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="0062d-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0062d-134">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0062d-134">-Policy</span></span>
<span data-ttu-id="0062d-135">Gibt die gespeicherte Zugriffsrichtlinie für eine Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="0062d-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0062d-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0062d-136">-Protocol</span></span>
<span data-ttu-id="0062d-137">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="0062d-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="0062d-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0062d-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="0062d-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0062d-139">HttpsOnly</span></span>
* <span data-ttu-id="0062d-140">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="0062d-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="0062d-141">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="0062d-141">-ShareName</span></span>
<span data-ttu-id="0062d-142">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="0062d-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="0062d-143">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0062d-143">-StartTime</span></span>
<span data-ttu-id="0062d-144">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="0062d-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="0062d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0062d-145">CommonParameters</span></span>
<span data-ttu-id="0062d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0062d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0062d-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0062d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0062d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0062d-148">INPUTS</span></span>

### <span data-ttu-id="0062d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0062d-149">System.String</span></span>

### <span data-ttu-id="0062d-150">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0062d-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0062d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0062d-151">OUTPUTS</span></span>

### <span data-ttu-id="0062d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0062d-152">System.String</span></span>

## <span data-ttu-id="0062d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="0062d-153">NOTES</span></span>
* <span data-ttu-id="0062d-154">Schlüsselwörter: Common, Azure, Dienste, Daten, Speicher, BLOB, Warteschlange, Tabelle</span><span class="sxs-lookup"><span data-stu-id="0062d-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="0062d-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0062d-155">RELATED LINKS</span></span>

[<span data-ttu-id="0062d-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0062d-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0062d-157">Neu – AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="0062d-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
