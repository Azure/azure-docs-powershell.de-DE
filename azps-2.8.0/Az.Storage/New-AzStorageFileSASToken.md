---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: 9a0a25664a5512dcdecea268cff1e2cdc177d3dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823907"
---
# <span data-ttu-id="ab71c-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="ab71c-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="ab71c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab71c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab71c-103">Generiert ein freigegebenes zugriffssignatur Token für eine Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="ab71c-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="ab71c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab71c-104">SYNTAX</span></span>

### <span data-ttu-id="ab71c-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="ab71c-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab71c-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ab71c-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab71c-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="ab71c-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab71c-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ab71c-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab71c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab71c-109">DESCRIPTION</span></span>
<span data-ttu-id="ab71c-110">Das Cmdlet **New-AzStorageFileSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="ab71c-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="ab71c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab71c-111">EXAMPLES</span></span>

### <span data-ttu-id="ab71c-112">Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens mit vollständigen Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="ab71c-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="ab71c-113">Dieser Befehl generiert ein freigegebenes zugriffssignatur Token, das über vollständige Berechtigungen für die Datei mit dem Namen filePath verfügt.</span><span class="sxs-lookup"><span data-stu-id="ab71c-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="ab71c-114">Beispiel 2: Generieren eines freigegebenen zugriffssignatur Tokens mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="ab71c-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ab71c-115">Mit dem ersten Befehl wird mithilfe des Get-Date-Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab71c-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="ab71c-116">Der Befehl speichert die aktuelle Uhrzeit in der $StartTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab71c-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="ab71c-117">Der zweite Befehl fügt dem Objekt in $StartTime zwei Stunden hinzu und speichert dann das Ergebnis in der $EndTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab71c-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="ab71c-118">Dieses Objekt ist eine Zeitdauer von zwei Stunden in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="ab71c-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="ab71c-119">Der dritte Befehl generiert ein freigegebenes zugriffssignatur Token, das über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="ab71c-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="ab71c-120">Dieses Token wird zum aktuellen Zeitpunkt gültig.</span><span class="sxs-lookup"><span data-stu-id="ab71c-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="ab71c-121">Das Token bleibt gültig, bis die Zeit in $EndTime gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ab71c-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="ab71c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab71c-122">PARAMETERS</span></span>

### <span data-ttu-id="ab71c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ab71c-123">-Context</span></span>
<span data-ttu-id="ab71c-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ab71c-125">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab71c-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ab71c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab71c-126">-DefaultProfile</span></span>
<span data-ttu-id="ab71c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab71c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab71c-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ab71c-128">-ExpiryTime</span></span>
<span data-ttu-id="ab71c-129">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="ab71c-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="ab71c-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="ab71c-130">-File</span></span>
<span data-ttu-id="ab71c-131">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ab71c-132">Mithilfe des Get-AzStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab71c-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab71c-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ab71c-133">-FullUri</span></span>
<span data-ttu-id="ab71c-134">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ab71c-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ab71c-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ab71c-135">-IPAddressOrRange</span></span>
<span data-ttu-id="ab71c-136">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="ab71c-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ab71c-137">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="ab71c-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="ab71c-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ab71c-138">-Path</span></span>
<span data-ttu-id="ab71c-139">Gibt den Pfad der Datei relativ zu einer Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="ab71c-140">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ab71c-140">-Permission</span></span>
<span data-ttu-id="ab71c-141">Gibt die Berechtigungen für eine Speicherdatei an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="ab71c-142">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="ab71c-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ab71c-143">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ab71c-143">-Policy</span></span>
<span data-ttu-id="ab71c-144">Gibt die gespeicherte Zugriffsrichtlinie für eine Datei an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="ab71c-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ab71c-145">-Protocol</span></span>
<span data-ttu-id="ab71c-146">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ab71c-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ab71c-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ab71c-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ab71c-148">HttpsOnly</span></span>
* <span data-ttu-id="ab71c-149">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="ab71c-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ab71c-150">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="ab71c-150">-ShareName</span></span>
<span data-ttu-id="ab71c-151">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab71c-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="ab71c-152">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ab71c-152">-StartTime</span></span>
<span data-ttu-id="ab71c-153">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="ab71c-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ab71c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab71c-154">CommonParameters</span></span>
<span data-ttu-id="ab71c-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab71c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab71c-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab71c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab71c-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab71c-157">INPUTS</span></span>

### <span data-ttu-id="ab71c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ab71c-158">System.String</span></span>

### <span data-ttu-id="ab71c-159">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="ab71c-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ab71c-160">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab71c-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab71c-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab71c-161">OUTPUTS</span></span>

### <span data-ttu-id="ab71c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ab71c-162">System.String</span></span>

## <span data-ttu-id="ab71c-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab71c-163">NOTES</span></span>

## <span data-ttu-id="ab71c-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab71c-164">RELATED LINKS</span></span>

[<span data-ttu-id="ab71c-165">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab71c-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ab71c-166">Neu – AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="ab71c-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
