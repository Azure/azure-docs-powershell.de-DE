---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: ec5f290a6c45725dfed369058d5e00bbee016f9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944506"
---
# <span data-ttu-id="12f79-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="12f79-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="12f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f79-102">SYNOPSIS</span></span>
<span data-ttu-id="12f79-103">Generiert ein Signaturtoken für den freigegebenen Zugriff für eine Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="12f79-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="12f79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12f79-104">SYNTAX</span></span>

### <span data-ttu-id="12f79-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="12f79-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f79-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="12f79-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f79-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="12f79-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f79-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="12f79-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f79-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12f79-109">DESCRIPTION</span></span>
<span data-ttu-id="12f79-110">Das **Cmdlet New-AzStorageFileSASToken** generiert ein Signaturtoken für den freigegebenen Zugriff für eine Azure Storage-Datei.</span><span class="sxs-lookup"><span data-stu-id="12f79-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="12f79-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12f79-111">EXAMPLES</span></span>

### <span data-ttu-id="12f79-112">Beispiel 1: Generieren eines Signaturtokens für den freigegebenen Zugriff mit vollständigen Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="12f79-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="12f79-113">Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff generiert, das über die vollständigen Berechtigungen für die Datei mit dem Namen FilePath verfügt.</span><span class="sxs-lookup"><span data-stu-id="12f79-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="12f79-114">Beispiel 2: Generieren eines Tokens für freigegebene Zugriffssignaturen mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="12f79-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="12f79-115">Mit dem ersten Befehl wird ein **DateTime-Objekt** mithilfe des cmdlets Get-Date erstellt.</span><span class="sxs-lookup"><span data-stu-id="12f79-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="12f79-116">Der Befehl speichert die aktuelle Uhrzeit in der $StartTime Variable.</span><span class="sxs-lookup"><span data-stu-id="12f79-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="12f79-117">Der zweite Befehl addiert dem Objekt in $StartTime zwei Stunden und speichert dann das Ergebnis in $EndTime Variable.</span><span class="sxs-lookup"><span data-stu-id="12f79-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="12f79-118">Dieses Objekt ist eine Zeit von zwei Stunden in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="12f79-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="12f79-119">Der dritte Befehl generiert ein Signaturtoken für den freigegebenen Zugriff, das über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="12f79-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="12f79-120">Dieses Token wird zum aktuellen Zeitpunkt gültig.</span><span class="sxs-lookup"><span data-stu-id="12f79-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="12f79-121">Das Token bleibt solange gültig, bis die Zeit in $EndTime.</span><span class="sxs-lookup"><span data-stu-id="12f79-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="12f79-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12f79-122">PARAMETERS</span></span>

### <span data-ttu-id="12f79-123">-Context</span><span class="sxs-lookup"><span data-stu-id="12f79-123">-Context</span></span>
<span data-ttu-id="12f79-124">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="12f79-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="12f79-125">Verwenden Sie das cmdlet New-AzStorageContext, um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="12f79-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f79-126">-DefaultProfile</span></span>
<span data-ttu-id="12f79-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12f79-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f79-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="12f79-128">-ExpiryTime</span></span>
<span data-ttu-id="12f79-129">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="12f79-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="12f79-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="12f79-130">-File</span></span>
<span data-ttu-id="12f79-131">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="12f79-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="12f79-132">Sie können eine Clouddatei erstellen oder mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="12f79-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="12f79-133">-FullUri</span></span>
<span data-ttu-id="12f79-134">Gibt an, dass dieses Cmdlet den vollständigen Blob-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="12f79-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="12f79-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="12f79-135">-IPAddressOrRange</span></span>
<span data-ttu-id="12f79-136">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, über die Anforderungen akzeptiert werden können, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="12f79-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="12f79-137">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="12f79-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="12f79-138">-Path</span><span class="sxs-lookup"><span data-stu-id="12f79-138">-Path</span></span>
<span data-ttu-id="12f79-139">Gibt den Pfad der Datei relativ zu einer Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="12f79-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-140">-Permission</span><span class="sxs-lookup"><span data-stu-id="12f79-140">-Permission</span></span>
<span data-ttu-id="12f79-141">Gibt die Berechtigungen für eine Speicherdatei an.</span><span class="sxs-lookup"><span data-stu-id="12f79-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="12f79-142">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für Lesen, Schreiben und Löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="12f79-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-143">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="12f79-143">-Policy</span></span>
<span data-ttu-id="12f79-144">Gibt die gespeicherte Zugriffsrichtlinie für eine Datei an.</span><span class="sxs-lookup"><span data-stu-id="12f79-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="12f79-145">-Protocol</span></span>
<span data-ttu-id="12f79-146">Gibt das Protokoll an, das für eine Anforderung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="12f79-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="12f79-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="12f79-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="12f79-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="12f79-148">HttpsOnly</span></span>
* <span data-ttu-id="12f79-149">HttpsOrhttp Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="12f79-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="12f79-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="12f79-150">-ShareName</span></span>
<span data-ttu-id="12f79-151">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="12f79-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f79-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="12f79-152">-StartTime</span></span>
<span data-ttu-id="12f79-153">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="12f79-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="12f79-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f79-154">CommonParameters</span></span>
<span data-ttu-id="12f79-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f79-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f79-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f79-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f79-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12f79-157">INPUTS</span></span>

### <span data-ttu-id="12f79-158">System.String</span><span class="sxs-lookup"><span data-stu-id="12f79-158">System.String</span></span>

### <span data-ttu-id="12f79-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="12f79-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="12f79-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12f79-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12f79-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12f79-161">OUTPUTS</span></span>

### <span data-ttu-id="12f79-162">System.String</span><span class="sxs-lookup"><span data-stu-id="12f79-162">System.String</span></span>

## <span data-ttu-id="12f79-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12f79-163">NOTES</span></span>

## <span data-ttu-id="12f79-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12f79-164">RELATED LINKS</span></span>

[<span data-ttu-id="12f79-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="12f79-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="12f79-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="12f79-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
