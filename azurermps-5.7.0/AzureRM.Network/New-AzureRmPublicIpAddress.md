---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503726"
---
# <span data-ttu-id="00bc3-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00bc3-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="00bc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="00bc3-103">Erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="00bc3-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00bc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00bc3-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00bc3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="00bc3-106">Das Cmdlet **New-AzureRmPublicIpAddress** erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="00bc3-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="00bc3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="00bc3-108">1: Erstellen einer neuen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="00bc3-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="00bc3-109">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt. Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="00bc3-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="00bc3-110">Eine öffentliche IP-Adresse wird dieser Ressource sofort zugewiesen, da die-AllocationMethod als "statisch" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="00bc3-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="00bc3-111">Wenn Sie als "dynamisch" festgelegt ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (wie ein VM-oder Load Balancer) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="00bc3-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="00bc3-112">2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN</span><span class="sxs-lookup"><span data-stu-id="00bc3-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="00bc3-113">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="00bc3-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="00bc3-114">Mit dem-ReverseFqdn-Parameter erstellt Azure einen DNS-PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und zeigt auf die im Befehl angegebene $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="00bc3-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="00bc3-115">Als Voraussetzung sollten die $customFqdn (sagen wir webapp.contoso.com) einen DNS-CNAME-Eintrag (Forward-Lookup) aufweisen, der auf $dnsPrefix. $Location. cloudapp.Azure.com verweist.</span><span class="sxs-lookup"><span data-stu-id="00bc3-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="00bc3-116">3: Erstellen einer neuen öffentlichen IP-Adresse mit IpTag</span><span class="sxs-lookup"><span data-stu-id="00bc3-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="00bc3-117">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt. Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="00bc3-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="00bc3-118">Eine öffentliche IP-Adresse wird dieser Ressource sofort zugewiesen, da die-AllocationMethod als "statisch" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="00bc3-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="00bc3-119">Wenn Sie als "dynamisch" festgelegt ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (wie ein VM-oder Load Balancer) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="00bc3-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="00bc3-120">Ein Iptag wird verwendet, um die der Ressource zugeordneten Kategorien zu Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="00bc3-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="00bc3-121">Iptag kann mithilfe von New-AzureRmPublicIpTag angegeben und als Eingabe über-IpTags übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="00bc3-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="00bc3-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="00bc3-122">PARAMETERS</span></span>

### <span data-ttu-id="00bc3-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="00bc3-123">-AllocationMethod</span></span>
<span data-ttu-id="00bc3-124">Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="00bc3-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="00bc3-125">Die zulässigen Werte für diesen Parameter sind static oder Dynamic.</span><span class="sxs-lookup"><span data-stu-id="00bc3-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00bc3-126">-AsJob</span></span>
<span data-ttu-id="00bc3-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="00bc3-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00bc3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bc3-128">-DefaultProfile</span></span>
<span data-ttu-id="00bc3-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00bc3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="00bc3-130">-DomainNameLabel</span></span>
<span data-ttu-id="00bc3-131">Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="00bc3-131">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-132">-Force</span><span class="sxs-lookup"><span data-stu-id="00bc3-132">-Force</span></span>
<span data-ttu-id="00bc3-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="00bc3-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00bc3-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="00bc3-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="00bc3-135">Gibt das Leerlauftimeout in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="00bc3-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="00bc3-136">-IpAddressVersion</span></span>
<span data-ttu-id="00bc3-137">Gibt die Version der IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="00bc3-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="00bc3-138">-IpTag</span></span>
<span data-ttu-id="00bc3-139">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="00bc3-139">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-140">-Standort</span><span class="sxs-lookup"><span data-stu-id="00bc3-140">-Location</span></span>
<span data-ttu-id="00bc3-141">Gibt den Bereich an, in dem eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00bc3-141">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-142">-Name</span><span class="sxs-lookup"><span data-stu-id="00bc3-142">-Name</span></span>
<span data-ttu-id="00bc3-143">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc3-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bc3-144">-ResourceGroupName</span></span>
<span data-ttu-id="00bc3-145">Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00bc3-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="00bc3-146">-ReverseFqdn</span></span>
<span data-ttu-id="00bc3-147">Gibt einen umgekehrten vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) an.</span><span class="sxs-lookup"><span data-stu-id="00bc3-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="00bc3-148">-Sku</span></span>
<span data-ttu-id="00bc3-149">Der öffentliche IP-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="00bc3-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="00bc3-150">-Tag</span></span>
<span data-ttu-id="00bc3-151">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="00bc3-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00bc3-152">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="00bc3-152">For example:</span></span>

<span data-ttu-id="00bc3-153">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="00bc3-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="00bc3-154">-Zone</span></span>
<span data-ttu-id="00bc3-155">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="00bc3-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00bc3-156">-Confirm</span></span>
<span data-ttu-id="00bc3-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00bc3-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00bc3-158">-WhatIf</span></span>
<span data-ttu-id="00bc3-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00bc3-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00bc3-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00bc3-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00bc3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bc3-161">CommonParameters</span></span>
<span data-ttu-id="00bc3-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bc3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bc3-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bc3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bc3-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00bc3-164">INPUTS</span></span>

### <span data-ttu-id="00bc3-165">Keine</span><span class="sxs-lookup"><span data-stu-id="00bc3-165">None</span></span>
<span data-ttu-id="00bc3-166">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="00bc3-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00bc3-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00bc3-167">OUTPUTS</span></span>

### <span data-ttu-id="00bc3-168">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00bc3-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="00bc3-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="00bc3-169">NOTES</span></span>

## <span data-ttu-id="00bc3-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00bc3-170">RELATED LINKS</span></span>

[<span data-ttu-id="00bc3-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00bc3-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="00bc3-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00bc3-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="00bc3-173">Satz-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00bc3-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
