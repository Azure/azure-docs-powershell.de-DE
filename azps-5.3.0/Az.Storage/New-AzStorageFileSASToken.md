---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: fcd58edbb3d6e03becc8e6305f58555fedf36107
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460251"
---
# <span data-ttu-id="725c6-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="725c6-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="725c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="725c6-102">SYNOPSIS</span></span>
<span data-ttu-id="725c6-103">Generiert ein Token für die Signatur für den freigegebenen Zugriff für eine Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="725c6-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="725c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="725c6-104">SYNTAX</span></span>

### <span data-ttu-id="725c6-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="725c6-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="725c6-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="725c6-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="725c6-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="725c6-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="725c6-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="725c6-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="725c6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="725c6-109">DESCRIPTION</span></span>
<span data-ttu-id="725c6-110">Das **Cmdlet "New-AzStorageFileSASToken"** generiert ein Signaturtoken für den freigegebenen Zugriff für eine Azure Storage-Datei.</span><span class="sxs-lookup"><span data-stu-id="725c6-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="725c6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="725c6-111">EXAMPLES</span></span>

### <span data-ttu-id="725c6-112">Beispiel 1: Generieren eines Tokens für eine Signatur für den freigegebenen Zugriff mit vollständigen Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="725c6-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="725c6-113">Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff generiert, das über vollständige Berechtigungen für die Datei namens "FilePath" verfügt.</span><span class="sxs-lookup"><span data-stu-id="725c6-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="725c6-114">Beispiel 2: Generieren eines Tokens für freigegebene Zugriffssignaturen mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="725c6-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="725c6-115">Der erste Befehl erstellt ein **DateTime-Objekt** mithilfe des Get-Date Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="725c6-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="725c6-116">Der Befehl speichert die aktuelle Uhrzeit in der $StartTime Variable.</span><span class="sxs-lookup"><span data-stu-id="725c6-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="725c6-117">Der zweite Befehl addiert zwei Stunden zum Objekt in $StartTime und speichert dann das Ergebnis in der $EndTime Variable.</span><span class="sxs-lookup"><span data-stu-id="725c6-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="725c6-118">Dieses Objekt ist eine Zeit in zwei Stunden in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="725c6-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="725c6-119">Der dritte Befehl generiert ein Token für die freigegebene Zugriffssignatur, das über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="725c6-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="725c6-120">Dieses Token wird zum aktuellen Zeitpunkt gültig.</span><span class="sxs-lookup"><span data-stu-id="725c6-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="725c6-121">Das Token bleibt so lange gültig, bis es in einem $EndTime.</span><span class="sxs-lookup"><span data-stu-id="725c6-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="725c6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="725c6-122">PARAMETERS</span></span>

### <span data-ttu-id="725c6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="725c6-123">-Context</span></span>
<span data-ttu-id="725c6-124">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="725c6-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="725c6-125">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="725c6-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="725c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725c6-126">-DefaultProfile</span></span>
<span data-ttu-id="725c6-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="725c6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="725c6-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="725c6-128">-ExpiryTime</span></span>
<span data-ttu-id="725c6-129">Gibt die Uhrzeit an, zu der die Signatur für den freigegebenen Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="725c6-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="725c6-130">-File</span><span class="sxs-lookup"><span data-stu-id="725c6-130">-File</span></span>
<span data-ttu-id="725c6-131">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="725c6-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="725c6-132">Sie können eine Clouddatei erstellen oder sie mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="725c6-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="725c6-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="725c6-133">-FullUri</span></span>
<span data-ttu-id="725c6-134">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="725c6-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="725c6-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="725c6-135">-IPAddressOrRange</span></span>
<span data-ttu-id="725c6-136">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="725c6-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="725c6-137">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="725c6-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="725c6-138">-Path</span><span class="sxs-lookup"><span data-stu-id="725c6-138">-Path</span></span>
<span data-ttu-id="725c6-139">Gibt den Pfad der Datei relativ zu einer Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="725c6-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="725c6-140">-Permission</span><span class="sxs-lookup"><span data-stu-id="725c6-140">-Permission</span></span>
<span data-ttu-id="725c6-141">Gibt die Berechtigungen für eine Speicherdatei an.</span><span class="sxs-lookup"><span data-stu-id="725c6-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="725c6-142">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="725c6-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="725c6-143">-Policy</span><span class="sxs-lookup"><span data-stu-id="725c6-143">-Policy</span></span>
<span data-ttu-id="725c6-144">Gibt die Gespeicherte Zugriffsrichtlinie für eine Datei an.</span><span class="sxs-lookup"><span data-stu-id="725c6-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="725c6-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="725c6-145">-Protocol</span></span>
<span data-ttu-id="725c6-146">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="725c6-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="725c6-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="725c6-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="725c6-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="725c6-148">HttpsOnly</span></span>
* <span data-ttu-id="725c6-149">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="725c6-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="725c6-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="725c6-150">-ShareName</span></span>
<span data-ttu-id="725c6-151">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="725c6-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="725c6-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="725c6-152">-StartTime</span></span>
<span data-ttu-id="725c6-153">Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.</span><span class="sxs-lookup"><span data-stu-id="725c6-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="725c6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725c6-154">CommonParameters</span></span>
<span data-ttu-id="725c6-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="725c6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725c6-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725c6-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725c6-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="725c6-157">INPUTS</span></span>

### <span data-ttu-id="725c6-158">System.String</span><span class="sxs-lookup"><span data-stu-id="725c6-158">System.String</span></span>

### <span data-ttu-id="725c6-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="725c6-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="725c6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="725c6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="725c6-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="725c6-161">OUTPUTS</span></span>

### <span data-ttu-id="725c6-162">System.String</span><span class="sxs-lookup"><span data-stu-id="725c6-162">System.String</span></span>

## <span data-ttu-id="725c6-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="725c6-163">NOTES</span></span>

## <span data-ttu-id="725c6-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="725c6-164">RELATED LINKS</span></span>

[<span data-ttu-id="725c6-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="725c6-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="725c6-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="725c6-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
