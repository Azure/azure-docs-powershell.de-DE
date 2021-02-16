---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160876"
---
# <span data-ttu-id="2b169-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b169-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="2b169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b169-102">SYNOPSIS</span></span>
<span data-ttu-id="2b169-103">Erstellt ein lokales Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="2b169-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="2b169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b169-104">SYNTAX</span></span>

### <span data-ttu-id="2b169-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b169-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b169-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="2b169-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b169-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b169-107">DESCRIPTION</span></span>
<span data-ttu-id="2b169-108">Das lokale Netzwerkgateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b169-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="2b169-109">Das **Cmdlet "New-AzLocalNetworkGateway"** erstellt das Objekt, das Ihr lokales Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Standort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung mit Azure herstellen wird.</span><span class="sxs-lookup"><span data-stu-id="2b169-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="2b169-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b169-110">EXAMPLES</span></span>

### <span data-ttu-id="2b169-111">Beispiel 1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="2b169-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="2b169-112">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" am Standort "WEST US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" lokal.</span><span class="sxs-lookup"><span data-stu-id="2b169-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="2b169-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b169-113">PARAMETERS</span></span>

### <span data-ttu-id="2b169-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b169-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="2b169-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b169-115">-AsJob</span></span>
<span data-ttu-id="2b169-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2b169-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b169-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="2b169-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b169-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2b169-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="2b169-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b169-119">-DefaultProfile</span></span>
<span data-ttu-id="2b169-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b169-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b169-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2b169-121">-Force</span></span>
<span data-ttu-id="2b169-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="2b169-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b169-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="2b169-123">-Fqdn</span></span>
<span data-ttu-id="2b169-124">FQDN des lokalen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="2b169-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b169-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b169-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b169-126">-Location</span><span class="sxs-lookup"><span data-stu-id="2b169-126">-Location</span></span>
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

### <span data-ttu-id="2b169-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2b169-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b169-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2b169-128">-PeerWeight</span></span>
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

### <span data-ttu-id="2b169-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b169-129">-ResourceGroupName</span></span>
<span data-ttu-id="2b169-130">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="2b169-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="2b169-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b169-131">-Tag</span></span>
<span data-ttu-id="2b169-132">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2b169-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b169-133">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2b169-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b169-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b169-134">-Confirm</span></span>
<span data-ttu-id="2b169-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b169-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b169-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2b169-136">-WhatIf</span></span>
<span data-ttu-id="2b169-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b169-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b169-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b169-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b169-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b169-139">CommonParameters</span></span>
<span data-ttu-id="2b169-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b169-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b169-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b169-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b169-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b169-142">INPUTS</span></span>

### <span data-ttu-id="2b169-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2b169-143">System.String</span></span>

### <span data-ttu-id="2b169-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2b169-144">System.String[]</span></span>

### <span data-ttu-id="2b169-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2b169-145">System.UInt32</span></span>

### <span data-ttu-id="2b169-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2b169-146">System.Int32</span></span>

### <span data-ttu-id="2b169-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b169-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2b169-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b169-148">OUTPUTS</span></span>

### <span data-ttu-id="2b169-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b169-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="2b169-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2b169-150">NOTES</span></span>

## <span data-ttu-id="2b169-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2b169-151">RELATED LINKS</span></span>

[<span data-ttu-id="2b169-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b169-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="2b169-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b169-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="2b169-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b169-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
