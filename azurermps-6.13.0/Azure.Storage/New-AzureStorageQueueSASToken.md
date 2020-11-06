---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: 337dcb1718cf48488115e38052c0fdfed73edc3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498618"
---
# <span data-ttu-id="6e6ff-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="6e6ff-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="6e6ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6ff-103">Generiert ein freigegebenes zugriffssignatur Token für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e6ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e6ff-104">SYNTAX</span></span>

### <span data-ttu-id="6e6ff-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="6e6ff-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e6ff-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="6e6ff-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e6ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e6ff-107">DESCRIPTION</span></span>
<span data-ttu-id="6e6ff-108">Das Cmdlet **New-AzureStorageQueueSASToken** generiert das Shared Access-Signaturtoken für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="6e6ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e6ff-109">EXAMPLES</span></span>

### <span data-ttu-id="6e6ff-110">Beispiel 1: Generieren eines SAS-Warteschlangen Tokens mit vollständiger Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6e6ff-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="6e6ff-111">In diesem Beispiel wird ein Warteschlangen-SAS-Token mit vollständiger Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="6e6ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e6ff-112">PARAMETERS</span></span>

### <span data-ttu-id="6e6ff-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6e6ff-113">-Context</span></span>
<span data-ttu-id="6e6ff-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6e6ff-115">Sie können es über New-AzureStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e6ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6ff-116">-DefaultProfile</span></span>
<span data-ttu-id="6e6ff-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e6ff-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e6ff-118">-ExpiryTime</span></span>
<span data-ttu-id="6e6ff-119">Gibt an, wann die freigegebene zugriffssignatur nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="6e6ff-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6e6ff-120">-FullUri</span></span>
<span data-ttu-id="6e6ff-121">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6e6ff-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6e6ff-122">-IPAddressOrRange</span></span>
<span data-ttu-id="6e6ff-123">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6e6ff-124">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="6e6ff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6e6ff-125">-Name</span></span>
<span data-ttu-id="6e6ff-126">Gibt den Namen einer Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e6ff-127">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6e6ff-127">-Permission</span></span>
<span data-ttu-id="6e6ff-128">Gibt Berechtigungen für eine Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="6e6ff-129">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6e6ff-130">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6e6ff-130">-Policy</span></span>
<span data-ttu-id="6e6ff-131">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="6e6ff-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="6e6ff-132">-Protocol</span></span>
<span data-ttu-id="6e6ff-133">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6e6ff-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6e6ff-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6e6ff-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6e6ff-135">HttpsOnly</span></span>
* <span data-ttu-id="6e6ff-136">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e6ff-137">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="6e6ff-137">-StartTime</span></span>
<span data-ttu-id="6e6ff-138">Gibt an, wann die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6e6ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6ff-139">CommonParameters</span></span>
<span data-ttu-id="6e6ff-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6ff-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e6ff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6ff-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e6ff-142">INPUTS</span></span>

### <span data-ttu-id="6e6ff-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6e6ff-143">System.String</span></span>

### <span data-ttu-id="6e6ff-144">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e6ff-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e6ff-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e6ff-145">OUTPUTS</span></span>

### <span data-ttu-id="6e6ff-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6e6ff-146">System.String</span></span>

## <span data-ttu-id="6e6ff-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e6ff-147">NOTES</span></span>

## <span data-ttu-id="6e6ff-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e6ff-148">RELATED LINKS</span></span>
