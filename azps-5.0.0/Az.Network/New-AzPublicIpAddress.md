---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 3bfed7f4c980ab246f4e38d500860ccd4e2ef09f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301930"
---
# <span data-ttu-id="1956a-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1956a-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="1956a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1956a-102">SYNOPSIS</span></span>
<span data-ttu-id="1956a-103">Erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1956a-103">Creates a public IP address.</span></span>

## <span data-ttu-id="1956a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1956a-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1956a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1956a-105">DESCRIPTION</span></span>
<span data-ttu-id="1956a-106">Das Cmdlet **New-AzPublicIpAddress** erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1956a-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="1956a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1956a-107">EXAMPLES</span></span>

### <span data-ttu-id="1956a-108">Beispiel 1: Erstellen einer neuen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="1956a-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="1956a-109">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt. Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="1956a-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="1956a-110">Eine öffentliche IP-Adresse wird dieser Ressource sofort zugewiesen, da die-AllocationMethod als "statisch" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1956a-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="1956a-111">Wenn Sie als "dynamisch" festgelegt ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (wie ein VM-oder Load Balancer) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="1956a-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="1956a-112">Beispiel 2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN</span><span class="sxs-lookup"><span data-stu-id="1956a-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="1956a-113">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="1956a-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="1956a-114">Mit dem-ReverseFqdn-Parameter erstellt Azure einen DNS-PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und zeigt auf die im Befehl angegebene $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="1956a-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="1956a-115">Als Voraussetzung sollten die $customFqdn (sagen wir webapp.contoso.com) einen DNS-CNAME-Eintrag (Forward-Lookup) aufweisen, der auf $dnsPrefix. $Location. cloudapp.Azure.com verweist.</span><span class="sxs-lookup"><span data-stu-id="1956a-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="1956a-116">Beispiel 3: Erstellen einer neuen öffentlichen IP-Adresse mit IpTag</span><span class="sxs-lookup"><span data-stu-id="1956a-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="1956a-117">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt. Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="1956a-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="1956a-118">Eine öffentliche IP-Adresse wird dieser Ressource sofort zugewiesen, da die-AllocationMethod als "statisch" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1956a-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="1956a-119">Wenn Sie als "dynamisch" festgelegt ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (wie ein VM-oder Load Balancer) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="1956a-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="1956a-120">Ein Iptag wird verwendet, um die der Ressource zugeordneten Kategorien zu Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="1956a-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="1956a-121">Iptag kann mithilfe von New-AzPublicIpTag angegeben und als Eingabe über-IpTags übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1956a-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="1956a-122">Beispiel 4: Erstellen einer neuen öffentlichen IP-Adresse aus einem Präfix</span><span class="sxs-lookup"><span data-stu-id="1956a-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="1956a-123">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="1956a-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="1956a-124">Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="1956a-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="1956a-125">Eine öffentliche IP-Adresse wird dieser Ressource sofort aus dem angegebenen publicIpPrefix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1956a-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="1956a-126">Diese Option wird nur für die "Standard"-SKU und "static"-AllocationMethod unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1956a-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="1956a-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="1956a-127">PARAMETERS</span></span>

### <span data-ttu-id="1956a-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="1956a-128">-AllocationMethod</span></span>
<span data-ttu-id="1956a-129">Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956a-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="1956a-130">Die zulässigen Werte für diesen Parameter sind static oder Dynamic.</span><span class="sxs-lookup"><span data-stu-id="1956a-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1956a-131">-AsJob</span></span>
<span data-ttu-id="1956a-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1956a-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1956a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1956a-133">-DefaultProfile</span></span>
<span data-ttu-id="1956a-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1956a-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1956a-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="1956a-135">-DomainNameLabel</span></span>
<span data-ttu-id="1956a-136">Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="1956a-136">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-137">-Force</span><span class="sxs-lookup"><span data-stu-id="1956a-137">-Force</span></span>
<span data-ttu-id="1956a-138">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1956a-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1956a-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1956a-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1956a-140">Gibt das Leerlauftimeout in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="1956a-140">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="1956a-141">-IpAddressVersion</span></span>
<span data-ttu-id="1956a-142">Gibt die Version der IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="1956a-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="1956a-143">-IpTag</span></span>
<span data-ttu-id="1956a-144">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="1956a-144">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="1956a-145">-Location</span></span>
<span data-ttu-id="1956a-146">Gibt den Bereich an, in dem eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956a-146">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-147">-Name</span><span class="sxs-lookup"><span data-stu-id="1956a-147">-Name</span></span>
<span data-ttu-id="1956a-148">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1956a-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-149">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1956a-149">-PublicIpPrefix</span></span>
<span data-ttu-id="1956a-150">Gibt den PSPublicIpPrefix an, aus dem die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956a-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1956a-151">-ResourceGroupName</span></span>
<span data-ttu-id="1956a-152">Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956a-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="1956a-153">-ReverseFqdn</span></span>
<span data-ttu-id="1956a-154">Gibt einen umgekehrten vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) an.</span><span class="sxs-lookup"><span data-stu-id="1956a-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="1956a-155">-Sku</span></span>
<span data-ttu-id="1956a-156">Der öffentliche IP-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="1956a-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="1956a-157">-Tag</span></span>
<span data-ttu-id="1956a-158">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1956a-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1956a-159">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1956a-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="1956a-160">-Zone</span></span>
<span data-ttu-id="1956a-161">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="1956a-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1956a-162">-Confirm</span></span>
<span data-ttu-id="1956a-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1956a-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1956a-164">-WhatIf</span></span>
<span data-ttu-id="1956a-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1956a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1956a-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1956a-166">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1956a-167">CommonParameters</span></span>
<span data-ttu-id="1956a-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1956a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1956a-169">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1956a-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1956a-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1956a-170">INPUTS</span></span>

### <span data-ttu-id="1956a-171">System. String</span><span class="sxs-lookup"><span data-stu-id="1956a-171">System.String</span></span>

### <span data-ttu-id="1956a-172">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="1956a-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="1956a-173">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1956a-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="1956a-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1956a-174">System.Int32</span></span>

### <span data-ttu-id="1956a-175">System. String []</span><span class="sxs-lookup"><span data-stu-id="1956a-175">System.String[]</span></span>

### <span data-ttu-id="1956a-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1956a-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1956a-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1956a-177">OUTPUTS</span></span>

### <span data-ttu-id="1956a-178">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1956a-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1956a-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="1956a-179">NOTES</span></span>

## <span data-ttu-id="1956a-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1956a-180">RELATED LINKS</span></span>

[<span data-ttu-id="1956a-181">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1956a-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="1956a-182">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1956a-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="1956a-183">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1956a-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
