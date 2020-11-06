---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: da9394d4d255a4ac09c8de437ee72b9d399cda35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496725"
---
# <span data-ttu-id="1e1eb-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="1e1eb-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="1e1eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1eb-103">Generiert ein freigegebenes zugriffssignatur Token für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e1eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e1eb-104">SYNTAX</span></span>

### <span data-ttu-id="1e1eb-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="1e1eb-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1e1eb-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="1e1eb-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="1e1eb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e1eb-107">DESCRIPTION</span></span>
<span data-ttu-id="1e1eb-108">Das Cmdlet **New-AzureStorageQueueSASToken** generiert das Shared Access-Signaturtoken für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="1e1eb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e1eb-109">EXAMPLES</span></span>

### <span data-ttu-id="1e1eb-110">Beispiel 1: Generieren eines SAS-Warteschlangen Tokens mit vollständiger Berechtigung</span><span class="sxs-lookup"><span data-stu-id="1e1eb-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="1e1eb-111">In diesem Beispiel wird ein Warteschlangen-SAS-Token mit vollständiger Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="1e1eb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e1eb-112">PARAMETERS</span></span>

### <span data-ttu-id="1e1eb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1e1eb-113">-Context</span></span>
<span data-ttu-id="1e1eb-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1e1eb-115">Sie können es über New-AzureStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1e1eb-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1e1eb-116">-ExpiryTime</span></span>
<span data-ttu-id="1e1eb-117">Gibt an, wann die freigegebene zugriffssignatur nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="1e1eb-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1e1eb-118">-FullUri</span></span>
<span data-ttu-id="1e1eb-119">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="1e1eb-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1e1eb-120">-IPAddressOrRange</span></span>
<span data-ttu-id="1e1eb-121">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1e1eb-122">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="1e1eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1e1eb-123">-Name</span></span>
<span data-ttu-id="1e1eb-124">Gibt den Namen einer Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e1eb-125">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="1e1eb-125">-Permission</span></span>
<span data-ttu-id="1e1eb-126">Gibt Berechtigungen für eine Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="1e1eb-127">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1e1eb-127">-Policy</span></span>
<span data-ttu-id="1e1eb-128">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="1e1eb-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1e1eb-129">-Protocol</span></span>
<span data-ttu-id="1e1eb-130">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1e1eb-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1e1eb-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1e1eb-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1e1eb-132">HttpsOnly</span></span>
* <span data-ttu-id="1e1eb-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1e1eb-133">HttpsOrHttp</span></span>

<span data-ttu-id="1e1eb-134">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1e1eb-135">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="1e1eb-135">-StartTime</span></span>
<span data-ttu-id="1e1eb-136">Gibt an, wann die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="1e1eb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1eb-137">CommonParameters</span></span>
<span data-ttu-id="1e1eb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1eb-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1eb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1eb-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e1eb-140">INPUTS</span></span>

### <span data-ttu-id="1e1eb-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e1eb-141">IStorageContext</span></span>

<span data-ttu-id="1e1eb-142">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1e1eb-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e1eb-143">String</span></span>

<span data-ttu-id="1e1eb-144">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e1eb-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1e1eb-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e1eb-145">OUTPUTS</span></span>

### <span data-ttu-id="1e1eb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1e1eb-146">System.String</span></span>

## <span data-ttu-id="1e1eb-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e1eb-147">NOTES</span></span>

## <span data-ttu-id="1e1eb-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e1eb-148">RELATED LINKS</span></span>

