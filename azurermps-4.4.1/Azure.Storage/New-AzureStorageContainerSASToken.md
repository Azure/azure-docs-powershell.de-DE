---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d7c7847a92c7bbb241046479c70d1dabb75ea685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477490"
---
# <span data-ttu-id="ca690-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ca690-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="ca690-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca690-102">SYNOPSIS</span></span>
<span data-ttu-id="ca690-103">Generiert ein SAS-Token für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="ca690-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca690-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca690-104">SYNTAX</span></span>

### <span data-ttu-id="ca690-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="ca690-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ca690-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="ca690-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ca690-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca690-107">DESCRIPTION</span></span>
<span data-ttu-id="ca690-108">Das Cmdlet **New-AzureStorageContainerSASToken** generiert ein SAS-Token (Shared Access Signature) für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="ca690-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="ca690-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca690-109">EXAMPLES</span></span>

### <span data-ttu-id="ca690-110">Beispiel 1: Generieren eines Container-SAS-Tokens mit der Berechtigung "vollständiger Container"</span><span class="sxs-lookup"><span data-stu-id="ca690-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="ca690-111">In diesem Beispiel wird ein Container-SAS-Token mit vollständiger Container Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="ca690-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="ca690-112">Beispiel 2: generieren mehrerer Container-SAS-Tokens nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca690-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="ca690-113">In diesem Beispiel werden mehrere Container-SAS-Token mithilfe der Pipeline generiert.</span><span class="sxs-lookup"><span data-stu-id="ca690-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="ca690-114">Beispiel 3: Erstellen eines Container-SAS-Tokens mit Shared Access-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca690-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="ca690-115">In diesem Beispiel wird ein Container-SAS-Token mit einer gemeinsamen Zugriffsrichtlinie generiert.</span><span class="sxs-lookup"><span data-stu-id="ca690-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="ca690-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca690-116">PARAMETERS</span></span>

### <span data-ttu-id="ca690-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ca690-117">-Context</span></span>
<span data-ttu-id="ca690-118">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ca690-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca690-119">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca690-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca690-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca690-120">-ExpiryTime</span></span>
<span data-ttu-id="ca690-121">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="ca690-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="ca690-122">Wenn der Benutzer die Startzeit, aber nicht die Ablaufzeit festlegt, wird die Ablaufzeit auf die Startzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca690-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="ca690-123">Wenn weder die Startzeit noch die Ablaufzeit angegeben ist, wird die Verfallszeit auf die aktuelle Uhrzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca690-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="ca690-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ca690-124">-FullUri</span></span>
<span data-ttu-id="ca690-125">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ca690-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ca690-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ca690-126">-IPAddressOrRange</span></span>
<span data-ttu-id="ca690-127">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="ca690-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ca690-128">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="ca690-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="ca690-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ca690-129">-Name</span></span>
<span data-ttu-id="ca690-130">Gibt den Namen eines Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="ca690-130">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="ca690-131">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ca690-131">-Permission</span></span>
<span data-ttu-id="ca690-132">Gibt Berechtigungen für einen Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="ca690-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="ca690-133">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ca690-133">-Policy</span></span>
<span data-ttu-id="ca690-134">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="ca690-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="ca690-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ca690-135">-Protocol</span></span>
<span data-ttu-id="ca690-136">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ca690-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ca690-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca690-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ca690-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ca690-138">HttpsOnly</span></span>
* <span data-ttu-id="ca690-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="ca690-139">HttpsOrHttp</span></span>

<span data-ttu-id="ca690-140">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="ca690-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ca690-141">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ca690-141">-StartTime</span></span>
<span data-ttu-id="ca690-142">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="ca690-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ca690-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca690-143">CommonParameters</span></span>
<span data-ttu-id="ca690-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca690-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca690-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca690-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca690-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca690-146">INPUTS</span></span>

### <span data-ttu-id="ca690-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca690-147">IStorageContext</span></span>

<span data-ttu-id="ca690-148">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca690-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ca690-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ca690-149">String</span></span>

<span data-ttu-id="ca690-150">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca690-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ca690-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca690-151">OUTPUTS</span></span>

### <span data-ttu-id="ca690-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ca690-152">System.String</span></span>

## <span data-ttu-id="ca690-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca690-153">NOTES</span></span>

## <span data-ttu-id="ca690-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca690-154">RELATED LINKS</span></span>

[<span data-ttu-id="ca690-155">Neu – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca690-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
