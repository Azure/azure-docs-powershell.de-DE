---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 15775f23a205257505d812c5f0493f9f7c124c2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499950"
---
# <span data-ttu-id="d8335-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d8335-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8335-102">SYNOPSIS</span></span>
<span data-ttu-id="d8335-103">Erstellt eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="d8335-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8335-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8335-104">SYNTAX</span></span>

### <span data-ttu-id="d8335-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8335-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8335-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d8335-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8335-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8335-107">DESCRIPTION</span></span>
<span data-ttu-id="d8335-108">Das Cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** erstellt eine eingehende NAT-Regelkonfiguration für ein Azure-Lastenausgleichssystem.</span><span class="sxs-lookup"><span data-stu-id="d8335-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d8335-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8335-109">EXAMPLES</span></span>

### <span data-ttu-id="d8335-110">Beispiel 1: Erstellen einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="d8335-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="d8335-111">Der erste Befehl erstellt eine öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d8335-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="d8335-112">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d8335-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="d8335-113">Der dritte Befehl erstellt eine eingehende NAT-Regelkonfiguration mit dem Namen MyInboundNatRule mit dem Front-End-Objekt in $Frontend.</span><span class="sxs-lookup"><span data-stu-id="d8335-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="d8335-114">Das TCP-Protokoll wird angegeben, und der Front-End-Port ist 3389, derselbe wie der Back-End-Port in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="d8335-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="d8335-115">Die *FrontendIpConfiguration* -, *Procotol* -, *FrontendPort* -und *BackendPort* -Parameter sind alle erforderlich, um eine eingehende NAT-Regelkonfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8335-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="d8335-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8335-116">PARAMETERS</span></span>

### <span data-ttu-id="d8335-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d8335-117">-BackendPort</span></span>
<span data-ttu-id="d8335-118">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="d8335-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d8335-119">-EnableFloatingIP</span></span>
<span data-ttu-id="d8335-120">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8335-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d8335-121">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8335-121">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d8335-122">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8335-122">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d8335-123">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d8335-124">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d8335-124">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-125">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d8335-125">-FrontendPort</span></span>
<span data-ttu-id="d8335-126">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="d8335-126">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d8335-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d8335-128">Gibt die Zeitdauer in Minuten an, für die der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="d8335-128">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d8335-129">-Name</span></span>
<span data-ttu-id="d8335-130">Gibt den Namen der Regelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8335-130">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d8335-131">-Protocol</span></span>
<span data-ttu-id="d8335-132">Gibt ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="d8335-132">Specifies a protocol.</span></span>
<span data-ttu-id="d8335-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d8335-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8335-134">TCP</span><span class="sxs-lookup"><span data-stu-id="d8335-134">Tcp</span></span>
- <span data-ttu-id="d8335-135">UDP</span><span class="sxs-lookup"><span data-stu-id="d8335-135">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8335-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8335-136">-DefaultProfile</span></span>
<span data-ttu-id="d8335-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8335-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8335-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8335-138">CommonParameters</span></span>
<span data-ttu-id="d8335-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8335-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8335-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8335-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8335-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8335-141">INPUTS</span></span>

## <span data-ttu-id="d8335-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8335-142">OUTPUTS</span></span>

### <span data-ttu-id="d8335-143">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d8335-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="d8335-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8335-144">NOTES</span></span>

## <span data-ttu-id="d8335-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8335-145">RELATED LINKS</span></span>

[<span data-ttu-id="d8335-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8335-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8335-148">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-148">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d8335-149">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d8335-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d8335-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8335-151">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8335-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


