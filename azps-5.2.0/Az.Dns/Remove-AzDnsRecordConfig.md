---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: aa67873ba55f815e7fdd8ada4658370c16e65c4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302360"
---
# <span data-ttu-id="b31e0-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b31e0-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="b31e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b31e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b31e0-103">Entfernt einen DNS-Eintrag aus einem lokalen Datensatzsatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="b31e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b31e0-104">SYNTAX</span></span>

### <span data-ttu-id="b31e0-105">A</span><span class="sxs-lookup"><span data-stu-id="b31e0-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31e0-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="b31e0-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31e0-107">NS</span><span class="sxs-lookup"><span data-stu-id="b31e0-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31e0-108">MX</span><span class="sxs-lookup"><span data-stu-id="b31e0-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31e0-109">PTR</span><span class="sxs-lookup"><span data-stu-id="b31e0-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31e0-110">TXT</span><span class="sxs-lookup"><span data-stu-id="b31e0-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31e0-111">SRV</span><span class="sxs-lookup"><span data-stu-id="b31e0-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31e0-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="b31e0-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31e0-113">Caa</span><span class="sxs-lookup"><span data-stu-id="b31e0-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31e0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b31e0-114">DESCRIPTION</span></span>
<span data-ttu-id="b31e0-115">Das **Cmdlet "Remove-AzDnsRecordConfig"** entfernt einen Domain Name System (DNS)-Eintrag aus einem Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="b31e0-116">Das **Objekt "RecordSet"** ist ein Offlineobjekt, und änderungen an diesem Objekt ändern die DNS-Antworten erst, nachdem Sie das Cmdlet "Set-AzDnsRecordSet" ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b31e0-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="b31e0-117">Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp exakt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b31e0-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="b31e0-118">Sie können keine SOA-Einträge hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="b31e0-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="b31e0-119">SOA-Einträge werden automatisch erstellt, wenn eine DNS-Zone erstellt wird, und beim Löschen der DNS-Zone automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b31e0-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="b31e0-120">Sie können das **Objekt "RecordSet"** als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="b31e0-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="b31e0-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b31e0-121">EXAMPLES</span></span>

### <span data-ttu-id="b31e0-122">Beispiel 1: Entfernen eines A-Datensatzes aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-123">In diesem Beispiel wird ein A-Datensatz aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="b31e0-124">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="b31e0-125">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-126">Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-127">In diesem Beispiel wird ein AAAA-Datensatz aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="b31e0-128">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="b31e0-129">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-130">Beispiel 3: Entfernen eines #A0 aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-131">In diesem Beispiel wird ein #A0 aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="b31e0-132">Da ein #A0 mindestens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="b31e0-133">Beispiel 4: Entfernen eines MX-Eintrags aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-134">In diesem Beispiel wird ein "MX"-Eintrag aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="b31e0-135">Der Datensatzname "@" steht für einen Datensatzsatz an der Anschlagspitze der Zone.</span><span class="sxs-lookup"><span data-stu-id="b31e0-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="b31e0-136">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b31e0-137">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-138">Beispiel 5: Entfernen eines Neuen Datensatzes aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-139">In diesem Beispiel wird ein NS-Datensatz aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="b31e0-140">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b31e0-141">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-142">Beispiel 6: Entfernen eines PTR-Eintrags aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-143">In diesem Beispiel wird ein PtR-Datensatz aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="b31e0-144">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b31e0-145">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-146">Beispiel 7: Entfernen eines SRV-Eintrags aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-147">In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="b31e0-148">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b31e0-149">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b31e0-150">Beispiel 8: Entfernen eines TXT-Eintrags aus einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="b31e0-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="b31e0-151">In diesem Beispiel wird ein "TXT"-Eintrag aus einem vorhandenen Datensatzsatz entfernt.</span><span class="sxs-lookup"><span data-stu-id="b31e0-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="b31e0-152">Wenn dies der einzige Datensatz im Datensatzsatz ist, ist das Ergebnis ein leerer Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b31e0-153">Informationen zum vollständigen Entfernen eines Datensatzes finden Sie unter "Remove-AzDnsRecordSet".</span><span class="sxs-lookup"><span data-stu-id="b31e0-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="b31e0-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b31e0-154">PARAMETERS</span></span>

