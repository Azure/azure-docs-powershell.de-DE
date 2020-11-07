---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 6db2d9defaed434aa74f64d6f13af4f029edf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662936"
---
# <span data-ttu-id="545d4-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="545d4-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="545d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="545d4-102">SYNOPSIS</span></span>
<span data-ttu-id="545d4-103">Erstellt ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="545d4-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="545d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="545d4-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="545d4-105">DESCRIPTION</span></span>
<span data-ttu-id="545d4-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="545d4-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="545d4-107">Das Cmdlet **New-AzureRmLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.</span><span class="sxs-lookup"><span data-stu-id="545d4-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="545d4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="545d4-108">EXAMPLES</span></span>

### <span data-ttu-id="545d4-109">1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="545d4-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="545d4-110">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.</span><span class="sxs-lookup"><span data-stu-id="545d4-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="545d4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="545d4-111">PARAMETERS</span></span>

### <span data-ttu-id="545d4-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="545d4-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="545d4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="545d4-113">-AsJob</span></span>
<span data-ttu-id="545d4-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="545d4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="545d4-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="545d4-115">-Asn</span></span>
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

### <span data-ttu-id="545d4-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="545d4-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="545d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545d4-117">-DefaultProfile</span></span>
<span data-ttu-id="545d4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="545d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="545d4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="545d4-119">-Force</span></span>
<span data-ttu-id="545d4-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="545d4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="545d4-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="545d4-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="545d4-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="545d4-122">-Location</span></span>
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

### <span data-ttu-id="545d4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="545d4-123">-Name</span></span>
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

### <span data-ttu-id="545d4-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="545d4-124">-PeerWeight</span></span>
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

### <span data-ttu-id="545d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="545d4-126">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="545d4-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="545d4-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="545d4-127">-Tag</span></span>
<span data-ttu-id="545d4-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="545d4-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="545d4-129">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="545d4-129">For example:</span></span>

<span data-ttu-id="545d4-130">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="545d4-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="545d4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="545d4-131">-Confirm</span></span>
<span data-ttu-id="545d4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="545d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545d4-133">-WhatIf</span></span>
<span data-ttu-id="545d4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="545d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545d4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="545d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545d4-136">CommonParameters</span></span>
<span data-ttu-id="545d4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545d4-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545d4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545d4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="545d4-139">INPUTS</span></span>

### <span data-ttu-id="545d4-140">Keine</span><span class="sxs-lookup"><span data-stu-id="545d4-140">None</span></span>
<span data-ttu-id="545d4-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="545d4-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="545d4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="545d4-142">OUTPUTS</span></span>

### <span data-ttu-id="545d4-143">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="545d4-143">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="545d4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="545d4-144">NOTES</span></span>

## <span data-ttu-id="545d4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="545d4-145">RELATED LINKS</span></span>

[<span data-ttu-id="545d4-146">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="545d4-146">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="545d4-147">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="545d4-147">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="545d4-148">Satz-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="545d4-148">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
