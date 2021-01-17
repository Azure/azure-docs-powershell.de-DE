---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471709"
---
# <span data-ttu-id="b27c2-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="b27c2-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="b27c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b27c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b27c2-103">Generiert ein SAS-Token für eine Azure Storage-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b27c2-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="b27c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b27c2-104">SYNTAX</span></span>

### <span data-ttu-id="b27c2-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b27c2-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b27c2-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b27c2-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b27c2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b27c2-107">DESCRIPTION</span></span>
<span data-ttu-id="b27c2-108">Das **Cmdlet "New-AzStorageTableSASToken"** generiert ein TOKEN (Shared Access Signature) für eine Azure Storage-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b27c2-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="b27c2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b27c2-109">EXAMPLES</span></span>

### <span data-ttu-id="b27c2-110">Beispiel 1: Generieren eines SAS-Tokens, das über vollständige Berechtigungen für eine Tabelle verfügt</span><span class="sxs-lookup"><span data-stu-id="b27c2-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="b27c2-111">Dieser Befehl generiert ein SAS-Token mit vollständigen Berechtigungen für die Tabelle mit dem Namen "ContosoResources".</span><span class="sxs-lookup"><span data-stu-id="b27c2-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="b27c2-112">Dieses Token ist für Berechtigungen zum Lesen, Hinzufügen, Aktualisieren und Löschen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b27c2-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="b27c2-113">Beispiel 2: Generieren eines SAS-Tokens für einen Bereich von Partitionen</span><span class="sxs-lookup"><span data-stu-id="b27c2-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="b27c2-114">Dieser Befehl generiert ein SAS-Token mit vollständigen Berechtigungen für die Tabelle "ContosoResources".</span><span class="sxs-lookup"><span data-stu-id="b27c2-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="b27c2-115">Der Befehl beschränkt das Token auf den Bereich, den die *Parameter "StartPartitionKey"* und *"EndPartitionKey"* angeben.</span><span class="sxs-lookup"><span data-stu-id="b27c2-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="b27c2-116">Beispiel 3: Generieren eines SAS-Tokens, das über eine gespeicherte Zugriffsrichtlinie für eine Tabelle verfügt</span><span class="sxs-lookup"><span data-stu-id="b27c2-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="b27c2-117">Dieser Befehl generiert ein SAS-Token für die Tabelle mit dem Namen "ContosoResources".</span><span class="sxs-lookup"><span data-stu-id="b27c2-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="b27c2-118">Der Befehl gibt die gespeicherte Zugriffsrichtlinie namens "ClientPolicy01" an.</span><span class="sxs-lookup"><span data-stu-id="b27c2-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="b27c2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b27c2-119">PARAMETERS</span></span>

### <span data-ttu-id="b27c2-120">-Context</span><span class="sxs-lookup"><span data-stu-id="b27c2-120">-Context</span></span>
<span data-ttu-id="b27c2-121">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b27c2-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b27c2-122">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27c2-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b27c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27c2-123">-DefaultProfile</span></span>
<span data-ttu-id="b27c2-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b27c2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27c2-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="b27c2-125">-EndPartitionKey</span></span>
<span data-ttu-id="b27c2-126">Gibt den Partitionsschlüssel am Ende des Bereichs für das token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b27c2-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b27c2-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="b27c2-127">-EndRowKey</span></span>
<span data-ttu-id="b27c2-128">Gibt den Zeilenschlüssel für das Ende des Bereichs für das token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b27c2-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b27c2-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b27c2-129">-ExpiryTime</span></span>
<span data-ttu-id="b27c2-130">Gibt an, wann das SAS-Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="b27c2-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="b27c2-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b27c2-131">-FullUri</span></span>
<span data-ttu-id="b27c2-132">Gibt an, dass dieses Cmdlet den vollständigen Warteschlangen-URI mit dem SAS-Token zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b27c2-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="b27c2-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b27c2-133">-IPAddressOrRange</span></span>
<span data-ttu-id="b27c2-134">Gibt die IP-Adresse oder den Bereich der IP-Adressen an, von denen Anforderungen akzeptiert werden, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b27c2-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b27c2-135">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="b27c2-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="b27c2-136">-Name</span><span class="sxs-lookup"><span data-stu-id="b27c2-136">-Name</span></span>
<span data-ttu-id="b27c2-137">Gibt den Namen einer Azure Storage-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="b27c2-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="b27c2-138">Dieses Cmdlet erstellt ein SAS-Token für die Tabelle, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b27c2-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="b27c2-139">-Permission</span><span class="sxs-lookup"><span data-stu-id="b27c2-139">-Permission</span></span>
<span data-ttu-id="b27c2-140">Gibt Berechtigungen für eine Azure Storage-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="b27c2-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="b27c2-141">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="b27c2-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b27c2-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="b27c2-142">-Policy</span></span>
<span data-ttu-id="b27c2-143">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token enthält.</span><span class="sxs-lookup"><span data-stu-id="b27c2-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="b27c2-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b27c2-144">-Protocol</span></span>
<span data-ttu-id="b27c2-145">Gibt das für eine Anforderung zulässige Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="b27c2-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b27c2-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b27c2-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b27c2-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b27c2-147">HttpsOnly</span></span>
* <span data-ttu-id="b27c2-148">"HttpsOrHttp" der Standardwert ist "HttpsOrHttp".</span><span class="sxs-lookup"><span data-stu-id="b27c2-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b27c2-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="b27c2-149">-StartPartitionKey</span></span>
<span data-ttu-id="b27c2-150">Gibt den Partitionsschlüssel des Startbereichs für das Token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b27c2-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b27c2-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="b27c2-151">-StartRowKey</span></span>
<span data-ttu-id="b27c2-152">Gibt den Zeilenschlüssel für den Anfang des Bereichs für das token an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b27c2-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b27c2-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b27c2-153">-StartTime</span></span>
<span data-ttu-id="b27c2-154">Gibt an, wann das SAS-Token gültig wird.</span><span class="sxs-lookup"><span data-stu-id="b27c2-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="b27c2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27c2-155">CommonParameters</span></span>
<span data-ttu-id="b27c2-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27c2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27c2-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27c2-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27c2-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b27c2-158">INPUTS</span></span>

### <span data-ttu-id="b27c2-159">System.String</span><span class="sxs-lookup"><span data-stu-id="b27c2-159">System.String</span></span>

### <span data-ttu-id="b27c2-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b27c2-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b27c2-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b27c2-161">OUTPUTS</span></span>

### <span data-ttu-id="b27c2-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b27c2-162">System.String</span></span>

## <span data-ttu-id="b27c2-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b27c2-163">NOTES</span></span>

## <span data-ttu-id="b27c2-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b27c2-164">RELATED LINKS</span></span>

[<span data-ttu-id="b27c2-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b27c2-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
