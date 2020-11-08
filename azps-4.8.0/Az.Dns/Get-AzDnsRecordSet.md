---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009856"
---
# <span data-ttu-id="7268e-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7268e-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="7268e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7268e-102">SYNOPSIS</span></span>
<span data-ttu-id="7268e-103">Ruft einen DNS-Eintragssatz ab.</span><span class="sxs-lookup"><span data-stu-id="7268e-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="7268e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7268e-104">SYNTAX</span></span>

### <span data-ttu-id="7268e-105">Felder</span><span class="sxs-lookup"><span data-stu-id="7268e-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7268e-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="7268e-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7268e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7268e-107">DESCRIPTION</span></span>
<span data-ttu-id="7268e-108">Das Cmdlet " **Get-AzDnsRecordSet** " Ruft den DNS-Eintragssatz (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone ab.</span><span class="sxs-lookup"><span data-stu-id="7268e-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="7268e-109">Wenn Sie die Parameter *Name* oder *RecordType* nicht angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Typs in der Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="7268e-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="7268e-110">Wenn Sie den Parameter *RecordType* , aber nicht den Parameter *Name* angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Datensatztyps zurück.</span><span class="sxs-lookup"><span data-stu-id="7268e-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="7268e-111">Sie können den Pipelineoperator verwenden, um ein **dnsZone** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **dnsZone** -Objekt als *Zone* -Parameter übergeben, oder Alternativ können Sie die Zone und die Ressourcengruppe nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="7268e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7268e-112">EXAMPLES</span></span>

### <span data-ttu-id="7268e-113">Beispiel 1: Abrufen von Daten Satz Sätzen mit einem angegebenen Namen und Typ</span><span class="sxs-lookup"><span data-stu-id="7268e-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="7268e-114">Dieser Befehl ruft den Daten Satz Satz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in der $Recordset-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7268e-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="7268e-115">Da die Parameter *Name* und *RecordType* angegeben werden, wird nur ein **Recordset** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="7268e-116">Beispiel 2: Abrufen von Daten Satz Sätzen eines angegebenen Typs</span><span class="sxs-lookup"><span data-stu-id="7268e-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="7268e-117">Dieser Befehl ruft ein Array aller Daten Satz Sätze des Datensatztyps A in der Zone mit dem Namen MyZone.com in der Ressourcengruppe myresourcegroup ab und speichert Sie dann in der $Recordsets Variablen.</span><span class="sxs-lookup"><span data-stu-id="7268e-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="7268e-118">Beispiel 3: Abrufen aller Daten Satz Sätze in einer Zone</span><span class="sxs-lookup"><span data-stu-id="7268e-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="7268e-119">Dieser Befehl ruft ein Array aller Datensatzgruppen in der Zone mit dem Namen MyZone.com in der Ressourcengruppe mit dem Namen myresourcegroup ab und speichert Sie dann in der $Recordsets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7268e-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="7268e-120">Beispiel 4: Abrufen aller Daten Satz Sätze in einer Zone mithilfe eines dnsZone-Objekts</span><span class="sxs-lookup"><span data-stu-id="7268e-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="7268e-121">Dieses Beispiel entspricht Beispiel 3 oben.</span><span class="sxs-lookup"><span data-stu-id="7268e-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="7268e-122">Dieses Mal wird die Zone mithilfe eines Zone-Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="7268e-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7268e-123">PARAMETERS</span></span>

### <span data-ttu-id="7268e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7268e-124">-DefaultProfile</span></span>
<span data-ttu-id="7268e-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7268e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7268e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7268e-126">-Name</span></span>
<span data-ttu-id="7268e-127">Gibt den Namen des abzurufenden **Recordsets** an.</span><span class="sxs-lookup"><span data-stu-id="7268e-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="7268e-128">Wenn Sie den Parameter *Name* nicht angeben, werden alle Daten Satz Sätze des angegebenen Typs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="7268e-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="7268e-129">-RecordType</span></span>
<span data-ttu-id="7268e-130">Gibt den Typ des DNS-Eintrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7268e-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="7268e-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7268e-131">Valid values are:</span></span> 
- <span data-ttu-id="7268e-132">Eine</span><span class="sxs-lookup"><span data-stu-id="7268e-132">A</span></span>
- <span data-ttu-id="7268e-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="7268e-133">AAAA</span></span>
- <span data-ttu-id="7268e-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="7268e-134">CNAME</span></span>
- <span data-ttu-id="7268e-135">MX</span><span class="sxs-lookup"><span data-stu-id="7268e-135">MX</span></span>
- <span data-ttu-id="7268e-136">NS</span><span class="sxs-lookup"><span data-stu-id="7268e-136">NS</span></span>
- <span data-ttu-id="7268e-137">PTR</span><span class="sxs-lookup"><span data-stu-id="7268e-137">PTR</span></span>
- <span data-ttu-id="7268e-138">SOA</span><span class="sxs-lookup"><span data-stu-id="7268e-138">SOA</span></span>
- <span data-ttu-id="7268e-139">SRV</span><span class="sxs-lookup"><span data-stu-id="7268e-139">SRV</span></span>
- <span data-ttu-id="7268e-140">TXT wenn Sie den *RecordType* -Parameter nicht angeben, müssen Sie auch den Parameter *Name* weglassen.</span><span class="sxs-lookup"><span data-stu-id="7268e-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="7268e-141">Dieses Cmdlet gibt dann alle Daten Satz Sätze in der Zone (aller Namen und Typen) zurück.</span><span class="sxs-lookup"><span data-stu-id="7268e-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="7268e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7268e-142">-ResourceGroupName</span></span>
<span data-ttu-id="7268e-143">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="7268e-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="7268e-144">Der Zonen Name muss auch mit dem Parameter *zonename* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7268e-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="7268e-145">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein **dnsZone** -Objekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7268e-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="7268e-146">-Zone</span></span>
<span data-ttu-id="7268e-147">Gibt die DNS-Zone an, die den Daten Satz Satz enthält, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7268e-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="7268e-148">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="7268e-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="7268e-149">-ZoneName</span></span>
<span data-ttu-id="7268e-150">Gibt den Namen der DNS-Zone an, die den aufzurufenden Daten Satz Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="7268e-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="7268e-151">Die Ressourcengruppe mit der Zone muss ebenfalls mithilfe des *ResourceGroupName* -Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7268e-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7268e-152">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7268e-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7268e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7268e-153">CommonParameters</span></span>
<span data-ttu-id="7268e-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7268e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7268e-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7268e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7268e-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7268e-156">INPUTS</span></span>

### <span data-ttu-id="7268e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7268e-157">System.String</span></span>

### <span data-ttu-id="7268e-158">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="7268e-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="7268e-159">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7268e-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7268e-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7268e-160">OUTPUTS</span></span>

### <span data-ttu-id="7268e-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7268e-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="7268e-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="7268e-162">NOTES</span></span>

## <span data-ttu-id="7268e-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7268e-163">RELATED LINKS</span></span>

[<span data-ttu-id="7268e-164">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7268e-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="7268e-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7268e-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="7268e-166">Satz-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7268e-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


