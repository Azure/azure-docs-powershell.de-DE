---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005930"
---
# <span data-ttu-id="b18d6-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b18d6-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="b18d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b18d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b18d6-103">Fügt einem Azure-Dienst ein internes Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="b18d6-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="b18d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b18d6-104">SYNTAX</span></span>

### <span data-ttu-id="b18d6-105">ServiceAndSlot (Standard)</span><span class="sxs-lookup"><span data-stu-id="b18d6-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b18d6-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="b18d6-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b18d6-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="b18d6-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b18d6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b18d6-108">DESCRIPTION</span></span>
<span data-ttu-id="b18d6-109">Das Cmdlet **Add-AzureInternalLoadBalancer** fügt einem Azure-Dienst eine interne Load Balancer-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="b18d6-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="b18d6-110">Bei einem virtuellen Netzwerk können Sie ein Subnetz oder die IP-Adresse des internen Load Balancer angeben.</span><span class="sxs-lookup"><span data-stu-id="b18d6-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="b18d6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b18d6-111">EXAMPLES</span></span>

### <span data-ttu-id="b18d6-112">Beispiel 1: Hinzufügen eines internen Load Balancer</span><span class="sxs-lookup"><span data-stu-id="b18d6-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="b18d6-113">Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.</span><span class="sxs-lookup"><span data-stu-id="b18d6-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="b18d6-114">Beispiel 2: Hinzufügen eines internen Lastenausgleichs für ein angegebenes Subnetz</span><span class="sxs-lookup"><span data-stu-id="b18d6-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="b18d6-115">Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.</span><span class="sxs-lookup"><span data-stu-id="b18d6-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="b18d6-116">Der Befehl gibt das Subnetz mit dem Namen FrontEndSubnet an.</span><span class="sxs-lookup"><span data-stu-id="b18d6-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="b18d6-117">Beispiel 3: Hinzufügen eines internen Lastenausgleichs für ein angegebenes Subnetz und eine Adresse</span><span class="sxs-lookup"><span data-stu-id="b18d6-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="b18d6-118">Dieser Befehl fügt dem Dienst mit dem Namen ContosoWebsite01 ein internes Lastenausgleichsmodul mit dem Namen "ContosoILB" hinzu.</span><span class="sxs-lookup"><span data-stu-id="b18d6-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="b18d6-119">Der Befehl gibt das Subnetz mit dem Namen FrontEndSubnet und die statische Adresse des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="b18d6-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="b18d6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b18d6-120">PARAMETERS</span></span>

### <span data-ttu-id="b18d6-121">-Information</span><span class="sxs-lookup"><span data-stu-id="b18d6-121">-InformationAction</span></span>
<span data-ttu-id="b18d6-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b18d6-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b18d6-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b18d6-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b18d6-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b18d6-124">Continue</span></span>
- <span data-ttu-id="b18d6-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b18d6-125">Ignore</span></span>
- <span data-ttu-id="b18d6-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b18d6-126">Inquire</span></span>
- <span data-ttu-id="b18d6-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b18d6-127">SilentlyContinue</span></span>
- <span data-ttu-id="b18d6-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="b18d6-128">Stop</span></span>
- <span data-ttu-id="b18d6-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b18d6-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b18d6-130">-InformationVariable</span></span>
<span data-ttu-id="b18d6-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b18d6-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b18d6-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="b18d6-133">Gibt den Namen des internen Lastenausgleichs an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b18d6-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="b18d6-134">-Profile</span></span>
<span data-ttu-id="b18d6-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b18d6-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b18d6-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b18d6-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b18d6-137">-ServiceName</span></span>
<span data-ttu-id="b18d6-138">Gibt den Namen des Diensts an, dem dieses Cmdlet ein internes Lastenausgleichsmodul hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b18d6-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="b18d6-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="b18d6-140">Gibt die IP-Adresse des virtuellen Netzwerks für ein internes Lastenausgleichsmodul an, das dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b18d6-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b18d6-141">-SubnetName</span></span>
<span data-ttu-id="b18d6-142">Gibt den Namen des Subnets für ein internes Lastenausgleichsmodul an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b18d6-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b18d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18d6-143">CommonParameters</span></span>
<span data-ttu-id="b18d6-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b18d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18d6-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18d6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18d6-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b18d6-146">INPUTS</span></span>

## <span data-ttu-id="b18d6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b18d6-147">OUTPUTS</span></span>

### <span data-ttu-id="b18d6-148">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b18d6-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="b18d6-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b18d6-149">NOTES</span></span>

## <span data-ttu-id="b18d6-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b18d6-150">RELATED LINKS</span></span>

[<span data-ttu-id="b18d6-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b18d6-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="b18d6-152">Neu – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="b18d6-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="b18d6-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b18d6-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="b18d6-154">Satz-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b18d6-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


