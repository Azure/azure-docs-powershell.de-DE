---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: cc1f4186d63b67619734cbfad807d114e2be5463
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500230"
---
# <span data-ttu-id="475c2-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="475c2-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="475c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="475c2-102">SYNOPSIS</span></span>
<span data-ttu-id="475c2-103">Fügt einen DNS-Eintrag zu einem lokalen Datensatzobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="475c2-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="475c2-104">SYNTAX</span></span>

### <span data-ttu-id="475c2-105">Eine</span><span class="sxs-lookup"><span data-stu-id="475c2-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="475c2-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-107">NS</span><span class="sxs-lookup"><span data-stu-id="475c2-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-108">MX</span><span class="sxs-lookup"><span data-stu-id="475c2-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-109">PTR</span><span class="sxs-lookup"><span data-stu-id="475c2-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-110">TXT</span><span class="sxs-lookup"><span data-stu-id="475c2-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="475c2-111">SRV</span><span class="sxs-lookup"><span data-stu-id="475c2-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475c2-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="475c2-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="475c2-113">CAA</span><span class="sxs-lookup"><span data-stu-id="475c2-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475c2-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="475c2-114">DESCRIPTION</span></span>
<span data-ttu-id="475c2-115">Mit dem Cmdlet **Add-AzureRmDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) zu einem **Recordset** -Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="475c2-116">Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="475c2-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="475c2-117">Bei der Erstellung einer DNS-Zone werden SOA-Einträge erstellt, die beim Löschen der DNS-Zone entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="475c2-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="475c2-118">Sie können keine SOA-Einträge hinzufügen oder entfernen, aber Sie können Sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="475c2-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="475c2-119">Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="475c2-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="475c2-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="475c2-120">EXAMPLES</span></span>

### <span data-ttu-id="475c2-121">Beispiel 1: Hinzufügen eines a-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-122">In diesem Beispiel wird ein A-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="475c2-123">Beispiel 2: Hinzufügen eines AAAA-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-124">In diesem Beispiel wird ein AAAA-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="475c2-125">Beispiel 3: Hinzufügen eines CNAME-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-126">In diesem Beispiel wird ein CNAME-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="475c2-127">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, muss er zunächst ein leerer Daten Satz Satz sein, oder vorhandene Datensätze müssen mithilfe von Remove-AzureRmDnsRecordConfig entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="475c2-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="475c2-128">Beispiel 4: Hinzufügen eines MX-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-129">In diesem Beispiel wird ein MX-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="475c2-130">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="475c2-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="475c2-131">Beispiel 5: Hinzufügen eines NS-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-132">In diesem Beispiel wird ein NS-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="475c2-133">Beispiel 6: Hinzufügen eines PTR-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-134">In diesem Beispiel wird ein PTR-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="475c2-135">Beispiel 7: Hinzufügen eines SRV-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-136">In diesem Beispiel wird ein SRV-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="475c2-137">Beispiel 8: Hinzufügen eines txt-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="475c2-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="475c2-138">In diesem Beispiel wird ein TXT-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="475c2-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="475c2-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="475c2-139">PARAMETERS</span></span>

### <span data-ttu-id="475c2-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="475c2-140">-CaaFlags</span></span>
<span data-ttu-id="475c2-141">Die Flags für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="475c2-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="475c2-142">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="475c2-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="475c2-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="475c2-143">-CaaTag</span></span>
<span data-ttu-id="475c2-144">Das Tag-Feld des hinzuzufügenden CAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="475c2-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="475c2-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="475c2-145">-CaaValue</span></span>
<span data-ttu-id="475c2-146">Das Feld "Wert" für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="475c2-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="475c2-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="475c2-147">-Cname</span></span>
<span data-ttu-id="475c2-148">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="475c2-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="475c2-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475c2-149">-DefaultProfile</span></span>
<span data-ttu-id="475c2-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="475c2-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="475c2-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="475c2-151">-Exchange</span></span>
<span data-ttu-id="475c2-152">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="475c2-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="475c2-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="475c2-153">-Ipv4Address</span></span>
<span data-ttu-id="475c2-154">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="475c2-155">-IPv6</span><span class="sxs-lookup"><span data-stu-id="475c2-155">-Ipv6Address</span></span>
<span data-ttu-id="475c2-156">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="475c2-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="475c2-157">-Nsdname</span></span>
<span data-ttu-id="475c2-158">Gibt den Namenserver Namen für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="475c2-159">-Port</span><span class="sxs-lookup"><span data-stu-id="475c2-159">-Port</span></span>
<span data-ttu-id="475c2-160">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="475c2-161">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="475c2-161">-Preference</span></span>
<span data-ttu-id="475c2-162">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="475c2-163">-Priorität</span><span class="sxs-lookup"><span data-stu-id="475c2-163">-Priority</span></span>
<span data-ttu-id="475c2-164">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="475c2-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="475c2-165">-Ptrdname</span></span>
<span data-ttu-id="475c2-166">Gibt den Zieldomänen Namen eines PTR-Eintrags (Pointer Resource) an.</span><span class="sxs-lookup"><span data-stu-id="475c2-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="475c2-167">-Recordset</span><span class="sxs-lookup"><span data-stu-id="475c2-167">-RecordSet</span></span>
<span data-ttu-id="475c2-168">Gibt das **Recordset** -Objekt an, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="475c2-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="475c2-169">-Target</span><span class="sxs-lookup"><span data-stu-id="475c2-169">-Target</span></span>
<span data-ttu-id="475c2-170">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="475c2-171">-Wert</span><span class="sxs-lookup"><span data-stu-id="475c2-171">-Value</span></span>
<span data-ttu-id="475c2-172">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="475c2-173">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="475c2-173">-Weight</span></span>
<span data-ttu-id="475c2-174">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="475c2-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="475c2-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475c2-175">CommonParameters</span></span>
<span data-ttu-id="475c2-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475c2-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475c2-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475c2-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475c2-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="475c2-178">INPUTS</span></span>

### <span data-ttu-id="475c2-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="475c2-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="475c2-180">Parameter: Recordset (ByValue)</span><span class="sxs-lookup"><span data-stu-id="475c2-180">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="475c2-181">System. String</span><span class="sxs-lookup"><span data-stu-id="475c2-181">System.String</span></span>

### <span data-ttu-id="475c2-182">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="475c2-182">System.UInt16</span></span>

### <span data-ttu-id="475c2-183">System. Byte</span><span class="sxs-lookup"><span data-stu-id="475c2-183">System.Byte</span></span>

## <span data-ttu-id="475c2-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="475c2-184">OUTPUTS</span></span>

### <span data-ttu-id="475c2-185">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="475c2-185">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="475c2-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="475c2-186">NOTES</span></span>

## <span data-ttu-id="475c2-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="475c2-187">RELATED LINKS</span></span>

[<span data-ttu-id="475c2-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="475c2-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="475c2-189">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="475c2-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="475c2-190">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="475c2-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
