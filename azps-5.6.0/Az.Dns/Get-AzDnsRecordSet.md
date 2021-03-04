---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935064"
---
# <span data-ttu-id="c91b0-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c91b0-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="c91b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c91b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c91b0-103">Ruft einen DNS-Eintragssatz ab.</span><span class="sxs-lookup"><span data-stu-id="c91b0-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="c91b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c91b0-104">SYNTAX</span></span>

### <span data-ttu-id="c91b0-105">Felder</span><span class="sxs-lookup"><span data-stu-id="c91b0-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c91b0-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="c91b0-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c91b0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c91b0-107">DESCRIPTION</span></span>
<span data-ttu-id="c91b0-108">Das **Get-AzDnsRecordSet-Cmdlet** ruft den Eintrag Domain Name System (DNS) mit dem angegebenen Namen und Typ in der angegebenen Zone ab.</span><span class="sxs-lookup"><span data-stu-id="c91b0-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="c91b0-109">Wenn Sie die Parameter *Name* oder *RecordType* nicht angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Typs in der Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="c91b0-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="c91b0-110">Wenn Sie den *Parameter RecordType,* aber nicht den *Parameter Name* angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Datensatztyps zurück.</span><span class="sxs-lookup"><span data-stu-id="c91b0-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="c91b0-111">Sie können den Pipelineoperator verwenden, um ein **DnsZone-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **DnsZone-Objekt** als Parameter *Zone* übergeben oder alternativ die Zone und Ressourcengruppe nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="c91b0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c91b0-112">EXAMPLES</span></span>

### <span data-ttu-id="c91b0-113">Beispiel 1: Get record sets with a specified name and type</span><span class="sxs-lookup"><span data-stu-id="c91b0-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="c91b0-114">Dieser Befehl ruft den Datensatzsatz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in der $RecordSet Variablen.</span><span class="sxs-lookup"><span data-stu-id="c91b0-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c91b0-115">Da die *Parameter Name* und *RecordType* angegeben werden, wird nur ein **RecordSet-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="c91b0-116">Beispiel 2: Get record sets of a specified type</span><span class="sxs-lookup"><span data-stu-id="c91b0-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="c91b0-117">Dieser Befehl ruft ein Array aller Datensatzsätze des Datensatztyps A in der Zone mit dem Namen myzone.com in der Ressourcengruppe mit dem Namen MyResourceGroup ab und speichert sie dann in der $RecordSets-Variable.</span><span class="sxs-lookup"><span data-stu-id="c91b0-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="c91b0-118">Beispiel 3: Alle Datensatzsätze in einer Zone erhalten</span><span class="sxs-lookup"><span data-stu-id="c91b0-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="c91b0-119">Dieser Befehl ruft ein Array aller Datensatzsätze in der Zone mit dem Namen myzone.com in der Ressourcengruppe mit dem Namen MyResourceGroup ab und speichert sie dann in der $RecordSets Variablen.</span><span class="sxs-lookup"><span data-stu-id="c91b0-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="c91b0-120">Beispiel 4: Alle Datensatzsätze in einer Zone mithilfe eines DnsZone-Objekts</span><span class="sxs-lookup"><span data-stu-id="c91b0-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="c91b0-121">Dieses Beispiel entspricht dem obigen Beispiel 3.</span><span class="sxs-lookup"><span data-stu-id="c91b0-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="c91b0-122">Dieses Mal wird die Zone mit einem Zonenobjekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="c91b0-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c91b0-123">PARAMETERS</span></span>

### <span data-ttu-id="c91b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91b0-124">-DefaultProfile</span></span>
<span data-ttu-id="c91b0-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c91b0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c91b0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c91b0-126">-Name</span></span>
<span data-ttu-id="c91b0-127">Gibt den Namen des **zu erhaltenden RecordSets** an.</span><span class="sxs-lookup"><span data-stu-id="c91b0-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="c91b0-128">Wenn Sie den Parameter Name *nicht angeben,* werden alle Datensatzsätze des angegebenen Typs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91b0-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="c91b0-129">-RecordType</span></span>
<span data-ttu-id="c91b0-130">Gibt den Typ des DNS-Eintrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c91b0-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="c91b0-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c91b0-131">Valid values are:</span></span> 
- <span data-ttu-id="c91b0-132">A</span><span class="sxs-lookup"><span data-stu-id="c91b0-132">A</span></span>
- <span data-ttu-id="c91b0-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="c91b0-133">AAAA</span></span>
- <span data-ttu-id="c91b0-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="c91b0-134">CNAME</span></span>
- <span data-ttu-id="c91b0-135">MX</span><span class="sxs-lookup"><span data-stu-id="c91b0-135">MX</span></span>
- <span data-ttu-id="c91b0-136">NS</span><span class="sxs-lookup"><span data-stu-id="c91b0-136">NS</span></span>
- <span data-ttu-id="c91b0-137">PTR</span><span class="sxs-lookup"><span data-stu-id="c91b0-137">PTR</span></span>
- <span data-ttu-id="c91b0-138">SOA</span><span class="sxs-lookup"><span data-stu-id="c91b0-138">SOA</span></span>
- <span data-ttu-id="c91b0-139">SRV</span><span class="sxs-lookup"><span data-stu-id="c91b0-139">SRV</span></span>
- <span data-ttu-id="c91b0-140">TXT Wenn Sie den Parameter *RecordType nicht* angeben, müssen Sie auch den Parameter *Name weglassen.*</span><span class="sxs-lookup"><span data-stu-id="c91b0-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="c91b0-141">Dieses Cmdlet gibt dann alle Datensatzsätze in der Zone (aller Namen und Typen) zurück.</span><span class="sxs-lookup"><span data-stu-id="c91b0-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91b0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91b0-142">-ResourceGroupName</span></span>
<span data-ttu-id="c91b0-143">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="c91b0-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="c91b0-144">Der Zonenname muss auch mit dem Parameter *ZoneName angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="c91b0-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="c91b0-145">Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein **DnsZone-Objekt** mit dem Parameter *Zone* übergeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91b0-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="c91b0-146">-Zone</span></span>
<span data-ttu-id="c91b0-147">Gibt die DNS-Zone an, die den Datensatzsatz enthält, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c91b0-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="c91b0-148">Alternativ können Sie die Zone mithilfe der *Parameter ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c91b0-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c91b0-149">-ZoneName</span></span>
<span data-ttu-id="c91b0-150">Gibt den Namen der DNS-Zone an, die den zu erhaltenden Eintrag enthält.</span><span class="sxs-lookup"><span data-stu-id="c91b0-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="c91b0-151">Die Ressourcengruppe, die die Zone enthält, muss auch mithilfe des *Parameters ResourceGroupName angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="c91b0-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="c91b0-152">Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein DNS Zone-Objekt mit dem Parameter *Zone* übergeben.</span><span class="sxs-lookup"><span data-stu-id="c91b0-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91b0-153">CommonParameters</span></span>
<span data-ttu-id="c91b0-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91b0-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c91b0-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91b0-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c91b0-156">INPUTS</span></span>

### <span data-ttu-id="c91b0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c91b0-157">System.String</span></span>

### <span data-ttu-id="c91b0-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c91b0-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="c91b0-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c91b0-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c91b0-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c91b0-160">OUTPUTS</span></span>

### <span data-ttu-id="c91b0-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c91b0-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c91b0-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c91b0-162">NOTES</span></span>

## <span data-ttu-id="c91b0-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c91b0-163">RELATED LINKS</span></span>

[<span data-ttu-id="c91b0-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c91b0-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="c91b0-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c91b0-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="c91b0-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c91b0-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


