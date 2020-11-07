---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849607"
---
# <span data-ttu-id="e5a18-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="e5a18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5a18-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a18-103">Erstellt ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5a18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a18-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a18-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5a18-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a18-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5a18-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="e5a18-107">Das Cmdlet **New-AzureRmLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.</span><span class="sxs-lookup"><span data-stu-id="e5a18-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="e5a18-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5a18-108">EXAMPLES</span></span>

### <span data-ttu-id="e5a18-109">1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="e5a18-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="e5a18-110">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.</span><span class="sxs-lookup"><span data-stu-id="e5a18-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="e5a18-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a18-111">PARAMETERS</span></span>

### <span data-ttu-id="e5a18-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e5a18-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="e5a18-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5a18-113">-AsJob</span></span>
<span data-ttu-id="e5a18-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e5a18-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5a18-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="e5a18-115">-Asn</span></span>
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

### <span data-ttu-id="e5a18-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e5a18-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="e5a18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a18-117">-DefaultProfile</span></span>
<span data-ttu-id="e5a18-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5a18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a18-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e5a18-119">-Force</span></span>
<span data-ttu-id="e5a18-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e5a18-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5a18-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="e5a18-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="e5a18-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="e5a18-122">-Location</span></span>
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

### <span data-ttu-id="e5a18-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a18-123">-Name</span></span>
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

### <span data-ttu-id="e5a18-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e5a18-124">-PeerWeight</span></span>
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

### <span data-ttu-id="e5a18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a18-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5a18-126">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="e5a18-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="e5a18-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5a18-127">-Tag</span></span>
<span data-ttu-id="e5a18-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="e5a18-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5a18-129">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e5a18-129">For example:</span></span>

<span data-ttu-id="e5a18-130">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="e5a18-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e5a18-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5a18-131">-Confirm</span></span>
<span data-ttu-id="e5a18-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5a18-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a18-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a18-133">-WhatIf</span></span>
<span data-ttu-id="e5a18-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5a18-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a18-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5a18-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a18-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a18-136">CommonParameters</span></span>
<span data-ttu-id="e5a18-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a18-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a18-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a18-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a18-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5a18-139">INPUTS</span></span>

## <span data-ttu-id="e5a18-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5a18-140">OUTPUTS</span></span>

### <span data-ttu-id="e5a18-141">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e5a18-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5a18-142">NOTES</span></span>

## <span data-ttu-id="e5a18-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5a18-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5a18-144">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e5a18-145">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e5a18-146">Satz-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5a18-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
