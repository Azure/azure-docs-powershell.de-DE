---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665280"
---
# <span data-ttu-id="7b205-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="7b205-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="7b205-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b205-102">SYNOPSIS</span></span>
<span data-ttu-id="7b205-103">Generiert ein SAS-Token für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="7b205-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b205-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b205-104">SYNTAX</span></span>

### <span data-ttu-id="7b205-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="7b205-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7b205-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="7b205-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="7b205-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b205-107">DESCRIPTION</span></span>
<span data-ttu-id="7b205-108">Das Cmdlet **New-AzureStorageTableSASToken** generiert ein SAS-Token (Shared Access Signature) für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="7b205-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="7b205-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b205-109">EXAMPLES</span></span>

### <span data-ttu-id="7b205-110">Beispiel 1: Generieren eines SAS-Tokens mit vollständigen Berechtigungen für eine Tabelle</span><span class="sxs-lookup"><span data-stu-id="7b205-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="7b205-111">Dieser Befehl generiert ein SAS-Token mit vollständigen Berechtigungen für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="7b205-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="7b205-112">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7b205-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="7b205-113">Beispiel 2: Generieren eines SAS-Tokens für einen Bereich von Partitionen</span><span class="sxs-lookup"><span data-stu-id="7b205-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="7b205-114">Dieser Befehl generiert und SAS-Token mit vollständigen Berechtigungen für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="7b205-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="7b205-115">Der Befehl schränkt das Token auf den Bereich ein, den die Parameter *StartPartitionKey* und *EndPartitionKey* angeben.</span><span class="sxs-lookup"><span data-stu-id="7b205-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="7b205-116">Beispiel 3: Generieren eines SAS-Tokens, das über eine gespeicherte Zugriffsrichtlinie für eine Tabelle verfügt</span><span class="sxs-lookup"><span data-stu-id="7b205-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="7b205-117">Dieser Befehl generiert ein SAS-Token für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="7b205-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="7b205-118">Der Befehl gibt die gespeicherte Zugriffsrichtlinie mit dem Namen "ClientPolicy01" an.</span><span class="sxs-lookup"><span data-stu-id="7b205-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="7b205-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b205-119">PARAMETERS</span></span>

### <span data-ttu-id="7b205-120">-Context</span><span class="sxs-lookup"><span data-stu-id="7b205-120">-Context</span></span>
<span data-ttu-id="7b205-121">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7b205-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b205-122">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7b205-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="7b205-123">-EndPartitionKey</span></span>
<span data-ttu-id="7b205-124">Gibt den Partitionsschlüssel am Ende des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="7b205-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="7b205-125">-EndRowKey</span></span>
<span data-ttu-id="7b205-126">Gibt den Zeilenschlüssel für das Ende des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="7b205-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7b205-127">-ExpiryTime</span></span>
<span data-ttu-id="7b205-128">Gibt an, wann das SAS-Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="7b205-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="7b205-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7b205-129">-FullUri</span></span>
<span data-ttu-id="7b205-130">Gibt an, dass dieses Cmdlet den vollständigen Warteschlangen-URI mit dem SAS-Token zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7b205-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="7b205-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7b205-131">-IPAddressOrRange</span></span>
<span data-ttu-id="7b205-132">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="7b205-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7b205-133">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="7b205-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="7b205-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7b205-134">-Name</span></span>
<span data-ttu-id="7b205-135">Gibt den Namen einer Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="7b205-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="7b205-136">Mit diesem Cmdlet wird ein SAS-Token für die von diesem Parameter festgelegte Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="7b205-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-137">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="7b205-137">-Permission</span></span>
<span data-ttu-id="7b205-138">Gibt Berechtigungen für eine Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="7b205-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-139">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7b205-139">-Policy</span></span>
<span data-ttu-id="7b205-140">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="7b205-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7b205-141">-Protocol</span></span>
<span data-ttu-id="7b205-142">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="7b205-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7b205-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7b205-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7b205-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7b205-144">HttpsOnly</span></span>
* <span data-ttu-id="7b205-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="7b205-145">HttpsOrHttp</span></span>

<span data-ttu-id="7b205-146">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="7b205-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="7b205-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="7b205-147">-StartPartitionKey</span></span>
<span data-ttu-id="7b205-148">Gibt den Partitionsschlüssel des Startbereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="7b205-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="7b205-149">-StartRowKey</span></span>
<span data-ttu-id="7b205-150">Gibt den Zeilenschlüssel für den Anfang des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="7b205-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b205-151">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="7b205-151">-StartTime</span></span>
<span data-ttu-id="7b205-152">Gibt an, wann das SAS-Token gültig wird.</span><span class="sxs-lookup"><span data-stu-id="7b205-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="7b205-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b205-153">CommonParameters</span></span>
<span data-ttu-id="7b205-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b205-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b205-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b205-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b205-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b205-156">INPUTS</span></span>

### <span data-ttu-id="7b205-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b205-157">IStorageContext</span></span>

<span data-ttu-id="7b205-158">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b205-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7b205-159">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7b205-159">String</span></span>

<span data-ttu-id="7b205-160">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b205-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7b205-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b205-161">OUTPUTS</span></span>

### <span data-ttu-id="7b205-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7b205-162">System.String</span></span>

## <span data-ttu-id="7b205-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b205-163">NOTES</span></span>

## <span data-ttu-id="7b205-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b205-164">RELATED LINKS</span></span>

[<span data-ttu-id="7b205-165">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b205-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
