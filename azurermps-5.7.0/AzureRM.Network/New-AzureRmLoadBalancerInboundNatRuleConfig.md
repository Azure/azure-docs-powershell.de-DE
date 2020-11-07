---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 0b974d1d79be82f3c16f1052abe0eecc7fa9ba30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663464"
---
# <span data-ttu-id="4e5d2-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4e5d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5d2-103">Erstellt eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e5d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e5d2-104">SYNTAX</span></span>

### <span data-ttu-id="4e5d2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5d2-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e5d2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e5d2-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e5d2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e5d2-108">Das Cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** erstellt eine eingehende NAT-Regelkonfiguration für ein Azure-Lastenausgleichssystem.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4e5d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e5d2-109">EXAMPLES</span></span>

### <span data-ttu-id="4e5d2-110">Beispiel 1: Erstellen einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="4e5d2-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="4e5d2-111">Der erste Befehl erstellt eine öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="4e5d2-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="4e5d2-113">Der dritte Befehl erstellt eine eingehende NAT-Regelkonfiguration mit dem Namen MyInboundNatRule mit dem Front-End-Objekt in $Frontend.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="4e5d2-114">Das TCP-Protokoll wird angegeben, und der Front-End-Port ist 3389, derselbe wie der Back-End-Port in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="4e5d2-115">Die *FrontendIpConfiguration* -, *Procotol* -, *FrontendPort* -und *BackendPort* -Parameter sind alle erforderlich, um eine eingehende NAT-Regelkonfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="4e5d2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e5d2-116">PARAMETERS</span></span>

### <span data-ttu-id="4e5d2-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4e5d2-117">-BackendPort</span></span>
<span data-ttu-id="4e5d2-118">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5d2-119">-DefaultProfile</span></span>
<span data-ttu-id="4e5d2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e5d2-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4e5d2-121">-EnableFloatingIP</span></span>
<span data-ttu-id="4e5d2-122">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4e5d2-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5d2-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4e5d2-124">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4e5d2-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4e5d2-126">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-126">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4e5d2-127">-FrontendPort</span></span>
<span data-ttu-id="4e5d2-128">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4e5d2-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4e5d2-130">Gibt die Zeitdauer in Minuten an, für die der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4e5d2-131">-Name</span></span>
<span data-ttu-id="4e5d2-132">Gibt den Namen der Regelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4e5d2-133">-Protocol</span></span>
<span data-ttu-id="4e5d2-134">Gibt ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-134">Specifies a protocol.</span></span>
<span data-ttu-id="4e5d2-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e5d2-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e5d2-136">TCP</span><span class="sxs-lookup"><span data-stu-id="4e5d2-136">Tcp</span></span>
- <span data-ttu-id="4e5d2-137">UDP</span><span class="sxs-lookup"><span data-stu-id="4e5d2-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5d2-138">CommonParameters</span></span>
<span data-ttu-id="4e5d2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5d2-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5d2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5d2-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e5d2-141">INPUTS</span></span>

### <span data-ttu-id="4e5d2-142">Keine</span><span class="sxs-lookup"><span data-stu-id="4e5d2-142">None</span></span>
<span data-ttu-id="4e5d2-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e5d2-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e5d2-144">OUTPUTS</span></span>

### <span data-ttu-id="4e5d2-145">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="4e5d2-145">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="4e5d2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e5d2-146">NOTES</span></span>

## <span data-ttu-id="4e5d2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e5d2-147">RELATED LINKS</span></span>

[<span data-ttu-id="4e5d2-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4e5d2-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4e5d2-150">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-150">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4e5d2-151">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4e5d2-151">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="4e5d2-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4e5d2-153">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e5d2-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


