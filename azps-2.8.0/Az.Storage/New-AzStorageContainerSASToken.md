---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: eb84c4c00e54d06588a82f10bad824737e8546f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826723"
---
# <span data-ttu-id="01f13-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="01f13-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="01f13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01f13-102">SYNOPSIS</span></span>
<span data-ttu-id="01f13-103">Generiert ein SAS-Token für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="01f13-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="01f13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f13-104">SYNTAX</span></span>

### <span data-ttu-id="01f13-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="01f13-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01f13-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="01f13-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f13-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01f13-107">DESCRIPTION</span></span>
<span data-ttu-id="01f13-108">Das Cmdlet **New-AzStorageContainerSASToken** generiert ein SAS-Token (Shared Access Signature) für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="01f13-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="01f13-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f13-109">EXAMPLES</span></span>

### <span data-ttu-id="01f13-110">Beispiel 1: Generieren eines Container-SAS-Tokens mit der Berechtigung "vollständiger Container"</span><span class="sxs-lookup"><span data-stu-id="01f13-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="01f13-111">In diesem Beispiel wird ein Container-SAS-Token mit vollständiger Container Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="01f13-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="01f13-112">Beispiel 2: generieren mehrerer Container-SAS-Tokens nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="01f13-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="01f13-113">In diesem Beispiel werden mehrere Container-SAS-Token mithilfe der Pipeline generiert.</span><span class="sxs-lookup"><span data-stu-id="01f13-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="01f13-114">Beispiel 3: Erstellen eines Container-SAS-Tokens mit Shared Access-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="01f13-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="01f13-115">In diesem Beispiel wird ein Container-SAS-Token mit einer gemeinsamen Zugriffsrichtlinie generiert.</span><span class="sxs-lookup"><span data-stu-id="01f13-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="01f13-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f13-116">PARAMETERS</span></span>

### <span data-ttu-id="01f13-117">-Context</span><span class="sxs-lookup"><span data-stu-id="01f13-117">-Context</span></span>
<span data-ttu-id="01f13-118">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="01f13-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="01f13-119">Sie können es mithilfe des New-AzStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="01f13-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="01f13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f13-120">-DefaultProfile</span></span>
<span data-ttu-id="01f13-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01f13-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f13-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="01f13-122">-ExpiryTime</span></span>
<span data-ttu-id="01f13-123">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="01f13-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="01f13-124">Wenn der Benutzer die Startzeit, aber nicht die Ablaufzeit festlegt, wird die Ablaufzeit auf die Startzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01f13-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="01f13-125">Wenn weder die Startzeit noch die Ablaufzeit angegeben ist, wird die Verfallszeit auf die aktuelle Uhrzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01f13-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="01f13-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="01f13-126">-FullUri</span></span>
<span data-ttu-id="01f13-127">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="01f13-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="01f13-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="01f13-128">-IPAddressOrRange</span></span>
<span data-ttu-id="01f13-129">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="01f13-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="01f13-130">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="01f13-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="01f13-131">-Name</span><span class="sxs-lookup"><span data-stu-id="01f13-131">-Name</span></span>
<span data-ttu-id="01f13-132">Gibt den Namen eines Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="01f13-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01f13-133">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="01f13-133">-Permission</span></span>
<span data-ttu-id="01f13-134">Gibt Berechtigungen für einen Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="01f13-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="01f13-135">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="01f13-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="01f13-136">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="01f13-136">-Policy</span></span>
<span data-ttu-id="01f13-137">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="01f13-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="01f13-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="01f13-138">-Protocol</span></span>
<span data-ttu-id="01f13-139">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="01f13-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="01f13-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="01f13-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="01f13-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="01f13-141">HttpsOnly</span></span>
* <span data-ttu-id="01f13-142">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="01f13-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="01f13-143">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="01f13-143">-StartTime</span></span>
<span data-ttu-id="01f13-144">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="01f13-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="01f13-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f13-145">CommonParameters</span></span>
<span data-ttu-id="01f13-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f13-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f13-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f13-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f13-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01f13-148">INPUTS</span></span>

### <span data-ttu-id="01f13-149">System. String</span><span class="sxs-lookup"><span data-stu-id="01f13-149">System.String</span></span>

### <span data-ttu-id="01f13-150">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01f13-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01f13-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01f13-151">OUTPUTS</span></span>

### <span data-ttu-id="01f13-152">System. String</span><span class="sxs-lookup"><span data-stu-id="01f13-152">System.String</span></span>

## <span data-ttu-id="01f13-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="01f13-153">NOTES</span></span>

## <span data-ttu-id="01f13-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01f13-154">RELATED LINKS</span></span>

[<span data-ttu-id="01f13-155">Neu – AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="01f13-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