### <span data-ttu-id="b31e0-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="b31e0-155">-CaaFlags</span></span>
<span data-ttu-id="b31e0-156">Die Kennzeichen für den hinzuzufügende CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b31e0-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="b31e0-157">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="b31e0-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="b31e0-158">-CaaTag</span></span>
<span data-ttu-id="b31e0-159">Das Tagfeld des hinzuzufügende ZERTIFIZIERUNGA-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="b31e0-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="b31e0-160">-CaaValue</span></span>
<span data-ttu-id="b31e0-161">Das Wertfeld für den hinzuzufügende ZERTIFIZIERUNGA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="b31e0-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="b31e0-162">-Cname</span></span>
<span data-ttu-id="b31e0-163">Gibt den Domänennamen für einen kanonischen Namen (CNAME)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31e0-164">-DefaultProfile</span></span>
<span data-ttu-id="b31e0-165">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b31e0-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b31e0-166">-Exchange</span></span>
<span data-ttu-id="b31e0-167">Gibt den E-Mail-Exchange-Servernamen für einen Mail Exchange (MX)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="b31e0-168">-Ipv4Address</span></span>
<span data-ttu-id="b31e0-169">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-169">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="b31e0-170">-Ipv6Address</span></span>
<span data-ttu-id="b31e0-171">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="b31e0-172">-Nsdname</span></span>
<span data-ttu-id="b31e0-173">Gibt den Namenserver für einen Namenserverdatensatz an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-174">-Port</span><span class="sxs-lookup"><span data-stu-id="b31e0-174">-Port</span></span>
<span data-ttu-id="b31e0-175">Gibt den Port für einen Dienstdatensatz (SRV) an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-176">-Preference</span><span class="sxs-lookup"><span data-stu-id="b31e0-176">-Preference</span></span>
<span data-ttu-id="b31e0-177">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="b31e0-178">-Priority</span></span>
<span data-ttu-id="b31e0-179">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="b31e0-180">-Ptrdname</span></span>
<span data-ttu-id="b31e0-181">Gibt den Zieldomänennamen eines Zeigerdatensatzs (PTR) an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="b31e0-182">-RecordSet</span></span>
<span data-ttu-id="b31e0-183">Gibt das **RecordSet-Objekt** an, das den zu entfernenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="b31e0-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-184">-Target</span><span class="sxs-lookup"><span data-stu-id="b31e0-184">-Target</span></span>
<span data-ttu-id="b31e0-185">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-186">-Value</span><span class="sxs-lookup"><span data-stu-id="b31e0-186">-Value</span></span>
<span data-ttu-id="b31e0-187">Gibt den Wert für einen "TXT"-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="b31e0-188">-Weight</span></span>
<span data-ttu-id="b31e0-189">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="b31e0-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31e0-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31e0-190">CommonParameters</span></span>
<span data-ttu-id="b31e0-191">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31e0-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31e0-192">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b31e0-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31e0-193">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b31e0-193">INPUTS</span></span>

### <span data-ttu-id="b31e0-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b31e0-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="b31e0-195">System.String</span><span class="sxs-lookup"><span data-stu-id="b31e0-195">System.String</span></span>

### <span data-ttu-id="b31e0-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="b31e0-196">System.UInt16</span></span>

### <span data-ttu-id="b31e0-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="b31e0-197">System.Byte</span></span>

## <span data-ttu-id="b31e0-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b31e0-198">OUTPUTS</span></span>

### <span data-ttu-id="b31e0-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b31e0-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b31e0-200">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b31e0-200">NOTES</span></span>

## <span data-ttu-id="b31e0-201">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b31e0-201">RELATED LINKS</span></span>

[<span data-ttu-id="b31e0-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b31e0-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="b31e0-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b31e0-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b31e0-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b31e0-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
