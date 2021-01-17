---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471717"
---
# <span data-ttu-id="6904e-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="6904e-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="6904e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6904e-102">SYNOPSIS</span></span>
<span data-ttu-id="6904e-103">Generieren Sie das Token "Signatur für freigegebenen Zugriff" für die Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="6904e-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="6904e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6904e-104">SYNTAX</span></span>

### <span data-ttu-id="6904e-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="6904e-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6904e-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="6904e-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6904e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6904e-107">DESCRIPTION</span></span>
<span data-ttu-id="6904e-108">Das **Cmdlet "New-AzStorageShareSASToken"** generiert ein Token für die Signatur für den freigegebenen Zugriff für eine Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="6904e-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="6904e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6904e-109">EXAMPLES</span></span>

### <span data-ttu-id="6904e-110">Beispiel 1: Generieren eines Tokens für eine Signatur für den freigegebenen Zugriff für eine Freigabe</span><span class="sxs-lookup"><span data-stu-id="6904e-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="6904e-111">Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff für die Freigabe namens "ContosoShare" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6904e-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="6904e-112">Beispiel 2: Generieren mehrerer Signaturtoken für den freigegebenen Zugriff mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="6904e-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="6904e-113">Dieser Befehl ruft alle Speicherfreigaben ab, die dem Präfixtest entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6904e-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="6904e-114">Der Befehl übergibt sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6904e-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6904e-115">Das aktuelle Cmdlet erstellt ein freigegebenes Zugriffstoken für jede Speicherfreigabe mit den angegebenen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="6904e-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="6904e-116">Beispiel 3: Generieren eines Tokens für eine Signatur für den freigegebenen Zugriff, das eine Richtlinie für den freigegebenen Zugriff verwendet</span><span class="sxs-lookup"><span data-stu-id="6904e-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="6904e-117">Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff für die Speicherfreigabe namens "ContosoShare" erstellt, das die Richtlinie "ContosoPolicy03" enthält.</span><span class="sxs-lookup"><span data-stu-id="6904e-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="6904e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6904e-118">PARAMETERS</span></span>

### <span data-ttu-id="6904e-119">-Context</span><span class="sxs-lookup"><span data-stu-id="6904e-119">-Context</span></span>
<span data-ttu-id="6904e-120">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="6904e-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6904e-121">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6904e-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6904e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6904e-122">-DefaultProfile</span></span>
<span data-ttu-id="6904e-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6904e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6904e-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6904e-124">-ExpiryTime</span></span>
<span data-ttu-id="6904e-125">Gibt die Uhrzeit an, zu der die Signatur für den freigegebenen Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="6904e-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="6904e-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6904e-126">-FullUri</span></span>
<span data-ttu-id="6904e-127">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6904e-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6904e-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6904e-128">-IPAddressOrRange</span></span>
<span data-ttu-id="6904e-129">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="6904e-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6904e-130">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="6904e-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="6904e-131">-Permission</span><span class="sxs-lookup"><span data-stu-id="6904e-131">-Permission</span></span>
<span data-ttu-id="6904e-132">Gibt die Berechtigungen im Token für den Zugriff auf die Freigabe und die Dateien unter der Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="6904e-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="6904e-133">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="6904e-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6904e-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="6904e-134">-Policy</span></span>
<span data-ttu-id="6904e-135">Gibt die Richtlinie für den gespeicherten Zugriff für eine Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="6904e-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="6904e-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6904e-136">-Protocol</span></span>
<span data-ttu-id="6904e-137">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="6904e-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6904e-138">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6904e-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6904e-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6904e-139">HttpsOnly</span></span>
* <span data-ttu-id="6904e-140">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="6904e-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="6904e-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6904e-141">-ShareName</span></span>
<span data-ttu-id="6904e-142">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="6904e-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="6904e-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6904e-143">-StartTime</span></span>
<span data-ttu-id="6904e-144">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="6904e-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6904e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6904e-145">CommonParameters</span></span>
<span data-ttu-id="6904e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6904e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6904e-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6904e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6904e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6904e-148">INPUTS</span></span>

### <span data-ttu-id="6904e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6904e-149">System.String</span></span>

### <span data-ttu-id="6904e-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6904e-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6904e-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6904e-151">OUTPUTS</span></span>

### <span data-ttu-id="6904e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="6904e-152">System.String</span></span>

## <span data-ttu-id="6904e-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6904e-153">NOTES</span></span>
* <span data-ttu-id="6904e-154">Schlüsselwörter: Allgemein, Azure, Dienste, Daten, Speicher, BLOB, Warteschlange, Tabelle</span><span class="sxs-lookup"><span data-stu-id="6904e-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="6904e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6904e-155">RELATED LINKS</span></span>

[<span data-ttu-id="6904e-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="6904e-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="6904e-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="6904e-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
