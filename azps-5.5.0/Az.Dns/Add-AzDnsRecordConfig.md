---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163593"
---
# <span data-ttu-id="bc7d4-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bc7d4-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="bc7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7d4-103">Fügt einem lokalen Datensatzsatzobjekt einen DNS-Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="bc7d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc7d4-104">SYNTAX</span></span>

### <span data-ttu-id="bc7d4-105">A</span><span class="sxs-lookup"><span data-stu-id="bc7d4-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="bc7d4-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-107">NS</span><span class="sxs-lookup"><span data-stu-id="bc7d4-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-108">MX</span><span class="sxs-lookup"><span data-stu-id="bc7d4-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-109">PTR</span><span class="sxs-lookup"><span data-stu-id="bc7d4-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-110">TXT</span><span class="sxs-lookup"><span data-stu-id="bc7d4-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-111">SRV</span><span class="sxs-lookup"><span data-stu-id="bc7d4-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="bc7d4-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7d4-113">Caa</span><span class="sxs-lookup"><span data-stu-id="bc7d4-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc7d4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc7d4-114">DESCRIPTION</span></span>
<span data-ttu-id="bc7d4-115">Das **Cmdlet "Add-AzDnsRecordConfig"** fügt einem "RecordSet"-Objekt einen Domain Name System **(DNS)-Eintrag** hinzu.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="bc7d4-116">Das **Objekt "RecordSet"** ist ein Offlineobjekt, und änderungen an diesem Objekt ändern die DNS-Antworten erst, nachdem Sie das Cmdlet "Set-AzDnsRecordSet" ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="bc7d4-117">SOA-Einträge werden erstellt, wenn eine DNS-Zone erstellt wird, und beim Löschen der DNS-Zone entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="bc7d4-118">Sie können keine SOA-Einträge hinzufügen oder entfernen, sie aber bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="bc7d4-119">Sie können das **Objekt "RecordSet"** als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="bc7d4-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc7d4-120">EXAMPLES</span></span>

### <span data-ttu-id="bc7d4-121">Beispiel 1: Hinzufügen eines A-Datensatzes zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-122">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein A-Datensatz hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="bc7d4-123">Beispiel 2: Hinzufügen eines AAAA-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-124">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein AAAA-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="bc7d4-125">Beispiel 3: Hinzufügen eines #A0 zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-126">In diesem Beispiel wird einem vorhandenen Datensatz ein #A0 hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="bc7d4-127">Da ein #A0 mindestens einen Datensatz enthalten kann, muss er zunächst ein leerer Datensatzsatz sein, oder vorhandene Datensätze müssen mithilfe von "Remove-AzDnsRecordConfig" entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="bc7d4-128">Beispiel 4: Hinzufügen eines MX-Eintrags zu einem Eintragssatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-129">In diesem Beispiel wird einem vorhandenen Eintragssatz ein "MX"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="bc7d4-130">Der Datensatzname "@" steht für einen Datensatzsatz an der Anschlagspitze der Zone.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="bc7d4-131">Beispiel 5: Hinzufügen eines NS-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-132">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein NS-Datensatz hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="bc7d4-133">Beispiel 6: Hinzufügen eines PTR-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-134">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein PtR-Datensatz hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="bc7d4-135">Beispiel 7: Hinzufügen eines SRV-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-136">In diesem Beispiel wird einem vorhandenen Datensatz ein "SRV"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="bc7d4-137">Beispiel 8: Hinzufügen eines TXT-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="bc7d4-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="bc7d4-138">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein "TXT"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="bc7d4-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc7d4-139">PARAMETERS</span></span>

### <span data-ttu-id="bc7d4-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="bc7d4-140">-CaaFlags</span></span>
<span data-ttu-id="bc7d4-141">Die Kennzeichen für den hinzuzufügende CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="bc7d4-142">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="bc7d4-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="bc7d4-143">-CaaTag</span></span>
<span data-ttu-id="bc7d4-144">Das Tagfeld des hinzuzufügende ZERTIFIZIERUNGA-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="bc7d4-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="bc7d4-145">-CaaValue</span></span>
<span data-ttu-id="bc7d4-146">Das Wertfeld für den hinzuzufügende ZERTIFIZIERUNGA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="bc7d4-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="bc7d4-147">-Cname</span></span>
<span data-ttu-id="bc7d4-148">Gibt den Domänennamen für einen kanonischen Namen (CNAME)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="bc7d4-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7d4-149">-DefaultProfile</span></span>
<span data-ttu-id="bc7d4-150">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bc7d4-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc7d4-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="bc7d4-151">-Exchange</span></span>
<span data-ttu-id="bc7d4-152">Gibt den E-Mail-Exchange-Servernamen für einen Mail Exchange (MX)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="bc7d4-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="bc7d4-153">-Ipv4Address</span></span>
<span data-ttu-id="bc7d4-154">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="bc7d4-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="bc7d4-155">-Ipv6Address</span></span>
<span data-ttu-id="bc7d4-156">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="bc7d4-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="bc7d4-157">-Nsdname</span></span>
<span data-ttu-id="bc7d4-158">Gibt den Namen des Namenservers für einen Namenserverdatensatz an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="bc7d4-159">-Port</span><span class="sxs-lookup"><span data-stu-id="bc7d4-159">-Port</span></span>
<span data-ttu-id="bc7d4-160">Gibt den Port für einen Dienstdatensatz (SRV) an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="bc7d4-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="bc7d4-161">-Preference</span></span>
<span data-ttu-id="bc7d4-162">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="bc7d4-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="bc7d4-163">-Priority</span></span>
<span data-ttu-id="bc7d4-164">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="bc7d4-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="bc7d4-165">-Ptrdname</span></span>
<span data-ttu-id="bc7d4-166">Gibt den Zieldomänennamen eines Zeigerressourcendatensatzes (PtR) an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="bc7d4-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="bc7d4-167">-RecordSet</span></span>
<span data-ttu-id="bc7d4-168">Gibt das zu **bearbeitende "RecordSet"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="bc7d4-169">-Target</span><span class="sxs-lookup"><span data-stu-id="bc7d4-169">-Target</span></span>
<span data-ttu-id="bc7d4-170">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="bc7d4-171">-Value</span><span class="sxs-lookup"><span data-stu-id="bc7d4-171">-Value</span></span>
<span data-ttu-id="bc7d4-172">Gibt den Wert für einen "TXT"-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="bc7d4-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="bc7d4-173">-Weight</span></span>
<span data-ttu-id="bc7d4-174">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="bc7d4-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7d4-175">CommonParameters</span></span>
<span data-ttu-id="bc7d4-176">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc7d4-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7d4-177">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc7d4-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7d4-178">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc7d4-178">INPUTS</span></span>

### <span data-ttu-id="bc7d4-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bc7d4-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="bc7d4-180">System.String</span><span class="sxs-lookup"><span data-stu-id="bc7d4-180">System.String</span></span>

### <span data-ttu-id="bc7d4-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="bc7d4-181">System.UInt16</span></span>

### <span data-ttu-id="bc7d4-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="bc7d4-182">System.Byte</span></span>

## <span data-ttu-id="bc7d4-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc7d4-183">OUTPUTS</span></span>

### <span data-ttu-id="bc7d4-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bc7d4-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="bc7d4-185">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc7d4-185">NOTES</span></span>

## <span data-ttu-id="bc7d4-186">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc7d4-186">RELATED LINKS</span></span>

[<span data-ttu-id="bc7d4-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bc7d4-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="bc7d4-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bc7d4-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="bc7d4-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bc7d4-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
