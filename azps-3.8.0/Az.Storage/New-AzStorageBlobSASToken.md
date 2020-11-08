---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003343"
---
# <span data-ttu-id="a8282-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a8282-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="a8282-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8282-102">SYNOPSIS</span></span>
<span data-ttu-id="a8282-103">Generiert ein SAS-Token für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="a8282-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="a8282-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8282-104">SYNTAX</span></span>

### <span data-ttu-id="a8282-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8282-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8282-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="a8282-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8282-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="a8282-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8282-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="a8282-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8282-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8282-109">DESCRIPTION</span></span>
<span data-ttu-id="a8282-110">Das Cmdlet **New-AzStorageBlobSASToken** generiert ein SAS-Token (Shared Access Signature) für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="a8282-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="a8282-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8282-111">EXAMPLES</span></span>

### <span data-ttu-id="a8282-112">Beispiel 1: Generieren eines BLOB-SAS-Tokens mit vollständiger BLOB-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a8282-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="a8282-113">In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger BLOB-Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="a8282-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="a8282-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="a8282-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="a8282-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="a8282-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="a8282-116">Beispiel 3: Generieren eines Benutzer Identitäts-SAS-Tokens mit Speicherkontext basierend auf der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a8282-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="a8282-117">In diesem Beispiel wird ein BLOB-SAS-Token für Benutzeridentität mit Speicherkontext generiert, das auf der OAuth-Authentifizierung basiert.</span><span class="sxs-lookup"><span data-stu-id="a8282-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="a8282-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8282-118">PARAMETERS</span></span>

### <span data-ttu-id="a8282-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a8282-119">-Blob</span></span>
<span data-ttu-id="a8282-120">Gibt den Speicher-BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="a8282-120">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a8282-121">-CloudBlob</span></span>
<span data-ttu-id="a8282-122">Gibt das **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a8282-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="a8282-123">Verwenden Sie das Cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) , um ein **CloudBlob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8282-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-124">-Container</span><span class="sxs-lookup"><span data-stu-id="a8282-124">-Container</span></span>
<span data-ttu-id="a8282-125">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="a8282-125">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-126">-Context</span><span class="sxs-lookup"><span data-stu-id="a8282-126">-Context</span></span>
<span data-ttu-id="a8282-127">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a8282-127">Specifies the storage context.</span></span>
<span data-ttu-id="a8282-128">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, wird ein BLOB-SAS-Token für die Benutzeridentität generiert.</span><span class="sxs-lookup"><span data-stu-id="a8282-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="a8282-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8282-129">-DefaultProfile</span></span>
<span data-ttu-id="a8282-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8282-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8282-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a8282-131">-ExpiryTime</span></span>
<span data-ttu-id="a8282-132">Gibt an, wann die freigegebene zugriffssignatur abläuft.</span><span class="sxs-lookup"><span data-stu-id="a8282-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="a8282-133">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, muss die Ablaufzeit in sieben Tagen ab der aktuellen Uhrzeit liegen und darf nicht älter als die aktuelle Uhrzeit sein.</span><span class="sxs-lookup"><span data-stu-id="a8282-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="a8282-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a8282-134">-FullUri</span></span>
<span data-ttu-id="a8282-135">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a8282-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="a8282-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a8282-136">-IPAddressOrRange</span></span>
<span data-ttu-id="a8282-137">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8282-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a8282-138">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="a8282-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="a8282-139">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a8282-139">-Permission</span></span>
<span data-ttu-id="a8282-140">Gibt die Berechtigungen für ein Speicher-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a8282-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="a8282-141">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="a8282-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-142">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a8282-142">-Policy</span></span>
<span data-ttu-id="a8282-143">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="a8282-143">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-144">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a8282-144">-Protocol</span></span>
<span data-ttu-id="a8282-145">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="a8282-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a8282-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a8282-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a8282-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a8282-147">HttpsOnly</span></span>
* <span data-ttu-id="a8282-148">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a8282-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a8282-149">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="a8282-149">-StartTime</span></span>
<span data-ttu-id="a8282-150">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="a8282-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="a8282-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8282-151">-Confirm</span></span>
<span data-ttu-id="a8282-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8282-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8282-153">-WhatIf</span></span>
<span data-ttu-id="a8282-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8282-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8282-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8282-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8282-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8282-156">CommonParameters</span></span>
<span data-ttu-id="a8282-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8282-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8282-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8282-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8282-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8282-159">INPUTS</span></span>

### <span data-ttu-id="a8282-160">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a8282-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a8282-161">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8282-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a8282-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8282-162">OUTPUTS</span></span>

### <span data-ttu-id="a8282-163">System. String</span><span class="sxs-lookup"><span data-stu-id="a8282-163">System.String</span></span>

## <span data-ttu-id="a8282-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8282-164">NOTES</span></span>

## <span data-ttu-id="a8282-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8282-165">RELATED LINKS</span></span>

[<span data-ttu-id="a8282-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a8282-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a8282-167">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a8282-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
