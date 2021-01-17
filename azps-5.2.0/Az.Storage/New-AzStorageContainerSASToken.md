---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304067"
---
# <span data-ttu-id="ee74b-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ee74b-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="ee74b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee74b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee74b-103">Generiert ein SAS-Token für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="ee74b-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="ee74b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee74b-104">SYNTAX</span></span>

### <span data-ttu-id="ee74b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="ee74b-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee74b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="ee74b-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee74b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee74b-107">DESCRIPTION</span></span>
<span data-ttu-id="ee74b-108">Das **Cmdlet "New-AzStorageContainerSASToken"** generiert ein SAS (Shared Access Signature)-Token für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="ee74b-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="ee74b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee74b-109">EXAMPLES</span></span>

### <span data-ttu-id="ee74b-110">Beispiel 1: Generieren eines Container-SAS-Tokens mit der vollständigen Containerberechtigung</span><span class="sxs-lookup"><span data-stu-id="ee74b-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="ee74b-111">In diesem Beispiel wird ein Container-SAS-Token mit der vollständigen Containerberechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="ee74b-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="ee74b-112">Beispiel 2: Generieren mehrerer Container-SAS-Tokens durch Pipeline</span><span class="sxs-lookup"><span data-stu-id="ee74b-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="ee74b-113">In diesem Beispiel werden mithilfe der Pipeline mehrere Container-SAS-Token generiert.</span><span class="sxs-lookup"><span data-stu-id="ee74b-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="ee74b-114">Beispiel 3: Generieren des Container-SAS-Tokens mit der Richtlinie für den freigegebenen Zugriff</span><span class="sxs-lookup"><span data-stu-id="ee74b-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="ee74b-115">In diesem Beispiel wird ein Container-SAS-Token mit einer Richtlinie für den freigegebenen Zugriff generiert.</span><span class="sxs-lookup"><span data-stu-id="ee74b-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="ee74b-116">Beispiel 3: Generieren eines BENUTZERidentitätscontainer-SAS-Tokens mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="ee74b-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="ee74b-117">In diesem Beispiel wird ein BENUTZERidentitätscontainer-SAS-Token mit Speicherkontext generiert, der auf der OAuth-Authentifizierung basiert.</span><span class="sxs-lookup"><span data-stu-id="ee74b-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="ee74b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee74b-118">PARAMETERS</span></span>

### <span data-ttu-id="ee74b-119">-Context</span><span class="sxs-lookup"><span data-stu-id="ee74b-119">-Context</span></span>
<span data-ttu-id="ee74b-120">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ee74b-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee74b-121">Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee74b-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="ee74b-122">Wenn der Speicherkontext auf der OAuth-Authentifizierung basiert, wird ein BENUTZERidentitätscontainer-SAS-Token generiert.</span><span class="sxs-lookup"><span data-stu-id="ee74b-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="ee74b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee74b-123">-DefaultProfile</span></span>
<span data-ttu-id="ee74b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee74b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee74b-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee74b-125">-ExpiryTime</span></span>
<span data-ttu-id="ee74b-126">Gibt die Uhrzeit an, zu der die Signatur für den freigegebenen Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="ee74b-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="ee74b-127">Wenn der Benutzer die Startzeit, aber nicht die Ablaufzeit fest legt, wird die Ablaufzeit auf die Startzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="ee74b-128">Wird weder die Start- noch die Ablaufzeit angegeben, wird die Ablaufzeit auf die aktuelle Uhrzeit plus eine Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="ee74b-129">Basiert der Speicherkontext auf der OAuth-Authentifizierung, muss die Ablaufzeit sieben Tage nach der aktuellen Uhrzeit und nicht vor der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="ee74b-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ee74b-130">-FullUri</span></span>
<span data-ttu-id="ee74b-131">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ee74b-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ee74b-132">-IPAddressOrRange</span></span>
<span data-ttu-id="ee74b-133">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="ee74b-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ee74b-134">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="ee74b-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="ee74b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="ee74b-135">-Name</span></span>
<span data-ttu-id="ee74b-136">Gibt den Namen eines Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="ee74b-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="ee74b-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="ee74b-137">-Permission</span></span>
<span data-ttu-id="ee74b-138">Gibt Berechtigungen für einen Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="ee74b-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="ee74b-139">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ee74b-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="ee74b-140">-Policy</span></span>
<span data-ttu-id="ee74b-141">Gibt eine Azure Stored Access Policy an.</span><span class="sxs-lookup"><span data-stu-id="ee74b-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="ee74b-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ee74b-142">-Protocol</span></span>
<span data-ttu-id="ee74b-143">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ee74b-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ee74b-144">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ee74b-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ee74b-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ee74b-145">HttpsOnly</span></span>
* <span data-ttu-id="ee74b-146">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="ee74b-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ee74b-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ee74b-147">-StartTime</span></span>
<span data-ttu-id="ee74b-148">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="ee74b-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ee74b-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee74b-149">-Confirm</span></span>
<span data-ttu-id="ee74b-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee74b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee74b-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ee74b-151">-WhatIf</span></span>
<span data-ttu-id="ee74b-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee74b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee74b-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee74b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee74b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee74b-154">CommonParameters</span></span>
<span data-ttu-id="ee74b-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee74b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee74b-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee74b-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee74b-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee74b-157">INPUTS</span></span>

### <span data-ttu-id="ee74b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="ee74b-158">System.String</span></span>

### <span data-ttu-id="ee74b-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee74b-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee74b-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee74b-160">OUTPUTS</span></span>

### <span data-ttu-id="ee74b-161">System.String</span><span class="sxs-lookup"><span data-stu-id="ee74b-161">System.String</span></span>

## <span data-ttu-id="ee74b-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ee74b-162">NOTES</span></span>

## <span data-ttu-id="ee74b-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ee74b-163">RELATED LINKS</span></span>

[<span data-ttu-id="ee74b-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ee74b-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
