---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501730"
---
# <span data-ttu-id="65fcf-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="65fcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="65fcf-103">Erstellt ein lokales Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65fcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fcf-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="65fcf-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="65fcf-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="65fcf-107">Das Cmdlet **New-AzureRmLocalNetworkGateway** erstellt das Objekt, das ihr auf-Prem-Gateway darstellt, basierend auf dem Namen, dem Ressourcengruppennamen, dem Speicherort und der IP-Adresse des Gateways sowie dem Adresspräfix des lokalen Netzwerks, das eine Verbindung zu Azure herstellt.</span><span class="sxs-lookup"><span data-stu-id="65fcf-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="65fcf-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65fcf-108">EXAMPLES</span></span>

### <span data-ttu-id="65fcf-109">1: Erstellen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="65fcf-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="65fcf-110">Erstellt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" an der Position "West US" mit der IP-Adresse "23.99.221.164" und dem Adresspräfix "10.5.51.0/24" auf-Prem.</span><span class="sxs-lookup"><span data-stu-id="65fcf-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="65fcf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="65fcf-111">PARAMETERS</span></span>

### <span data-ttu-id="65fcf-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="65fcf-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="65fcf-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="65fcf-113">-Asn</span></span>
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

### <span data-ttu-id="65fcf-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="65fcf-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="65fcf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="65fcf-115">-Force</span></span>
<span data-ttu-id="65fcf-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="65fcf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65fcf-117">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="65fcf-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="65fcf-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="65fcf-118">-Location</span></span>
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

### <span data-ttu-id="65fcf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="65fcf-119">-Name</span></span>
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

### <span data-ttu-id="65fcf-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="65fcf-120">-PeerWeight</span></span>
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

### <span data-ttu-id="65fcf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fcf-121">-ResourceGroupName</span></span>
<span data-ttu-id="65fcf-122">Gibt die Ressourcengruppe an, zu der das lokale Netzwerkgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="65fcf-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="65fcf-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="65fcf-123">-Tag</span></span>
<span data-ttu-id="65fcf-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="65fcf-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65fcf-125">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="65fcf-125">For example:</span></span>

<span data-ttu-id="65fcf-126">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="65fcf-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="65fcf-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65fcf-127">-Confirm</span></span>
<span data-ttu-id="65fcf-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65fcf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fcf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fcf-129">-WhatIf</span></span>
<span data-ttu-id="65fcf-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65fcf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65fcf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65fcf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fcf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fcf-132">-DefaultProfile</span></span>
<span data-ttu-id="65fcf-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65fcf-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fcf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fcf-134">CommonParameters</span></span>
<span data-ttu-id="65fcf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fcf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fcf-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65fcf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fcf-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65fcf-137">INPUTS</span></span>

## <span data-ttu-id="65fcf-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65fcf-138">OUTPUTS</span></span>

### <span data-ttu-id="65fcf-139">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="65fcf-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="65fcf-140">NOTES</span></span>

## <span data-ttu-id="65fcf-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65fcf-141">RELATED LINKS</span></span>

[<span data-ttu-id="65fcf-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="65fcf-143">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="65fcf-144">Satz-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65fcf-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
