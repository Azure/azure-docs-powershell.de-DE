---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 65a90f703f142a01429fb215bd5c66bef74bb4c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946763"
---
# <span data-ttu-id="20229-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="20229-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="20229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20229-102">SYNOPSIS</span></span>
<span data-ttu-id="20229-103">Generiert ein SAS-Token für eine Azure Storage-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20229-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="20229-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20229-104">SYNTAX</span></span>

### <span data-ttu-id="20229-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="20229-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20229-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="20229-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20229-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20229-107">DESCRIPTION</span></span>
<span data-ttu-id="20229-108">Das **Cmdlet New-AzStorageTableSASToken** generiert ein Sas-Token (Shared Access Signature) für eine Azure Storage-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20229-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="20229-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20229-109">EXAMPLES</span></span>

### <span data-ttu-id="20229-110">Beispiel 1: Generieren eines SAS-Tokens mit vollständigen Berechtigungen für eine Tabelle</span><span class="sxs-lookup"><span data-stu-id="20229-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="20229-111">Mit diesem Befehl wird ein SAS-Token mit vollständigen Berechtigungen für die Tabelle namens ContosoResources generiert.</span><span class="sxs-lookup"><span data-stu-id="20229-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="20229-112">Dieses Token ist zum Lesen, Hinzufügen, Aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="20229-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="20229-113">Beispiel 2: Generieren eines SAS-Tokens für einen Partitionsbereich</span><span class="sxs-lookup"><span data-stu-id="20229-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="20229-114">Dieser Befehl generiert und sas-Token mit vollständigen Berechtigungen für die Tabelle namens ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="20229-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="20229-115">Der Befehl beschränkt das Token auf den Bereich, den die *Parameter StartPartitionKey* und *EndPartitionKey* angeben.</span><span class="sxs-lookup"><span data-stu-id="20229-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="20229-116">Beispiel 3: Generieren eines SAS-Tokens mit einer gespeicherten Zugriffsrichtlinie für eine Tabelle</span><span class="sxs-lookup"><span data-stu-id="20229-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="20229-117">Mit diesem Befehl wird ein SAS-Token für die Tabelle namens ContosoResources generiert.</span><span class="sxs-lookup"><span data-stu-id="20229-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="20229-118">Der Befehl gibt die gespeicherte Zugriffsrichtlinie mit dem Namen ClientPolicy01 an.</span><span class="sxs-lookup"><span data-stu-id="20229-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="20229-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20229-119">PARAMETERS</span></span>

### <span data-ttu-id="20229-120">-Context</span><span class="sxs-lookup"><span data-stu-id="20229-120">-Context</span></span>
<span data-ttu-id="20229-121">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="20229-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="20229-122">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20229-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="20229-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20229-123">-DefaultProfile</span></span>
<span data-ttu-id="20229-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20229-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20229-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="20229-125">-EndPartitionKey</span></span>
<span data-ttu-id="20229-126">Gibt den Partitionsschlüssel des Bereichsendes für das Token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20229-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20229-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="20229-127">-EndRowKey</span></span>
<span data-ttu-id="20229-128">Gibt die Zeilentaste für das Ende des Bereichs für das Token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20229-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20229-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="20229-129">-ExpiryTime</span></span>
<span data-ttu-id="20229-130">Gibt an, wann das SAS-Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="20229-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="20229-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="20229-131">-FullUri</span></span>
<span data-ttu-id="20229-132">Gibt an, dass dieses Cmdlet den vollständigen Warteschlangen-URI mit dem SAS-Token zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="20229-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="20229-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="20229-133">-IPAddressOrRange</span></span>
<span data-ttu-id="20229-134">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, über die Anforderungen akzeptiert werden können, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="20229-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="20229-135">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="20229-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="20229-136">-Name</span><span class="sxs-lookup"><span data-stu-id="20229-136">-Name</span></span>
<span data-ttu-id="20229-137">Gibt den Namen einer Azure Storage-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="20229-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="20229-138">Dieses Cmdlet erstellt ein SAS-Token für die Tabelle, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="20229-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="20229-139">-Permission</span><span class="sxs-lookup"><span data-stu-id="20229-139">-Permission</span></span>
<span data-ttu-id="20229-140">Gibt Berechtigungen für eine Azure Storage-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="20229-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="20229-141">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für Lesen, Schreiben und Löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="20229-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="20229-142">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="20229-142">-Policy</span></span>
<span data-ttu-id="20229-143">Gibt eine richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token enthält.</span><span class="sxs-lookup"><span data-stu-id="20229-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="20229-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="20229-144">-Protocol</span></span>
<span data-ttu-id="20229-145">Gibt das Protokoll an, das für eine Anforderung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="20229-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="20229-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="20229-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="20229-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="20229-147">HttpsOnly</span></span>
* <span data-ttu-id="20229-148">HttpsOrhttp Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="20229-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="20229-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="20229-149">-StartPartitionKey</span></span>
<span data-ttu-id="20229-150">Gibt den Partitionsschlüssel des Anfangs des Bereichs für das Token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20229-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20229-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="20229-151">-StartRowKey</span></span>
<span data-ttu-id="20229-152">Gibt die Zeilentaste für den Anfang des Bereichs für das Token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20229-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20229-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="20229-153">-StartTime</span></span>
<span data-ttu-id="20229-154">Gibt an, wann das SAS-Token gültig wird.</span><span class="sxs-lookup"><span data-stu-id="20229-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="20229-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20229-155">CommonParameters</span></span>
<span data-ttu-id="20229-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20229-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20229-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20229-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20229-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20229-158">INPUTS</span></span>

### <span data-ttu-id="20229-159">System.String</span><span class="sxs-lookup"><span data-stu-id="20229-159">System.String</span></span>

### <span data-ttu-id="20229-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20229-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20229-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20229-161">OUTPUTS</span></span>

### <span data-ttu-id="20229-162">System.String</span><span class="sxs-lookup"><span data-stu-id="20229-162">System.String</span></span>

## <span data-ttu-id="20229-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20229-163">NOTES</span></span>

## <span data-ttu-id="20229-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20229-164">RELATED LINKS</span></span>

[<span data-ttu-id="20229-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="20229-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
