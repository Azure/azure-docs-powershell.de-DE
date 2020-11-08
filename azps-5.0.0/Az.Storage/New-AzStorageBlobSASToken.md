---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177379"
---
# <span data-ttu-id="5f53e-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5f53e-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="5f53e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f53e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f53e-103">Generiert ein SAS-Token für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="5f53e-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="5f53e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f53e-104">SYNTAX</span></span>

### <span data-ttu-id="5f53e-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f53e-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f53e-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="5f53e-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f53e-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="5f53e-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f53e-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="5f53e-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f53e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f53e-109">DESCRIPTION</span></span>
<span data-ttu-id="5f53e-110">Das Cmdlet **New-AzStorageBlobSASToken** generiert ein SAS-Token (Shared Access Signature) für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="5f53e-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="5f53e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f53e-111">EXAMPLES</span></span>

### <span data-ttu-id="5f53e-112">Beispiel 1: Generieren eines BLOB-SAS-Tokens mit vollständiger BLOB-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5f53e-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="5f53e-113">In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger BLOB-Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="5f53e-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="5f53e-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="5f53e-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="5f53e-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="5f53e-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="5f53e-116">Beispiel 3: Generieren eines Benutzer Identitäts-SAS-Tokens mit Speicherkontext basierend auf der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5f53e-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="5f53e-117">In diesem Beispiel wird ein BLOB-SAS-Token für Benutzeridentität mit Speicherkontext generiert, das auf der OAuth-Authentifizierung basiert.</span><span class="sxs-lookup"><span data-stu-id="5f53e-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="5f53e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f53e-118">PARAMETERS</span></span>

### <span data-ttu-id="5f53e-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="5f53e-119">-Blob</span></span>
<span data-ttu-id="5f53e-120">Gibt den Speicher-BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="5f53e-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="5f53e-121">-BlobBaseClient</span></span>
<span data-ttu-id="5f53e-122">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="5f53e-122">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="5f53e-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5f53e-123">-CloudBlob</span></span>
<span data-ttu-id="5f53e-124">Gibt das **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="5f53e-125">Verwenden Sie das Cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) , um ein **CloudBlob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5f53e-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="5f53e-126">-Container</span><span class="sxs-lookup"><span data-stu-id="5f53e-126">-Container</span></span>
<span data-ttu-id="5f53e-127">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="5f53e-128">-Context</span><span class="sxs-lookup"><span data-stu-id="5f53e-128">-Context</span></span>
<span data-ttu-id="5f53e-129">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-129">Specifies the storage context.</span></span>
<span data-ttu-id="5f53e-130">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, wird ein BLOB-SAS-Token für die Benutzeridentität generiert.</span><span class="sxs-lookup"><span data-stu-id="5f53e-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="5f53e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f53e-131">-DefaultProfile</span></span>
<span data-ttu-id="5f53e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f53e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f53e-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f53e-133">-ExpiryTime</span></span>
<span data-ttu-id="5f53e-134">Gibt an, wann die freigegebene zugriffssignatur abläuft.</span><span class="sxs-lookup"><span data-stu-id="5f53e-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="5f53e-135">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, muss die Ablaufzeit in sieben Tagen ab der aktuellen Uhrzeit liegen und darf nicht älter als die aktuelle Uhrzeit sein.</span><span class="sxs-lookup"><span data-stu-id="5f53e-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="5f53e-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5f53e-136">-FullUri</span></span>
<span data-ttu-id="5f53e-137">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5f53e-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5f53e-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5f53e-138">-IPAddressOrRange</span></span>
<span data-ttu-id="5f53e-139">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f53e-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5f53e-140">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="5f53e-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="5f53e-141">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5f53e-141">-Permission</span></span>
<span data-ttu-id="5f53e-142">Gibt die Berechtigungen für ein Speicher-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="5f53e-143">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="5f53e-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="5f53e-144">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5f53e-144">-Policy</span></span>
<span data-ttu-id="5f53e-145">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="5f53e-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5f53e-146">-Protocol</span></span>
<span data-ttu-id="5f53e-147">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="5f53e-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5f53e-148">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5f53e-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5f53e-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5f53e-149">HttpsOnly</span></span>
* <span data-ttu-id="5f53e-150">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5f53e-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5f53e-151">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="5f53e-151">-StartTime</span></span>
<span data-ttu-id="5f53e-152">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="5f53e-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="5f53e-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f53e-153">-Confirm</span></span>
<span data-ttu-id="5f53e-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f53e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f53e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f53e-155">-WhatIf</span></span>
<span data-ttu-id="5f53e-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f53e-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f53e-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f53e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f53e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f53e-158">CommonParameters</span></span>
<span data-ttu-id="5f53e-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f53e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f53e-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f53e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f53e-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f53e-161">INPUTS</span></span>

### <span data-ttu-id="5f53e-162">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5f53e-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="5f53e-163">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f53e-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5f53e-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f53e-164">OUTPUTS</span></span>

### <span data-ttu-id="5f53e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="5f53e-165">System.String</span></span>

## <span data-ttu-id="5f53e-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f53e-166">NOTES</span></span>

## <span data-ttu-id="5f53e-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f53e-167">RELATED LINKS</span></span>

[<span data-ttu-id="5f53e-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5f53e-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="5f53e-169">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5f53e-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
