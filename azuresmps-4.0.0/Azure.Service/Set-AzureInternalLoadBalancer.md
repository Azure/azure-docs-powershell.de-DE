---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006160"
---
# <span data-ttu-id="1a865-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a865-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="1a865-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a865-102">SYNOPSIS</span></span>
<span data-ttu-id="1a865-103">Ändert eine interne Load Balancer-Konfiguration in einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1a865-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="1a865-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a865-104">SYNTAX</span></span>

### <span data-ttu-id="1a865-105">ServiceAndSlot (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a865-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a865-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="1a865-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a865-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="1a865-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a865-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a865-108">DESCRIPTION</span></span>
<span data-ttu-id="1a865-109">Das Cmdlet " **Satz-AzureInternalLoadBalancer** " ändert eine interne Load Balancer-Konfiguration in einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1a865-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="1a865-110">Bei einem virtuellen Netzwerk können Sie ein Subnetz oder die IP-Adresse des internen Load Balancer angeben.</span><span class="sxs-lookup"><span data-stu-id="1a865-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="1a865-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a865-111">EXAMPLES</span></span>

### <span data-ttu-id="1a865-112">1:</span><span class="sxs-lookup"><span data-stu-id="1a865-112">1:</span></span>
```

```

## <span data-ttu-id="1a865-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a865-113">PARAMETERS</span></span>

### <span data-ttu-id="1a865-114">-Information</span><span class="sxs-lookup"><span data-stu-id="1a865-114">-InformationAction</span></span>
<span data-ttu-id="1a865-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1a865-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1a865-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1a865-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a865-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1a865-117">Continue</span></span>
- <span data-ttu-id="1a865-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1a865-118">Ignore</span></span>
- <span data-ttu-id="1a865-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1a865-119">Inquire</span></span>
- <span data-ttu-id="1a865-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1a865-120">SilentlyContinue</span></span>
- <span data-ttu-id="1a865-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="1a865-121">Stop</span></span>
- <span data-ttu-id="1a865-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1a865-122">Suspend</span></span>

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

### <span data-ttu-id="1a865-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1a865-123">-InformationVariable</span></span>
<span data-ttu-id="1a865-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1a865-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1a865-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="1a865-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="1a865-126">Gibt den Namen des internen Lastenausgleichs an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="1a865-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1a865-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a865-127">-Profile</span></span>
<span data-ttu-id="1a865-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1a865-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a865-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1a865-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a865-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1a865-130">-ServiceName</span></span>
<span data-ttu-id="1a865-131">Gibt den Namen des Diensts an, in dem mit diesem Cmdlet ein interner Lastenausgleichsmechanismus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1a865-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

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

### <span data-ttu-id="1a865-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="1a865-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="1a865-133">Gibt die IP-Adresse des virtuellen Netzwerks für ein internes Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="1a865-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

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

### <span data-ttu-id="1a865-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1a865-134">-SubnetName</span></span>
<span data-ttu-id="1a865-135">Gibt den Namen des Subnets für ein internes Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="1a865-135">Specifies the name of the subnet for an internal load balancer.</span></span>

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

### <span data-ttu-id="1a865-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a865-136">CommonParameters</span></span>
<span data-ttu-id="1a865-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a865-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a865-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a865-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a865-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a865-139">INPUTS</span></span>

## <span data-ttu-id="1a865-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a865-140">OUTPUTS</span></span>

## <span data-ttu-id="1a865-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a865-141">NOTES</span></span>

## <span data-ttu-id="1a865-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a865-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a865-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a865-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="1a865-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a865-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="1a865-145">Neu – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="1a865-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="1a865-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a865-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


