---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459912"
---
# <span data-ttu-id="c48e3-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c48e3-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="c48e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c48e3-103">Erstellt einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="c48e3-103">Creates a private link service</span></span>

## <span data-ttu-id="c48e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c48e3-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c48e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c48e3-105">DESCRIPTION</span></span>
<span data-ttu-id="c48e3-106">Das **Cmdlet "New-AzPrivateLinkService"** erstellt einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="c48e3-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="c48e3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c48e3-107">EXAMPLES</span></span>

### <span data-ttu-id="c48e3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c48e3-108">Example 1</span></span>

<span data-ttu-id="c48e3-109">Im folgenden Beispiel wird ein privater Linkdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="c48e3-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="c48e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48e3-110">PARAMETERS</span></span>

### <span data-ttu-id="c48e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c48e3-111">-AsJob</span></span>
<span data-ttu-id="c48e3-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c48e3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c48e3-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="c48e3-113">-AutoApproval</span></span>
<span data-ttu-id="c48e3-114">Die automatischen Genehmigungsabonnements des privaten Linkdiensts</span><span class="sxs-lookup"><span data-stu-id="c48e3-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="c48e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48e3-115">-DefaultProfile</span></span>
<span data-ttu-id="c48e3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c48e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48e3-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="c48e3-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="c48e3-118">Aktivieren Sie das Proxyprotokoll für den privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="c48e3-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="c48e3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c48e3-119">-Force</span></span>
<span data-ttu-id="c48e3-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="c48e3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c48e3-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c48e3-121">-IpConfiguration</span></span>
<span data-ttu-id="c48e3-122">Die IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c48e3-122">The ip configurations</span></span>

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

### <span data-ttu-id="c48e3-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c48e3-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="c48e3-124">Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c48e3-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="c48e3-125">-Location</span><span class="sxs-lookup"><span data-stu-id="c48e3-125">-Location</span></span>
<span data-ttu-id="c48e3-126">den Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c48e3-126">location.</span></span>

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

### <span data-ttu-id="c48e3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c48e3-127">-Name</span></span>
<span data-ttu-id="c48e3-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="c48e3-128">The name of the service.</span></span>

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

### <span data-ttu-id="c48e3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48e3-129">-ResourceGroupName</span></span>
<span data-ttu-id="c48e3-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c48e3-130">The resource group name.</span></span>

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

### <span data-ttu-id="c48e3-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c48e3-131">-Tag</span></span>
<span data-ttu-id="c48e3-132">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c48e3-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c48e3-133">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c48e3-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c48e3-134">-Visibility</span><span class="sxs-lookup"><span data-stu-id="c48e3-134">-Visibility</span></span>
<span data-ttu-id="c48e3-135">Die Sichtbarkeitsabonnements des privaten Linkdiensts</span><span class="sxs-lookup"><span data-stu-id="c48e3-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="c48e3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c48e3-136">-Confirm</span></span>
<span data-ttu-id="c48e3-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c48e3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c48e3-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c48e3-138">-WhatIf</span></span>
<span data-ttu-id="c48e3-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c48e3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48e3-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c48e3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c48e3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48e3-141">CommonParameters</span></span>
<span data-ttu-id="c48e3-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48e3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48e3-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48e3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48e3-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c48e3-144">INPUTS</span></span>

### <span data-ttu-id="c48e3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c48e3-145">System.String</span></span>

### <span data-ttu-id="c48e3-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c48e3-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="c48e3-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c48e3-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="c48e3-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c48e3-148">OUTPUTS</span></span>

### <span data-ttu-id="c48e3-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c48e3-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c48e3-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c48e3-150">NOTES</span></span>

## <span data-ttu-id="c48e3-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c48e3-151">RELATED LINKS</span></span>

[<span data-ttu-id="c48e3-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c48e3-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="c48e3-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c48e3-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="c48e3-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c48e3-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
