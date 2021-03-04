---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921728"
---
# <span data-ttu-id="11fc6-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11fc6-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="11fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="11fc6-103">Erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="11fc6-103">Creates a public IP address.</span></span>

## <span data-ttu-id="11fc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11fc6-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11fc6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="11fc6-106">Das **Cmdlet New-AzPublicIpAddress** erstellt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="11fc6-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="11fc6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="11fc6-108">Beispiel 1: Erstellen einer neuen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="11fc6-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="11fc6-109">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="11fc6-110">Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da das -AllocationMethod als "Statisch" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11fc6-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="11fc6-111">Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="11fc6-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="11fc6-112">Beispiel 2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN</span><span class="sxs-lookup"><span data-stu-id="11fc6-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="11fc6-113">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="11fc6-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="11fc6-114">Mit dem -ReverseFqdn-Parameter erstellt Azure einen DNS-PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und gibt auf die im Befehl angegebene $customFqdn an.</span><span class="sxs-lookup"><span data-stu-id="11fc6-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="11fc6-115">Als Voraussetzung sollte der $customFqdn (z. B. webapp.contoso.com) einen DNS-CNAME-Eintrag (Forward-Lookup) haben, der auf $dnsPrefix.$location.cloudapp.azure.com hindeutet.</span><span class="sxs-lookup"><span data-stu-id="11fc6-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="11fc6-116">Beispiel 3: Erstellen einer neuen öffentlichen #A0 mit IpTag</span><span class="sxs-lookup"><span data-stu-id="11fc6-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="11fc6-117">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="11fc6-118">Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da das -AllocationMethod als "Statisch" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11fc6-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="11fc6-119">Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugewiesen, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen).</span><span class="sxs-lookup"><span data-stu-id="11fc6-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="11fc6-120">Ein Iptag wird verwendet, um die mit der Ressource verknüpften Tags zu spezifisch zu versehen.</span><span class="sxs-lookup"><span data-stu-id="11fc6-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="11fc6-121">Iptag kann mithilfe von -New-AzPublicIpTag angegeben und als Eingabe über -IpTags übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="11fc6-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="11fc6-122">Beispiel 4: Erstellen einer neuen öffentlichen IP-Adresse aus einem Präfix</span><span class="sxs-lookup"><span data-stu-id="11fc6-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="11fc6-123">Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="11fc6-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="11fc6-124">Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="11fc6-125">Dieser Ressource wird sofort eine öffentliche IP-Adresse aus dem angegebenen publicIpPrefix zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="11fc6-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="11fc6-126">Diese Option wird nur für die Sku "Standard" und "Static" AllocationMethod unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11fc6-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="11fc6-127">Beispiel 5: Erstellen einer neuen globalen öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="11fc6-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="11fc6-128">Mit diesem Befehl wird eine neue globale öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="11fc6-129">Dieser Ressource wird sofort eine globale öffentliche IP-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="11fc6-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="11fc6-130">Diese Option wird nur für die Sku "Standard" und "Static" AllocationMethod unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11fc6-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="11fc6-131">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="11fc6-131">PARAMETERS</span></span>

### <span data-ttu-id="11fc6-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="11fc6-132">-AllocationMethod</span></span>
<span data-ttu-id="11fc6-133">Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="11fc6-134">Die zulässigen Werte für diesen Parameter sind: Statisch oder Dynamisch.</span><span class="sxs-lookup"><span data-stu-id="11fc6-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="11fc6-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11fc6-135">-AsJob</span></span>
<span data-ttu-id="11fc6-136">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="11fc6-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11fc6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fc6-137">-DefaultProfile</span></span>
<span data-ttu-id="11fc6-138">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11fc6-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11fc6-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="11fc6-139">-DomainNameLabel</span></span>
<span data-ttu-id="11fc6-140">Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="11fc6-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="11fc6-141">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="11fc6-141">-Force</span></span>
<span data-ttu-id="11fc6-142">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="11fc6-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11fc6-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="11fc6-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="11fc6-144">Gibt die Leerlaufzeit in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="11fc6-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="11fc6-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="11fc6-145">-IpAddressVersion</span></span>
<span data-ttu-id="11fc6-146">Gibt die Version der IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="11fc6-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="11fc6-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="11fc6-147">-IpTag</span></span>
<span data-ttu-id="11fc6-148">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="11fc6-148">IpTag List.</span></span>

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

