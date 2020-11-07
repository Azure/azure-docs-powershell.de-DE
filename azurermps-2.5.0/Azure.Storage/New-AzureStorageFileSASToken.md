---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
ms.openlocfilehash: 7c1b29cdb420ed0af4be8ce8ff07c73db179cabe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848951"
---
# <span data-ttu-id="8faf6-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="8faf6-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="8faf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8faf6-102">SYNOPSIS</span></span>
<span data-ttu-id="8faf6-103">Generiert ein freigegebenes zugriffssignatur Token für eine Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="8faf6-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8faf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8faf6-104">SYNTAX</span></span>

### <span data-ttu-id="8faf6-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="8faf6-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8faf6-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="8faf6-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8faf6-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="8faf6-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8faf6-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="8faf6-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8faf6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8faf6-109">DESCRIPTION</span></span>
<span data-ttu-id="8faf6-110">Das Cmdlet **New-AzureStorageFileSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="8faf6-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="8faf6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8faf6-111">EXAMPLES</span></span>

### <span data-ttu-id="8faf6-112">Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens mit vollständigen Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="8faf6-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="8faf6-113">Dieser Befehl generiert ein freigegebenes zugriffssignatur Token, das über vollständige Berechtigungen für die Datei mit dem Namen filePath verfügt.</span><span class="sxs-lookup"><span data-stu-id="8faf6-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="8faf6-114">Beispiel 2: Generieren eines freigegebenen zugriffssignatur Tokens mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="8faf6-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="8faf6-115">Mit dem ersten Befehl wird mithilfe des Get-Date-Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8faf6-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="8faf6-116">Der Befehl speichert die aktuelle Uhrzeit in der $StartTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="8faf6-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="8faf6-117">Der zweite Befehl fügt dem Objekt in $StartTime zwei Stunden hinzu und speichert dann das Ergebnis in der $EndTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="8faf6-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="8faf6-118">Dieses Objekt ist eine Zeitdauer von zwei Stunden in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="8faf6-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="8faf6-119">Der dritte Befehl generiert ein freigegebenes zugriffssignatur Token, das über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8faf6-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="8faf6-120">Dieses Token wird zum aktuellen Zeitpunkt gültig.</span><span class="sxs-lookup"><span data-stu-id="8faf6-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="8faf6-121">Das Token bleibt gültig, bis die Zeit in $EndTime gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8faf6-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="8faf6-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8faf6-122">PARAMETERS</span></span>

### <span data-ttu-id="8faf6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="8faf6-123">-Context</span></span>
<span data-ttu-id="8faf6-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8faf6-125">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8faf6-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8faf6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8faf6-126">-DefaultProfile</span></span>
<span data-ttu-id="8faf6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8faf6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8faf6-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8faf6-128">-ExpiryTime</span></span>
<span data-ttu-id="8faf6-129">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="8faf6-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="8faf6-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="8faf6-130">-File</span></span>
<span data-ttu-id="8faf6-131">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="8faf6-132">Mithilfe des Get-AzureStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="8faf6-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8faf6-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8faf6-133">-FullUri</span></span>
<span data-ttu-id="8faf6-134">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8faf6-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8faf6-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8faf6-135">-IPAddressOrRange</span></span>
<span data-ttu-id="8faf6-136">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="8faf6-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8faf6-137">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="8faf6-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="8faf6-138">-Path</span><span class="sxs-lookup"><span data-stu-id="8faf6-138">-Path</span></span>
<span data-ttu-id="8faf6-139">Gibt den Pfad der Datei relativ zu einer Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="8faf6-140">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="8faf6-140">-Permission</span></span>
<span data-ttu-id="8faf6-141">Gibt die Berechtigungen für eine Speicherdatei an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="8faf6-142">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="8faf6-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8faf6-143">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8faf6-143">-Policy</span></span>
<span data-ttu-id="8faf6-144">Gibt die gespeicherte Zugriffsrichtlinie für eine Datei an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="8faf6-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8faf6-145">-Protocol</span></span>
<span data-ttu-id="8faf6-146">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8faf6-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8faf6-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8faf6-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8faf6-148">HttpsOnly</span></span>
* <span data-ttu-id="8faf6-149">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8faf6-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8faf6-150">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="8faf6-150">-ShareName</span></span>
<span data-ttu-id="8faf6-151">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8faf6-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="8faf6-152">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="8faf6-152">-StartTime</span></span>
<span data-ttu-id="8faf6-153">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="8faf6-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8faf6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8faf6-154">CommonParameters</span></span>
<span data-ttu-id="8faf6-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8faf6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8faf6-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8faf6-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8faf6-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8faf6-157">INPUTS</span></span>

### <span data-ttu-id="8faf6-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8faf6-158">System.String</span></span>

### <span data-ttu-id="8faf6-159">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="8faf6-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8faf6-160">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8faf6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="8faf6-161">Parameter: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8faf6-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="8faf6-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8faf6-162">OUTPUTS</span></span>

### <span data-ttu-id="8faf6-163">System. String</span><span class="sxs-lookup"><span data-stu-id="8faf6-163">System.String</span></span>

## <span data-ttu-id="8faf6-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="8faf6-164">NOTES</span></span>

## <span data-ttu-id="8faf6-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8faf6-165">RELATED LINKS</span></span>

[<span data-ttu-id="8faf6-166">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8faf6-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8faf6-167">Neu – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="8faf6-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
