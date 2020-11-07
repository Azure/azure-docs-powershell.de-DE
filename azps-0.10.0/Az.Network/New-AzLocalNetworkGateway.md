---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841323"
---
# <span data-ttu-id="b1f04-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="b1f04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1f04-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f04-103">Erstellt ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="b1f04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1f04-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1f04-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f04-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1f04-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b1f04-107">Das Cmdlet **New-AzLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.</span><span class="sxs-lookup"><span data-stu-id="b1f04-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="b1f04-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1f04-108">EXAMPLES</span></span>

### <span data-ttu-id="b1f04-109">1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="b1f04-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="b1f04-110">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.</span><span class="sxs-lookup"><span data-stu-id="b1f04-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="b1f04-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f04-111">PARAMETERS</span></span>

### <span data-ttu-id="b1f04-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b1f04-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="b1f04-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f04-113">-AsJob</span></span>
<span data-ttu-id="b1f04-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1f04-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1f04-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="b1f04-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f04-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b1f04-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="b1f04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f04-117">-DefaultProfile</span></span>
<span data-ttu-id="b1f04-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1f04-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1f04-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f04-119">-Force</span></span>
<span data-ttu-id="b1f04-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b1f04-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1f04-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1f04-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="b1f04-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="b1f04-122">-Location</span></span>
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

### <span data-ttu-id="b1f04-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f04-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f04-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="b1f04-124">-PeerWeight</span></span>
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

### <span data-ttu-id="b1f04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f04-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1f04-126">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="b1f04-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="b1f04-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1f04-127">-Tag</span></span>
<span data-ttu-id="b1f04-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b1f04-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b1f04-129">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b1f04-129">For example:</span></span>

<span data-ttu-id="b1f04-130">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b1f04-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b1f04-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1f04-131">-Confirm</span></span>
<span data-ttu-id="b1f04-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1f04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f04-133">-WhatIf</span></span>
<span data-ttu-id="b1f04-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1f04-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f04-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1f04-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f04-136">CommonParameters</span></span>
<span data-ttu-id="b1f04-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f04-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f04-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f04-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1f04-139">INPUTS</span></span>

## <span data-ttu-id="b1f04-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1f04-140">OUTPUTS</span></span>

### <span data-ttu-id="b1f04-141">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b1f04-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1f04-142">NOTES</span></span>

## <span data-ttu-id="b1f04-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1f04-143">RELATED LINKS</span></span>

[<span data-ttu-id="b1f04-144">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="b1f04-145">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="b1f04-146">Satz-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f04-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