### <span data-ttu-id="11fc6-149">-Location</span><span class="sxs-lookup"><span data-stu-id="11fc6-149">-Location</span></span>
<span data-ttu-id="11fc6-150">Gibt den Bereich an, in dem eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="11fc6-151">-Name</span><span class="sxs-lookup"><span data-stu-id="11fc6-151">-Name</span></span>
<span data-ttu-id="11fc6-152">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="11fc6-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11fc6-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11fc6-153">-PublicIpPrefix</span></span>
<span data-ttu-id="11fc6-154">Gibt das PSPublicIpPrefix an, aus dem die öffentliche IP-Adresse zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="11fc6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fc6-155">-ResourceGroupName</span></span>
<span data-ttu-id="11fc6-156">Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11fc6-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="11fc6-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="11fc6-157">-ReverseFqdn</span></span>
<span data-ttu-id="11fc6-158">Gibt einen umgekehrten vollqualifizierten Domänennamen (FQDN) an.</span><span class="sxs-lookup"><span data-stu-id="11fc6-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="11fc6-159">-Sku</span><span class="sxs-lookup"><span data-stu-id="11fc6-159">-Sku</span></span>
<span data-ttu-id="11fc6-160">Der name der öffentlichen IP-Sku.</span><span class="sxs-lookup"><span data-stu-id="11fc6-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="11fc6-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="11fc6-161">-Tag</span></span>
<span data-ttu-id="11fc6-162">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="11fc6-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11fc6-163">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="11fc6-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="11fc6-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="11fc6-164">-Tier</span></span>
<span data-ttu-id="11fc6-165">Die öffentliche IP-Sku-Ebene.</span><span class="sxs-lookup"><span data-stu-id="11fc6-165">The public IP Sku Tier.</span></span>

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

### <span data-ttu-id="11fc6-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="11fc6-166">-Zone</span></span>
<span data-ttu-id="11fc6-167">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugewiesene IP bezeichnet wird, muss von stammen.</span><span class="sxs-lookup"><span data-stu-id="11fc6-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="11fc6-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11fc6-168">-Confirm</span></span>
<span data-ttu-id="11fc6-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11fc6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11fc6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11fc6-170">-WhatIf</span></span>
<span data-ttu-id="11fc6-171">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11fc6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11fc6-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11fc6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11fc6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fc6-173">CommonParameters</span></span>
<span data-ttu-id="11fc6-174">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11fc6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fc6-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11fc6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fc6-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11fc6-176">INPUTS</span></span>

### <span data-ttu-id="11fc6-177">System.String</span><span class="sxs-lookup"><span data-stu-id="11fc6-177">System.String</span></span>

### <span data-ttu-id="11fc6-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="11fc6-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="11fc6-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11fc6-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="11fc6-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="11fc6-180">System.Int32</span></span>

### <span data-ttu-id="11fc6-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="11fc6-181">System.String[]</span></span>

### <span data-ttu-id="11fc6-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="11fc6-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11fc6-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11fc6-183">OUTPUTS</span></span>

### <span data-ttu-id="11fc6-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11fc6-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="11fc6-185">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="11fc6-185">NOTES</span></span>

## <span data-ttu-id="11fc6-186">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="11fc6-186">RELATED LINKS</span></span>

[<span data-ttu-id="11fc6-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11fc6-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="11fc6-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11fc6-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="11fc6-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="11fc6-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
