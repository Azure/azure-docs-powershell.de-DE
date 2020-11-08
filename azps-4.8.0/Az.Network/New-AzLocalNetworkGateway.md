---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175032"
---
# <span data-ttu-id="72ebd-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="72ebd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="72ebd-103">Erstellt ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="72ebd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ebd-104">SYNTAX</span></span>

### <span data-ttu-id="72ebd-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="72ebd-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ebd-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="72ebd-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72ebd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="72ebd-108">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="72ebd-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="72ebd-109">Das Cmdlet **New-AzLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.</span><span class="sxs-lookup"><span data-stu-id="72ebd-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="72ebd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="72ebd-111">Beispiel 1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="72ebd-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="72ebd-112">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.</span><span class="sxs-lookup"><span data-stu-id="72ebd-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="72ebd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="72ebd-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72ebd-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="72ebd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72ebd-115">-AsJob</span></span>
<span data-ttu-id="72ebd-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="72ebd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72ebd-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="72ebd-117">-Asn</span></span>
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

### <span data-ttu-id="72ebd-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="72ebd-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="72ebd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ebd-119">-DefaultProfile</span></span>
<span data-ttu-id="72ebd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72ebd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72ebd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="72ebd-121">-Force</span></span>
<span data-ttu-id="72ebd-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="72ebd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72ebd-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="72ebd-123">-Fqdn</span></span>
<span data-ttu-id="72ebd-124">FQDN des lokalen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="72ebd-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="72ebd-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="72ebd-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="72ebd-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="72ebd-126">-Location</span></span>
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

### <span data-ttu-id="72ebd-127">-Name</span><span class="sxs-lookup"><span data-stu-id="72ebd-127">-Name</span></span>
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

### <span data-ttu-id="72ebd-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="72ebd-128">-PeerWeight</span></span>
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

### <span data-ttu-id="72ebd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ebd-129">-ResourceGroupName</span></span>
<span data-ttu-id="72ebd-130">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="72ebd-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="72ebd-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="72ebd-131">-Tag</span></span>
<span data-ttu-id="72ebd-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="72ebd-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72ebd-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="72ebd-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72ebd-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72ebd-134">-Confirm</span></span>
<span data-ttu-id="72ebd-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72ebd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ebd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ebd-136">-WhatIf</span></span>
<span data-ttu-id="72ebd-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72ebd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ebd-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72ebd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ebd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ebd-139">CommonParameters</span></span>
<span data-ttu-id="72ebd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ebd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ebd-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72ebd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ebd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72ebd-142">INPUTS</span></span>

### <span data-ttu-id="72ebd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="72ebd-143">System.String</span></span>

### <span data-ttu-id="72ebd-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="72ebd-144">System.String[]</span></span>

### <span data-ttu-id="72ebd-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="72ebd-145">System.UInt32</span></span>

### <span data-ttu-id="72ebd-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="72ebd-146">System.Int32</span></span>

### <span data-ttu-id="72ebd-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="72ebd-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72ebd-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72ebd-148">OUTPUTS</span></span>

### <span data-ttu-id="72ebd-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="72ebd-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="72ebd-150">NOTES</span></span>

## <span data-ttu-id="72ebd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72ebd-151">RELATED LINKS</span></span>

[<span data-ttu-id="72ebd-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="72ebd-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="72ebd-154">Satz-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72ebd-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
