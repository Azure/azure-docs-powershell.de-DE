---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374000"
---
# <span data-ttu-id="21242-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="21242-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="21242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21242-102">SYNOPSIS</span></span>
<span data-ttu-id="21242-103">Generiert ein SAS-Token für ein Azure-Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="21242-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="21242-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21242-104">SYNTAX</span></span>

### <span data-ttu-id="21242-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="21242-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21242-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="21242-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21242-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="21242-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21242-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="21242-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21242-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21242-109">DESCRIPTION</span></span>
<span data-ttu-id="21242-110">Das **Cmdlet "New-AzStorageBlobSASToken"** generiert ein SAS (Shared Access Signature)-Token für ein Azure-Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="21242-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="21242-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21242-111">EXAMPLES</span></span>

### <span data-ttu-id="21242-112">Beispiel 1: Generieren eines BLOB-SAS-Tokens mit der vollständigen BLOB-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="21242-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="21242-113">In diesem Beispiel wird ein BLOB-SAS-Token mit der vollständigen BLOB-Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="21242-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="21242-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="21242-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="21242-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="21242-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="21242-116">Beispiel 3: Generieren eines Benutzeridentitäts-SAS-Tokens mit Speicherkontext basierend auf der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="21242-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="21242-117">In diesem Beispiel wird ein BENUTZERidentitäts-BLOB-SAS-Token mit Speicherkontext generiert, der auf der OAuth-Authentifizierung basiert.</span><span class="sxs-lookup"><span data-stu-id="21242-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="21242-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21242-118">PARAMETERS</span></span>

### <span data-ttu-id="21242-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="21242-119">-Blob</span></span>
<span data-ttu-id="21242-120">Gibt den Speicher-BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="21242-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="21242-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="21242-121">-BlobBaseClient</span></span>
<span data-ttu-id="21242-122">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="21242-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21242-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="21242-123">-CloudBlob</span></span>
<span data-ttu-id="21242-124">Gibt das Objekt **"CloudBlob"** an.</span><span class="sxs-lookup"><span data-stu-id="21242-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="21242-125">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** [das Cmdlet "Get-AzStorageBlob".](./Get-AzStorageBlob.md)</span><span class="sxs-lookup"><span data-stu-id="21242-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="21242-126">-Container</span><span class="sxs-lookup"><span data-stu-id="21242-126">-Container</span></span>
<span data-ttu-id="21242-127">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="21242-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="21242-128">-Context</span><span class="sxs-lookup"><span data-stu-id="21242-128">-Context</span></span>
<span data-ttu-id="21242-129">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="21242-129">Specifies the storage context.</span></span>
<span data-ttu-id="21242-130">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, wird ein BENUTZERidentitäts-BLOB-SAS-Token generiert.</span><span class="sxs-lookup"><span data-stu-id="21242-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="21242-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21242-131">-DefaultProfile</span></span>
<span data-ttu-id="21242-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21242-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21242-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="21242-133">-ExpiryTime</span></span>
<span data-ttu-id="21242-134">Gibt an, wann die Signatur für den freigegebenen Zugriff abläuft.</span><span class="sxs-lookup"><span data-stu-id="21242-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="21242-135">Basiert der Speicherkontext auf der OAuth-Authentifizierung, muss die Ablaufzeit sieben Tage nach der aktuellen Uhrzeit und nicht vor der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="21242-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="21242-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="21242-136">-FullUri</span></span>
<span data-ttu-id="21242-137">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="21242-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="21242-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="21242-138">-IPAddressOrRange</span></span>
<span data-ttu-id="21242-139">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="21242-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="21242-140">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="21242-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="21242-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="21242-141">-Permission</span></span>
<span data-ttu-id="21242-142">Gibt die Berechtigungen für ein Speicher-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="21242-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="21242-143">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="21242-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="21242-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="21242-144">-Policy</span></span>
<span data-ttu-id="21242-145">Gibt eine Azure Stored Access Policy an.</span><span class="sxs-lookup"><span data-stu-id="21242-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="21242-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="21242-146">-Protocol</span></span>
<span data-ttu-id="21242-147">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="21242-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="21242-148">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="21242-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="21242-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="21242-149">HttpsOnly</span></span>
* <span data-ttu-id="21242-150">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="21242-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="21242-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="21242-151">-StartTime</span></span>
<span data-ttu-id="21242-152">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="21242-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="21242-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21242-153">-Confirm</span></span>
<span data-ttu-id="21242-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21242-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21242-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21242-155">-WhatIf</span></span>
<span data-ttu-id="21242-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21242-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21242-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21242-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21242-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21242-158">CommonParameters</span></span>
<span data-ttu-id="21242-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21242-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21242-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21242-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21242-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21242-161">INPUTS</span></span>

### <span data-ttu-id="21242-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="21242-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="21242-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21242-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21242-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21242-164">OUTPUTS</span></span>

### <span data-ttu-id="21242-165">System.String</span><span class="sxs-lookup"><span data-stu-id="21242-165">System.String</span></span>

## <span data-ttu-id="21242-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21242-166">NOTES</span></span>

## <span data-ttu-id="21242-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21242-167">RELATED LINKS</span></span>

[<span data-ttu-id="21242-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="21242-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="21242-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="21242-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
