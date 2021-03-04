---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 1dbe66bd8c34cb653fe17d01b19a2eca1b23c479
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944548"
---
# <span data-ttu-id="6adaf-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6adaf-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="6adaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adaf-102">SYNOPSIS</span></span>
<span data-ttu-id="6adaf-103">Generiert ein SAS-Token für einen Azure-Speicherblob.</span><span class="sxs-lookup"><span data-stu-id="6adaf-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="6adaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6adaf-104">SYNTAX</span></span>

### <span data-ttu-id="6adaf-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="6adaf-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adaf-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="6adaf-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adaf-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="6adaf-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adaf-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="6adaf-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6adaf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6adaf-109">DESCRIPTION</span></span>
<span data-ttu-id="6adaf-110">Das **Cmdlet New-AzStorageBlobSASToken** generiert ein Sas-Token (Shared Access Signature) für ein Azure-Speicherblob.</span><span class="sxs-lookup"><span data-stu-id="6adaf-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="6adaf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6adaf-111">EXAMPLES</span></span>

### <span data-ttu-id="6adaf-112">Beispiel 1: Generieren eines Blob-SAS-Tokens mit vollständiger Blobberechtigung</span><span class="sxs-lookup"><span data-stu-id="6adaf-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="6adaf-113">In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger Blobberechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="6adaf-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="6adaf-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="6adaf-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="6adaf-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="6adaf-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="6adaf-116">Beispiel 3: Generieren eines Benutzeridentitäts-SAS-Tokens mit Speicherkontext basierend auf der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6adaf-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="6adaf-117">In diesem Beispiel wird ein Benutzeridentitäts-BLOB-SAS-Token mit Speicherkontext generiert, der auf der OAuth-Authentifizierung basiert.</span><span class="sxs-lookup"><span data-stu-id="6adaf-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="6adaf-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6adaf-118">PARAMETERS</span></span>

### <span data-ttu-id="6adaf-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="6adaf-119">-Blob</span></span>
<span data-ttu-id="6adaf-120">Gibt den Namen des Speicherblobs an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="6adaf-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6adaf-121">-BlobBaseClient</span></span>
<span data-ttu-id="6adaf-122">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="6adaf-122">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="6adaf-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6adaf-123">-CloudBlob</span></span>
<span data-ttu-id="6adaf-124">Gibt das **CloudBlob-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="6adaf-125">Zum Abrufen eines **CloudBlob-Objekts** verwenden Sie das [Get-AzStorageBlob-Cmdlet.](./Get-AzStorageBlob.md)</span><span class="sxs-lookup"><span data-stu-id="6adaf-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="6adaf-126">-Container</span><span class="sxs-lookup"><span data-stu-id="6adaf-126">-Container</span></span>
<span data-ttu-id="6adaf-127">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="6adaf-128">-Context</span><span class="sxs-lookup"><span data-stu-id="6adaf-128">-Context</span></span>
<span data-ttu-id="6adaf-129">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-129">Specifies the storage context.</span></span>
<span data-ttu-id="6adaf-130">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, wird ein Sastoken für benutzeridentitätsblob generiert.</span><span class="sxs-lookup"><span data-stu-id="6adaf-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="6adaf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adaf-131">-DefaultProfile</span></span>
<span data-ttu-id="6adaf-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6adaf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adaf-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6adaf-133">-ExpiryTime</span></span>
<span data-ttu-id="6adaf-134">Gibt an, wann die Signatur für den freigegebenen Zugriff abläuft.</span><span class="sxs-lookup"><span data-stu-id="6adaf-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="6adaf-135">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, muss die Ablaufzeit sieben Tage nach der aktuellen Uhrzeit und nicht vor der aktuellen Uhrzeit sein.</span><span class="sxs-lookup"><span data-stu-id="6adaf-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="6adaf-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6adaf-136">-FullUri</span></span>
<span data-ttu-id="6adaf-137">Gibt an, dass dieses Cmdlet den vollständigen Blob-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6adaf-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6adaf-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6adaf-138">-IPAddressOrRange</span></span>
<span data-ttu-id="6adaf-139">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, über die Anforderungen akzeptiert werden können, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="6adaf-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6adaf-140">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="6adaf-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="6adaf-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="6adaf-141">-Permission</span></span>
<span data-ttu-id="6adaf-142">Gibt die Berechtigungen für einen Speicherblob an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="6adaf-143">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für Lesen, Schreiben und Löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="6adaf-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="6adaf-144">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6adaf-144">-Policy</span></span>
<span data-ttu-id="6adaf-145">Gibt eine Azure Stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="6adaf-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="6adaf-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6adaf-146">-Protocol</span></span>
<span data-ttu-id="6adaf-147">Gibt das Protokoll an, das für eine Anforderung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6adaf-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6adaf-148">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6adaf-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6adaf-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6adaf-149">HttpsOnly</span></span>
* <span data-ttu-id="6adaf-150">HttpsOrhttp Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="6adaf-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="6adaf-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6adaf-151">-StartTime</span></span>
<span data-ttu-id="6adaf-152">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="6adaf-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6adaf-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6adaf-153">-Confirm</span></span>
<span data-ttu-id="6adaf-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6adaf-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6adaf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6adaf-155">-WhatIf</span></span>
<span data-ttu-id="6adaf-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6adaf-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6adaf-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6adaf-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6adaf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adaf-158">CommonParameters</span></span>
<span data-ttu-id="6adaf-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adaf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adaf-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6adaf-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adaf-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6adaf-161">INPUTS</span></span>

### <span data-ttu-id="6adaf-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6adaf-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6adaf-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6adaf-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6adaf-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6adaf-164">OUTPUTS</span></span>

### <span data-ttu-id="6adaf-165">System.String</span><span class="sxs-lookup"><span data-stu-id="6adaf-165">System.String</span></span>

## <span data-ttu-id="6adaf-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6adaf-166">NOTES</span></span>

## <span data-ttu-id="6adaf-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6adaf-167">RELATED LINKS</span></span>

[<span data-ttu-id="6adaf-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6adaf-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6adaf-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6adaf-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
