---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: e5e4eaf5fa6808432dfdb04120bf9ef92a98452b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496737"
---
# <span data-ttu-id="478c9-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="478c9-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="478c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="478c9-102">SYNOPSIS</span></span>
<span data-ttu-id="478c9-103">Generiert ein freigegebenes zugriffssignatur Token für eine Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="478c9-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="478c9-104">SYNTAX</span></span>

### <span data-ttu-id="478c9-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="478c9-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="478c9-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="478c9-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="478c9-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="478c9-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="478c9-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="478c9-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="478c9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="478c9-109">DESCRIPTION</span></span>
<span data-ttu-id="478c9-110">Das Cmdlet **New-AzureStorageFileSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="478c9-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="478c9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="478c9-111">EXAMPLES</span></span>

### <span data-ttu-id="478c9-112">Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens mit vollständigen Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="478c9-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="478c9-113">Dieser Befehl generiert ein freigegebenes zugriffssignatur Token, das über vollständige Berechtigungen für die Datei mit dem Namen filePath verfügt.</span><span class="sxs-lookup"><span data-stu-id="478c9-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="478c9-114">Beispiel 2: Generieren eines freigegebenen zugriffssignatur Tokens mit einem Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="478c9-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="478c9-115">Mit dem ersten Befehl wird mithilfe des Get-Date-Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="478c9-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="478c9-116">Der Befehl speichert die aktuelle Uhrzeit in der $StartTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="478c9-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="478c9-117">Der zweite Befehl fügt dem Objekt in $StartTime zwei Stunden hinzu und speichert dann das Ergebnis in der $EndTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="478c9-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="478c9-118">Dieses Objekt ist eine Zeitdauer von zwei Stunden in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="478c9-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="478c9-119">Der dritte Befehl generiert ein freigegebenes zugriffssignatur Token, das über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="478c9-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="478c9-120">Dieses Token wird zum aktuellen Zeitpunkt gültig.</span><span class="sxs-lookup"><span data-stu-id="478c9-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="478c9-121">Das Token bleibt gültig, bis die Zeit in $EndTime gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="478c9-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="478c9-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="478c9-122">PARAMETERS</span></span>

### <span data-ttu-id="478c9-123">-Context</span><span class="sxs-lookup"><span data-stu-id="478c9-123">-Context</span></span>
<span data-ttu-id="478c9-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="478c9-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="478c9-125">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="478c9-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="478c9-126">-ExpiryTime</span></span>
<span data-ttu-id="478c9-127">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="478c9-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-128">-Datei</span><span class="sxs-lookup"><span data-stu-id="478c9-128">-File</span></span>
<span data-ttu-id="478c9-129">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="478c9-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="478c9-130">Mithilfe des Get-AzureStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="478c9-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="478c9-131">-FullUri</span></span>
<span data-ttu-id="478c9-132">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="478c9-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="478c9-133">-IPAddressOrRange</span></span>
<span data-ttu-id="478c9-134">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="478c9-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="478c9-135">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="478c9-135">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-136">-Path</span><span class="sxs-lookup"><span data-stu-id="478c9-136">-Path</span></span>
<span data-ttu-id="478c9-137">Gibt den Pfad der Datei relativ zu einer Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="478c9-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-138">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="478c9-138">-Permission</span></span>
<span data-ttu-id="478c9-139">Gibt die Berechtigungen für eine Speicherdatei an.</span><span class="sxs-lookup"><span data-stu-id="478c9-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-140">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="478c9-140">-Policy</span></span>
<span data-ttu-id="478c9-141">Gibt die gespeicherte Zugriffsrichtlinie für eine Datei an.</span><span class="sxs-lookup"><span data-stu-id="478c9-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="478c9-142">-Protocol</span></span>
<span data-ttu-id="478c9-143">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="478c9-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="478c9-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="478c9-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="478c9-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="478c9-145">HttpsOnly</span></span>
* <span data-ttu-id="478c9-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="478c9-146">HttpsOrHttp</span></span>

<span data-ttu-id="478c9-147">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="478c9-147">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-148">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="478c9-148">-ShareName</span></span>
<span data-ttu-id="478c9-149">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="478c9-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-150">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="478c9-150">-StartTime</span></span>
<span data-ttu-id="478c9-151">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="478c9-151">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478c9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478c9-152">CommonParameters</span></span>
<span data-ttu-id="478c9-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478c9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478c9-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478c9-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478c9-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="478c9-155">INPUTS</span></span>

### <span data-ttu-id="478c9-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="478c9-156">IStorageContext</span></span>

<span data-ttu-id="478c9-157">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="478c9-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="478c9-158">Clouddatei</span><span class="sxs-lookup"><span data-stu-id="478c9-158">CloudFile</span></span>

<span data-ttu-id="478c9-159">Der Parameter "Datei" akzeptiert den Wert vom Typ "clouddatei" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="478c9-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="478c9-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="478c9-160">String</span></span>

<span data-ttu-id="478c9-161">Der Parameter "Path" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="478c9-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="478c9-162">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="478c9-162">String</span></span>

<span data-ttu-id="478c9-163">Der Parameter "Freigabename" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="478c9-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="478c9-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="478c9-164">OUTPUTS</span></span>

### <span data-ttu-id="478c9-165">System. String</span><span class="sxs-lookup"><span data-stu-id="478c9-165">System.String</span></span>

## <span data-ttu-id="478c9-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="478c9-166">NOTES</span></span>

## <span data-ttu-id="478c9-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="478c9-167">RELATED LINKS</span></span>

[<span data-ttu-id="478c9-168">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="478c9-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="478c9-169">Neu – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="478c9-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
