---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151588"
---
# <span data-ttu-id="f1eff-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1eff-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="f1eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1eff-102">SYNOPSIS</span></span>
<span data-ttu-id="f1eff-103">Erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f1eff-103">Creates a public IP address.</span></span>

## <span data-ttu-id="f1eff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1eff-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1eff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1eff-105">DESCRIPTION</span></span>
<span data-ttu-id="f1eff-106">Das **Cmdlet "New-AzPublicIpAddress"** erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f1eff-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="f1eff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1eff-107">EXAMPLES</span></span>

### <span data-ttu-id="f1eff-108">Beispiel 1: Erstellen einer neuen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="f1eff-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="f1eff-109">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f1eff-110">Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da "-AllocationMethod" als "Statisch" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1eff-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f1eff-111">Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugeordnet, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="f1eff-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="f1eff-112">Beispiel 2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN</span><span class="sxs-lookup"><span data-stu-id="f1eff-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="f1eff-113">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1eff-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f1eff-114">Mit dem Parameter "-ReverseFqdn" erstellt Azure einen DNS -PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und führt auf die $customFqdn, die im Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f1eff-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="f1eff-115">Als Voraussetzung sollte für die $customFqdn (z. B. webapp.contoso.com) ein DNS-CNAME-Eintrag (Forward-Lookup) vorhanden sein, der auf $dnsPrefix.$location.cloudapp.azure.com verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="f1eff-116">Beispiel 3: Erstellen einer neuen öffentlichen #A0 mit IpTag</span><span class="sxs-lookup"><span data-stu-id="f1eff-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="f1eff-117">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f1eff-118">Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da "-AllocationMethod" als "Statisch" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1eff-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f1eff-119">Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugeordnet, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="f1eff-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="f1eff-120">Ein Iptag wird verwendet, um die einer Ressource zugeordneten Tags zu spezifisch zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1eff-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="f1eff-121">Iptag kann mithilfe von New-AzPublicIpTag angegeben und als Eingabe über -IpTags übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1eff-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="f1eff-122">Beispiel 4: Erstellen einer neuen öffentlichen IP-Adresse aus einem Präfix</span><span class="sxs-lookup"><span data-stu-id="f1eff-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="f1eff-123">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1eff-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f1eff-124">Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f1eff-125">Dieser Ressource wird sofort eine öffentliche IP-Adresse aus dem angegebenen publicIpPrefix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f1eff-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="f1eff-126">Diese Option wird nur für die SKU "Standard" und "Static" AllocationMethod unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1eff-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="f1eff-127">Beispiel 5: Erstellen einer neuen globalen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="f1eff-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="f1eff-128">Mit diesem Befehl wird eine neue globale öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f1eff-129">Dieser Ressource wird sofort eine globale öffentliche IP-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f1eff-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="f1eff-130">Diese Option wird nur für die SKU "Standard" und "Static" AllocationMethod unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1eff-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="f1eff-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1eff-131">PARAMETERS</span></span>

### <span data-ttu-id="f1eff-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f1eff-132">-AllocationMethod</span></span>
<span data-ttu-id="f1eff-133">Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="f1eff-134">Die zulässigen Werte für diesen Parameter sind: Statisch oder dynamisch.</span><span class="sxs-lookup"><span data-stu-id="f1eff-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="f1eff-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1eff-135">-AsJob</span></span>
<span data-ttu-id="f1eff-136">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1eff-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1eff-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1eff-137">-DefaultProfile</span></span>
<span data-ttu-id="f1eff-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1eff-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1eff-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f1eff-139">-DomainNameLabel</span></span>
<span data-ttu-id="f1eff-140">Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="f1eff-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="f1eff-141">-Force</span><span class="sxs-lookup"><span data-stu-id="f1eff-141">-Force</span></span>
<span data-ttu-id="f1eff-142">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="f1eff-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1eff-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f1eff-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f1eff-144">Gibt die Leerlaufzeit in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="f1eff-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="f1eff-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f1eff-145">-IpAddressVersion</span></span>
<span data-ttu-id="f1eff-146">Gibt die Version der IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="f1eff-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="f1eff-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="f1eff-147">-IpTag</span></span>
<span data-ttu-id="f1eff-148">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="f1eff-148">IpTag List.</span></span>

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

### <span data-ttu-id="f1eff-149">-Location</span><span class="sxs-lookup"><span data-stu-id="f1eff-149">-Location</span></span>
<span data-ttu-id="f1eff-150">Gibt die Region an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f1eff-151">-Name</span><span class="sxs-lookup"><span data-stu-id="f1eff-151">-Name</span></span>
<span data-ttu-id="f1eff-152">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1eff-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f1eff-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1eff-153">-PublicIpPrefix</span></span>
<span data-ttu-id="f1eff-154">Gibt den PSPublicIpPrefix an, dem die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="f1eff-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1eff-155">-ResourceGroupName</span></span>
<span data-ttu-id="f1eff-156">Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1eff-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f1eff-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="f1eff-157">-ReverseFqdn</span></span>
<span data-ttu-id="f1eff-158">Gibt einen umgekehrten vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) an.</span><span class="sxs-lookup"><span data-stu-id="f1eff-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="f1eff-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="f1eff-159">-Sku</span></span>
<span data-ttu-id="f1eff-160">Der öffentliche IP-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="f1eff-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="f1eff-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1eff-161">-Tag</span></span>
<span data-ttu-id="f1eff-162">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f1eff-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f1eff-163">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f1eff-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f1eff-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="f1eff-164">-Tier</span></span>
<span data-ttu-id="f1eff-165">Die öffentliche IP-SKU-Stufe.</span><span class="sxs-lookup"><span data-stu-id="f1eff-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1eff-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="f1eff-166">-Zone</span></span>
<span data-ttu-id="f1eff-167">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="f1eff-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f1eff-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1eff-168">-Confirm</span></span>
<span data-ttu-id="f1eff-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1eff-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1eff-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1eff-170">-WhatIf</span></span>
<span data-ttu-id="f1eff-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1eff-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1eff-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1eff-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1eff-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1eff-173">CommonParameters</span></span>
<span data-ttu-id="f1eff-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1eff-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1eff-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1eff-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1eff-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1eff-176">INPUTS</span></span>

### <span data-ttu-id="f1eff-177">System.String</span><span class="sxs-lookup"><span data-stu-id="f1eff-177">System.String</span></span>

### <span data-ttu-id="f1eff-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="f1eff-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="f1eff-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1eff-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="f1eff-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f1eff-180">System.Int32</span></span>

### <span data-ttu-id="f1eff-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f1eff-181">System.String[]</span></span>

### <span data-ttu-id="f1eff-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1eff-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1eff-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1eff-183">OUTPUTS</span></span>

### <span data-ttu-id="f1eff-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1eff-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f1eff-185">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1eff-185">NOTES</span></span>

## <span data-ttu-id="f1eff-186">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1eff-186">RELATED LINKS</span></span>

[<span data-ttu-id="f1eff-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1eff-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="f1eff-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1eff-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="f1eff-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1eff-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
