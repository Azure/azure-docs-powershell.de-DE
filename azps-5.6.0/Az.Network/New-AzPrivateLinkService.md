---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 9ed82247ff0b1813293059a7608557184bdb18ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921744"
---
# <span data-ttu-id="d8091-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d8091-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="d8091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8091-102">SYNOPSIS</span></span>
<span data-ttu-id="d8091-103">Erstellt einen privaten Linkdienst</span><span class="sxs-lookup"><span data-stu-id="d8091-103">Creates a private link service</span></span>

## <span data-ttu-id="d8091-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8091-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8091-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8091-105">DESCRIPTION</span></span>
<span data-ttu-id="d8091-106">Das **Cmdlet New-AzPrivateLinkService** erstellt einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="d8091-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="d8091-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8091-107">EXAMPLES</span></span>

### <span data-ttu-id="d8091-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8091-108">Example 1</span></span>

<span data-ttu-id="d8091-109">Im folgenden Beispiel wird ein privater Linkdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8091-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="d8091-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8091-110">PARAMETERS</span></span>

### <span data-ttu-id="d8091-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8091-111">-AsJob</span></span>
<span data-ttu-id="d8091-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d8091-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8091-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="d8091-113">-AutoApproval</span></span>
<span data-ttu-id="d8091-114">Die Abonnements für die automatische Genehmigung des privaten Linkdiensts</span><span class="sxs-lookup"><span data-stu-id="d8091-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8091-115">-DefaultProfile</span></span>
<span data-ttu-id="d8091-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8091-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8091-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="d8091-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="d8091-118">Aktivieren des Proxyprotokolls für den privaten Linkdienst</span><span class="sxs-lookup"><span data-stu-id="d8091-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="d8091-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d8091-119">-Force</span></span>
<span data-ttu-id="d8091-120">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d8091-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d8091-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8091-121">-IpConfiguration</span></span>
<span data-ttu-id="d8091-122">Die IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d8091-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8091-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="d8091-124">Die Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d8091-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-125">-Location</span><span class="sxs-lookup"><span data-stu-id="d8091-125">-Location</span></span>
<span data-ttu-id="d8091-126">speicherort.</span><span class="sxs-lookup"><span data-stu-id="d8091-126">location.</span></span>

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

### <span data-ttu-id="d8091-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d8091-127">-Name</span></span>
<span data-ttu-id="d8091-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="d8091-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8091-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8091-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8091-130">The resource group name.</span></span>

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

### <span data-ttu-id="d8091-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8091-131">-Tag</span></span>
<span data-ttu-id="d8091-132">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d8091-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8091-133">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d8091-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d8091-134">-Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="d8091-134">-Visibility</span></span>
<span data-ttu-id="d8091-135">Die Sichtbarkeitsabonnements des privaten Linkdiensts</span><span class="sxs-lookup"><span data-stu-id="d8091-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8091-136">-Confirm</span></span>
<span data-ttu-id="d8091-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8091-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8091-138">-WhatIf</span></span>
<span data-ttu-id="d8091-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8091-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8091-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8091-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8091-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8091-141">CommonParameters</span></span>
<span data-ttu-id="d8091-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8091-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8091-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8091-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8091-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8091-144">INPUTS</span></span>

### <span data-ttu-id="d8091-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d8091-145">System.String</span></span>

### <span data-ttu-id="d8091-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d8091-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="d8091-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d8091-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="d8091-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8091-148">OUTPUTS</span></span>

### <span data-ttu-id="d8091-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d8091-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d8091-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d8091-150">NOTES</span></span>

## <span data-ttu-id="d8091-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d8091-151">RELATED LINKS</span></span>

[<span data-ttu-id="d8091-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d8091-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="d8091-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d8091-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="d8091-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d8091-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
