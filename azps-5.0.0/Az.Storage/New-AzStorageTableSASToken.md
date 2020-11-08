---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179549"
---
# <span data-ttu-id="cd868-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="cd868-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="cd868-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd868-102">SYNOPSIS</span></span>
<span data-ttu-id="cd868-103">Generiert ein SAS-Token für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="cd868-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="cd868-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd868-104">SYNTAX</span></span>

### <span data-ttu-id="cd868-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="cd868-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd868-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="cd868-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd868-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd868-107">DESCRIPTION</span></span>
<span data-ttu-id="cd868-108">Das Cmdlet **New-AzStorageTableSASToken** generiert ein SAS-Token (Shared Access Signature) für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="cd868-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="cd868-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd868-109">EXAMPLES</span></span>

### <span data-ttu-id="cd868-110">Beispiel 1: Generieren eines SAS-Tokens mit vollständigen Berechtigungen für eine Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd868-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="cd868-111">Dieser Befehl generiert ein SAS-Token mit vollständigen Berechtigungen für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="cd868-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="cd868-112">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="cd868-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="cd868-113">Beispiel 2: Generieren eines SAS-Tokens für einen Bereich von Partitionen</span><span class="sxs-lookup"><span data-stu-id="cd868-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="cd868-114">Dieser Befehl generiert und SAS-Token mit vollständigen Berechtigungen für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="cd868-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="cd868-115">Der Befehl schränkt das Token auf den Bereich ein, den die Parameter *StartPartitionKey* und *EndPartitionKey* angeben.</span><span class="sxs-lookup"><span data-stu-id="cd868-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="cd868-116">Beispiel 3: Generieren eines SAS-Tokens, das über eine gespeicherte Zugriffsrichtlinie für eine Tabelle verfügt</span><span class="sxs-lookup"><span data-stu-id="cd868-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="cd868-117">Dieser Befehl generiert ein SAS-Token für die Tabelle mit dem Namen ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="cd868-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="cd868-118">Der Befehl gibt die gespeicherte Zugriffsrichtlinie mit dem Namen "ClientPolicy01" an.</span><span class="sxs-lookup"><span data-stu-id="cd868-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="cd868-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd868-119">PARAMETERS</span></span>

### <span data-ttu-id="cd868-120">-Context</span><span class="sxs-lookup"><span data-stu-id="cd868-120">-Context</span></span>
<span data-ttu-id="cd868-121">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cd868-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd868-122">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd868-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cd868-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd868-123">-DefaultProfile</span></span>
<span data-ttu-id="cd868-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd868-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd868-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="cd868-125">-EndPartitionKey</span></span>
<span data-ttu-id="cd868-126">Gibt den Partitionsschlüssel am Ende des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="cd868-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="cd868-127">-EndRowKey</span></span>
<span data-ttu-id="cd868-128">Gibt den Zeilenschlüssel für das Ende des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="cd868-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cd868-129">-ExpiryTime</span></span>
<span data-ttu-id="cd868-130">Gibt an, wann das SAS-Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="cd868-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="cd868-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="cd868-131">-FullUri</span></span>
<span data-ttu-id="cd868-132">Gibt an, dass dieses Cmdlet den vollständigen Warteschlangen-URI mit dem SAS-Token zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cd868-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="cd868-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cd868-133">-IPAddressOrRange</span></span>
<span data-ttu-id="cd868-134">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd868-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="cd868-135">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="cd868-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="cd868-136">-Name</span><span class="sxs-lookup"><span data-stu-id="cd868-136">-Name</span></span>
<span data-ttu-id="cd868-137">Gibt den Namen einer Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="cd868-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="cd868-138">Mit diesem Cmdlet wird ein SAS-Token für die von diesem Parameter festgelegte Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd868-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-139">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="cd868-139">-Permission</span></span>
<span data-ttu-id="cd868-140">Gibt Berechtigungen für eine Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="cd868-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="cd868-141">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="cd868-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="cd868-142">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="cd868-142">-Policy</span></span>
<span data-ttu-id="cd868-143">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="cd868-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="cd868-144">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="cd868-144">-Protocol</span></span>
<span data-ttu-id="cd868-145">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="cd868-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="cd868-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd868-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="cd868-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cd868-147">HttpsOnly</span></span>
* <span data-ttu-id="cd868-148">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="cd868-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="cd868-149">-StartPartitionKey</span></span>
<span data-ttu-id="cd868-150">Gibt den Partitionsschlüssel des Startbereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="cd868-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="cd868-151">-StartRowKey</span></span>
<span data-ttu-id="cd868-152">Gibt den Zeilenschlüssel für den Anfang des Bereichs für das von diesem Cmdlet erstellte Token an.</span><span class="sxs-lookup"><span data-stu-id="cd868-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd868-153">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="cd868-153">-StartTime</span></span>
<span data-ttu-id="cd868-154">Gibt an, wann das SAS-Token gültig wird.</span><span class="sxs-lookup"><span data-stu-id="cd868-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="cd868-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd868-155">CommonParameters</span></span>
<span data-ttu-id="cd868-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd868-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd868-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd868-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd868-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd868-158">INPUTS</span></span>

### <span data-ttu-id="cd868-159">System. String</span><span class="sxs-lookup"><span data-stu-id="cd868-159">System.String</span></span>

### <span data-ttu-id="cd868-160">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd868-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd868-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd868-161">OUTPUTS</span></span>

### <span data-ttu-id="cd868-162">System. String</span><span class="sxs-lookup"><span data-stu-id="cd868-162">System.String</span></span>

## <span data-ttu-id="cd868-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd868-163">NOTES</span></span>

## <span data-ttu-id="cd868-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd868-164">RELATED LINKS</span></span>

[<span data-ttu-id="cd868-165">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd868-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
