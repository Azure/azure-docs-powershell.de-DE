---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469003"
---
# <span data-ttu-id="5ad58-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="5ad58-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="5ad58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad58-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad58-103">Erstellen einer neuen Nat-Regel für die Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="5ad58-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="5ad58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ad58-104">SYNTAX</span></span>

### <span data-ttu-id="5ad58-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="5ad58-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad58-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="5ad58-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad58-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="5ad58-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad58-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="5ad58-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ad58-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ad58-109">DESCRIPTION</span></span>
<span data-ttu-id="5ad58-110">Das **Cmdlet "New-AzFirewallPolicyNatRule"** erstellt eine NAT-Regel für eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5ad58-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5ad58-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ad58-111">EXAMPLES</span></span>

### <span data-ttu-id="5ad58-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ad58-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="5ad58-113">In diesem Beispiel wird eine NAT-Regel mit der Quelladresse, dem Protokoll, der Zieladresse, dem Zielport, der übersetzten Adresse und dem übersetzten Port erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ad58-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="5ad58-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5ad58-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="5ad58-115">In diesem Beispiel wird eine NAT-Regel mit der Quelladresse, dem Protokoll, der Zieladresse, dem Zielport, dem übersetzten fqdn und dem übersetzten Port erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ad58-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="5ad58-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ad58-116">PARAMETERS</span></span>

### <span data-ttu-id="5ad58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad58-117">-DefaultProfile</span></span>
<span data-ttu-id="5ad58-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad58-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ad58-119">-Description</span></span>
<span data-ttu-id="5ad58-120">Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-120">The description of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5ad58-121">-DestinationAddress</span></span>
<span data-ttu-id="5ad58-122">Die Zieladressen der Regel.</span><span class="sxs-lookup"><span data-stu-id="5ad58-122">The destination addresses of the rule.</span></span> <span data-ttu-id="5ad58-123">Dies muss eine öffentliche IP der Firewall sein.</span><span class="sxs-lookup"><span data-stu-id="5ad58-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5ad58-124">-DestinationPort</span></span>
<span data-ttu-id="5ad58-125">Die Zielports der Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5ad58-126">-Name</span></span>
<span data-ttu-id="5ad58-127">Der Name der NAT Rule Collection</span><span class="sxs-lookup"><span data-stu-id="5ad58-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="5ad58-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5ad58-128">-Protocol</span></span>
<span data-ttu-id="5ad58-129">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5ad58-130">-SourceAddress</span></span>
<span data-ttu-id="5ad58-131">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="5ad58-132">-SourceIpGroup</span></span>
<span data-ttu-id="5ad58-133">Die Quell-IP-Gruppen der Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="5ad58-134">-TranslatedAddress</span></span>
<span data-ttu-id="5ad58-135">Die übersetzte Adresse für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="5ad58-136">-TranslatedFqdn</span></span>
<span data-ttu-id="5ad58-137">Der übersetzte FQDN für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad58-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="5ad58-138">-TranslatedPort</span></span>
<span data-ttu-id="5ad58-139">Der übersetzte Port für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="5ad58-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="5ad58-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad58-140">CommonParameters</span></span>
<span data-ttu-id="5ad58-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad58-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad58-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ad58-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad58-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad58-143">INPUTS</span></span>

### <span data-ttu-id="5ad58-144">Keine</span><span class="sxs-lookup"><span data-stu-id="5ad58-144">None</span></span>

## <span data-ttu-id="5ad58-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad58-145">OUTPUTS</span></span>

### <span data-ttu-id="5ad58-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="5ad58-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="5ad58-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ad58-147">NOTES</span></span>

## <span data-ttu-id="5ad58-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ad58-148">RELATED LINKS</span></span>
