---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841287"
---
# <span data-ttu-id="8bee5-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bee5-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="8bee5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bee5-102">SYNOPSIS</span></span>
<span data-ttu-id="8bee5-103">Erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8bee5-103">Creates a public IP address.</span></span>

## <span data-ttu-id="8bee5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bee5-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bee5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bee5-105">DESCRIPTION</span></span>
<span data-ttu-id="8bee5-106">Das Cmdlet **New-AzPublicIpAddress** erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8bee5-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="8bee5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bee5-107">EXAMPLES</span></span>

### <span data-ttu-id="8bee5-108">1: Erstellen einer neuen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="8bee5-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="8bee5-109">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt. Für $dnsPrefix. $Location. cloudapp.Azure.com wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="8bee5-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="8bee5-110">Eine öffentliche IP-Adresse wird dieser Ressource sofort zugewiesen, da die-AllocationMethod als "statisch" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8bee5-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="8bee5-111">Wenn Sie als "dynamisch" festgelegt ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (wie ein VM-oder Load Balancer) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="8bee5-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="8bee5-112">2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN</span><span class="sxs-lookup"><span data-stu-id="8bee5-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="8bee5-113">Mit diesem Befehl wird eine neue öffentliche IP-Adressen Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="8bee5-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="8bee5-114">Mit dem-ReverseFqdn-Parameter erstellt Azure einen DNS-PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und zeigt auf die im Befehl angegebene $customFqdn.</span><span class="sxs-lookup"><span data-stu-id="8bee5-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="8bee5-115">Als Voraussetzung sollten die $customFqdn (sagen wir webapp.contoso.com) einen DNS-CNAME-Eintrag (Forward-Lookup) aufweisen, der auf $dnsPrefix. $Location. cloudapp.Azure.com verweist.</span><span class="sxs-lookup"><span data-stu-id="8bee5-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="8bee5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bee5-116">PARAMETERS</span></span>

### <span data-ttu-id="8bee5-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="8bee5-117">-AllocationMethod</span></span>
<span data-ttu-id="8bee5-118">Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bee5-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="8bee5-119">Die zulässigen Werte für diesen Parameter sind static oder Dynamic.</span><span class="sxs-lookup"><span data-stu-id="8bee5-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="8bee5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bee5-120">-AsJob</span></span>
<span data-ttu-id="8bee5-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8bee5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bee5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bee5-122">-DefaultProfile</span></span>
<span data-ttu-id="8bee5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bee5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bee5-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="8bee5-124">-DomainNameLabel</span></span>
<span data-ttu-id="8bee5-125">Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="8bee5-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="8bee5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8bee5-126">-Force</span></span>
<span data-ttu-id="8bee5-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8bee5-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8bee5-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8bee5-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8bee5-129">Gibt das Leerlauftimeout in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="8bee5-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="8bee5-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8bee5-130">-IpAddressVersion</span></span>
<span data-ttu-id="8bee5-131">Gibt die Version der IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="8bee5-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="8bee5-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="8bee5-132">-Location</span></span>
<span data-ttu-id="8bee5-133">Gibt den Bereich an, in dem eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bee5-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="8bee5-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8bee5-134">-Name</span></span>
<span data-ttu-id="8bee5-135">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8bee5-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8bee5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bee5-136">-ResourceGroupName</span></span>
<span data-ttu-id="8bee5-137">Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bee5-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="8bee5-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="8bee5-138">-ReverseFqdn</span></span>
<span data-ttu-id="8bee5-139">Gibt einen umgekehrten vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) an.</span><span class="sxs-lookup"><span data-stu-id="8bee5-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="8bee5-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="8bee5-140">-Sku</span></span>
<span data-ttu-id="8bee5-141">Der öffentliche IP-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="8bee5-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="8bee5-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bee5-142">-Tag</span></span>
<span data-ttu-id="8bee5-143">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8bee5-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8bee5-144">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8bee5-144">For example:</span></span>

<span data-ttu-id="8bee5-145">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8bee5-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8bee5-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="8bee5-146">-Zone</span></span>
<span data-ttu-id="8bee5-147">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="8bee5-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8bee5-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bee5-148">-Confirm</span></span>
<span data-ttu-id="8bee5-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bee5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bee5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bee5-150">-WhatIf</span></span>
<span data-ttu-id="8bee5-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bee5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bee5-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bee5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bee5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bee5-153">CommonParameters</span></span>
<span data-ttu-id="8bee5-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bee5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bee5-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bee5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bee5-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bee5-156">INPUTS</span></span>

## <span data-ttu-id="8bee5-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bee5-157">OUTPUTS</span></span>

### <span data-ttu-id="8bee5-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bee5-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8bee5-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bee5-159">NOTES</span></span>

## <span data-ttu-id="8bee5-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bee5-160">RELATED LINKS</span></span>

[<span data-ttu-id="8bee5-161">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bee5-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="8bee5-162">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bee5-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="8bee5-163">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bee5-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
