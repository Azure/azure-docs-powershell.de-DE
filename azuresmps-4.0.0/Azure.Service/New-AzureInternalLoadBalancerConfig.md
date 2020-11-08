---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006120"
---
# <span data-ttu-id="8ac9a-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="8ac9a-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="8ac9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ac9a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac9a-103">Erstellt eine interne Load Balancer-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="8ac9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac9a-104">SYNTAX</span></span>

### <span data-ttu-id="8ac9a-105">ServiceAndSlot (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ac9a-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8ac9a-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="8ac9a-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac9a-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="8ac9a-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ac9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ac9a-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac9a-109">Mit dem Cmdlet **New-AzureInternalLoadBalancerConfig** wird ein **InternalLoadBalancerConfig** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="8ac9a-110">Wenn Sie eine Azure Virtual Machine-Bereitstellung erstellen, können Sie eine interne Load Balancer-Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="8ac9a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ac9a-111">EXAMPLES</span></span>

### <span data-ttu-id="8ac9a-112">Beispiel 1: Erstellen einer internen Load Balancer-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8ac9a-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="8ac9a-113">Dieser Befehl erstellt eine interne Load Balancer-Konfiguration für das Subnetz mit dem Namen FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="8ac9a-114">Der Befehl speichert die Konfiguration in der $IlbConfig Variablen, die Sie für die Bereitstellung virtueller Computer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="8ac9a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac9a-115">PARAMETERS</span></span>

### <span data-ttu-id="8ac9a-116">-Information</span><span class="sxs-lookup"><span data-stu-id="8ac9a-116">-InformationAction</span></span>
<span data-ttu-id="8ac9a-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ac9a-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8ac9a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ac9a-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8ac9a-119">Continue</span></span>
- <span data-ttu-id="8ac9a-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8ac9a-120">Ignore</span></span>
- <span data-ttu-id="8ac9a-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8ac9a-121">Inquire</span></span>
- <span data-ttu-id="8ac9a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ac9a-122">SilentlyContinue</span></span>
- <span data-ttu-id="8ac9a-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="8ac9a-123">Stop</span></span>
- <span data-ttu-id="8ac9a-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8ac9a-124">Suspend</span></span>

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

### <span data-ttu-id="8ac9a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ac9a-125">-InformationVariable</span></span>
<span data-ttu-id="8ac9a-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8ac9a-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="8ac9a-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="8ac9a-128">Gibt den Namen des internen Lastenausgleichs an, den dieses Cmdlet in die Konfiguration einschließt.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="8ac9a-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="8ac9a-129">-Profile</span></span>
<span data-ttu-id="8ac9a-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ac9a-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ac9a-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="8ac9a-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="8ac9a-133">Gibt die IP-Adresse des virtuellen Netzwerks für ein internes Lastenausgleichsmodul an, das dieses Cmdlet in die Konfiguration einschließt.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac9a-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8ac9a-134">-SubnetName</span></span>
<span data-ttu-id="8ac9a-135">Gibt den Namen des Subnets für ein internes Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac9a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac9a-136">CommonParameters</span></span>
<span data-ttu-id="8ac9a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac9a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac9a-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac9a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac9a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ac9a-139">INPUTS</span></span>

## <span data-ttu-id="8ac9a-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ac9a-140">OUTPUTS</span></span>

### <span data-ttu-id="8ac9a-141">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="8ac9a-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="8ac9a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ac9a-142">NOTES</span></span>

## <span data-ttu-id="8ac9a-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ac9a-143">RELATED LINKS</span></span>

[<span data-ttu-id="8ac9a-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ac9a-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="8ac9a-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ac9a-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="8ac9a-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ac9a-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="8ac9a-147">Satz-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ac9a-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


