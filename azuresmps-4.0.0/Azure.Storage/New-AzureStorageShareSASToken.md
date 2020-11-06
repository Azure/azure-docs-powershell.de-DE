---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475217"
---
# <span data-ttu-id="79133-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="79133-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="79133-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79133-102">SYNOPSIS</span></span>
<span data-ttu-id="79133-103">Generieren des Shared Access-Signaturtokens für die Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="79133-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="79133-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79133-104">SYNTAX</span></span>

### <span data-ttu-id="79133-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="79133-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="79133-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="79133-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="79133-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79133-107">DESCRIPTION</span></span>
<span data-ttu-id="79133-108">Das Cmdlet **New-AzureStorageShareSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="79133-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="79133-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79133-109">EXAMPLES</span></span>

### <span data-ttu-id="79133-110">Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens für eine Freigabe</span><span class="sxs-lookup"><span data-stu-id="79133-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="79133-111">Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Freigabe mit dem Namen ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="79133-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="79133-112">Beispiel 2: generieren mehrerer freigegebener zugriffssignatur Token mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="79133-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="79133-113">Dieser Befehl ruft alle Speicherfreigaben ab, die dem Präfix Test entsprechen.</span><span class="sxs-lookup"><span data-stu-id="79133-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="79133-114">Der Befehl übergibt Sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79133-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79133-115">Das aktuelle Cmdlet erstellt ein freigegebenes Zugriffstoken für jede Speicherfreigabe, die über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="79133-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="79133-116">Beispiel 3: Generieren eines freigegebenen zugriffssignatur Tokens, das eine freigegebene Zugriffsrichtlinie verwendet</span><span class="sxs-lookup"><span data-stu-id="79133-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="79133-117">Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Speicherfreigabe mit dem Namen ContosoShare, die die Richtlinie mit dem Namen ContosoPolicy03 hat.</span><span class="sxs-lookup"><span data-stu-id="79133-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="79133-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="79133-118">PARAMETERS</span></span>

### <span data-ttu-id="79133-119">-Context</span><span class="sxs-lookup"><span data-stu-id="79133-119">-Context</span></span>
<span data-ttu-id="79133-120">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="79133-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="79133-121">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79133-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="79133-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="79133-122">-ExpiryTime</span></span>
<span data-ttu-id="79133-123">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="79133-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="79133-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="79133-124">-FullUri</span></span>
<span data-ttu-id="79133-125">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="79133-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="79133-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="79133-126">-IPAddressOrRange</span></span>
<span data-ttu-id="79133-127">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="79133-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="79133-128">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="79133-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="79133-129">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="79133-129">-Permission</span></span>
<span data-ttu-id="79133-130">Gibt die Berechtigungen im Token an, um auf die Freigabe und die Dateien unter der Freigabe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="79133-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79133-131">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="79133-131">-Policy</span></span>
<span data-ttu-id="79133-132">Gibt die gespeicherte Zugriffsrichtlinie für eine Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="79133-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79133-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="79133-133">-Protocol</span></span>
<span data-ttu-id="79133-134">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="79133-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="79133-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79133-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="79133-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="79133-136">HttpsOnly</span></span>
* <span data-ttu-id="79133-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="79133-137">HttpsOrHttp</span></span>

<span data-ttu-id="79133-138">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="79133-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="79133-139">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="79133-139">-ShareName</span></span>
<span data-ttu-id="79133-140">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="79133-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79133-141">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="79133-141">-StartTime</span></span>
<span data-ttu-id="79133-142">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="79133-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="79133-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79133-143">CommonParameters</span></span>
<span data-ttu-id="79133-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79133-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79133-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79133-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79133-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79133-146">INPUTS</span></span>

## <span data-ttu-id="79133-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79133-147">OUTPUTS</span></span>

## <span data-ttu-id="79133-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="79133-148">NOTES</span></span>
* <span data-ttu-id="79133-149">Schlüsselwörter: Common, Azure, Dienste, Daten, Speicher, BLOB, Warteschlange, Tabelle</span><span class="sxs-lookup"><span data-stu-id="79133-149">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="79133-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79133-150">RELATED LINKS</span></span>

[<span data-ttu-id="79133-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="79133-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="79133-152">Neu – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="79133-152">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
