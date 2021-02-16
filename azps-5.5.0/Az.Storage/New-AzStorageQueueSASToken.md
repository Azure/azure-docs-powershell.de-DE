---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162964"
---
# <span data-ttu-id="f7da7-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="f7da7-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="f7da7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7da7-102">SYNOPSIS</span></span>
<span data-ttu-id="f7da7-103">Generiert ein Token für die Signatur für den freigegebenen Zugriff für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="f7da7-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f7da7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7da7-104">SYNTAX</span></span>

### <span data-ttu-id="f7da7-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f7da7-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7da7-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f7da7-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7da7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7da7-107">DESCRIPTION</span></span>
<span data-ttu-id="f7da7-108">Das **Cmdlet "New-AzStorageQueueSASToken"** generiert das Token für die Signatur für den freigegebenen Zugriff für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="f7da7-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f7da7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7da7-109">EXAMPLES</span></span>

### <span data-ttu-id="f7da7-110">Beispiel 1: Generieren eines Warteschlangen-SAS-Tokens mit der vollen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="f7da7-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="f7da7-111">In diesem Beispiel wird ein Warteschlangen-SAS-Token mit allen Berechtigungen generiert.</span><span class="sxs-lookup"><span data-stu-id="f7da7-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="f7da7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7da7-112">PARAMETERS</span></span>

### <span data-ttu-id="f7da7-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f7da7-113">-Context</span></span>
<span data-ttu-id="f7da7-114">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f7da7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f7da7-115">Sie können sie über New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7da7-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f7da7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7da7-116">-DefaultProfile</span></span>
<span data-ttu-id="f7da7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7da7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7da7-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f7da7-118">-ExpiryTime</span></span>
<span data-ttu-id="f7da7-119">Gibt an, wann die Signatur für den freigegebenen Zugriff nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="f7da7-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="f7da7-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f7da7-120">-FullUri</span></span>
<span data-ttu-id="f7da7-121">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7da7-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f7da7-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f7da7-122">-IPAddressOrRange</span></span>
<span data-ttu-id="f7da7-123">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f7da7-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f7da7-124">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="f7da7-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="f7da7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7da7-125">-Name</span></span>
<span data-ttu-id="f7da7-126">Gibt den Namen einer Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f7da7-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="f7da7-127">-Permission</span><span class="sxs-lookup"><span data-stu-id="f7da7-127">-Permission</span></span>
<span data-ttu-id="f7da7-128">Gibt Berechtigungen für eine Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f7da7-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="f7da7-129">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="f7da7-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f7da7-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="f7da7-130">-Policy</span></span>
<span data-ttu-id="f7da7-131">Gibt eine Azure-Richtlinie für gespeicherten Zugriff an.</span><span class="sxs-lookup"><span data-stu-id="f7da7-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="f7da7-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f7da7-132">-Protocol</span></span>
<span data-ttu-id="f7da7-133">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="f7da7-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f7da7-134">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f7da7-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f7da7-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f7da7-135">HttpsOnly</span></span>
* <span data-ttu-id="f7da7-136">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="f7da7-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f7da7-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f7da7-137">-StartTime</span></span>
<span data-ttu-id="f7da7-138">Gibt an, wann die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="f7da7-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f7da7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7da7-139">CommonParameters</span></span>
<span data-ttu-id="f7da7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7da7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7da7-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7da7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7da7-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7da7-142">INPUTS</span></span>

### <span data-ttu-id="f7da7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f7da7-143">System.String</span></span>

### <span data-ttu-id="f7da7-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7da7-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f7da7-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7da7-145">OUTPUTS</span></span>

### <span data-ttu-id="f7da7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f7da7-146">System.String</span></span>

## <span data-ttu-id="f7da7-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7da7-147">NOTES</span></span>

## <span data-ttu-id="f7da7-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7da7-148">RELATED LINKS</span></span>
