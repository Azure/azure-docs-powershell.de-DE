---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179034"
---
# <span data-ttu-id="eda03-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eda03-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="eda03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eda03-102">SYNOPSIS</span></span>
<span data-ttu-id="eda03-103">Erstellt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="eda03-103">Creates a private link service</span></span>

## <span data-ttu-id="eda03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eda03-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eda03-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eda03-105">DESCRIPTION</span></span>
<span data-ttu-id="eda03-106">Das Cmdlet " **New-AzPrivateLinkService** " erstellt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="eda03-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="eda03-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eda03-107">EXAMPLES</span></span>

### <span data-ttu-id="eda03-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eda03-108">Example 1</span></span>

<span data-ttu-id="eda03-109">Im folgenden Beispiel wird ein privater Link-Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="eda03-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="eda03-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eda03-110">PARAMETERS</span></span>

### <span data-ttu-id="eda03-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eda03-111">-AsJob</span></span>
<span data-ttu-id="eda03-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eda03-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eda03-113">– Autoapproval</span><span class="sxs-lookup"><span data-stu-id="eda03-113">-AutoApproval</span></span>
<span data-ttu-id="eda03-114">Die automatischen Genehmigungs Abonnements für den privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="eda03-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="eda03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda03-115">-DefaultProfile</span></span>
<span data-ttu-id="eda03-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eda03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda03-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="eda03-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="eda03-118">Aktivieren Sie das Proxy Protokoll für den privaten Link Dienst.</span><span class="sxs-lookup"><span data-stu-id="eda03-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="eda03-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eda03-119">-Force</span></span>
<span data-ttu-id="eda03-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="eda03-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eda03-121">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="eda03-121">-IpConfiguration</span></span>
<span data-ttu-id="eda03-122">Die IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="eda03-122">The ip configurations</span></span>

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

### <span data-ttu-id="eda03-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="eda03-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="eda03-124">Die Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="eda03-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="eda03-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="eda03-125">-Location</span></span>
<span data-ttu-id="eda03-126">Lage.</span><span class="sxs-lookup"><span data-stu-id="eda03-126">location.</span></span>

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

### <span data-ttu-id="eda03-127">-Name</span><span class="sxs-lookup"><span data-stu-id="eda03-127">-Name</span></span>
<span data-ttu-id="eda03-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="eda03-128">The name of the service.</span></span>

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

### <span data-ttu-id="eda03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda03-129">-ResourceGroupName</span></span>
<span data-ttu-id="eda03-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eda03-130">The resource group name.</span></span>

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

### <span data-ttu-id="eda03-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="eda03-131">-Tag</span></span>
<span data-ttu-id="eda03-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="eda03-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eda03-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="eda03-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eda03-134">– Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="eda03-134">-Visibility</span></span>
<span data-ttu-id="eda03-135">Die Sichtbarkeits Abonnements für den privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="eda03-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="eda03-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eda03-136">-Confirm</span></span>
<span data-ttu-id="eda03-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eda03-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda03-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda03-138">-WhatIf</span></span>
<span data-ttu-id="eda03-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eda03-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda03-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eda03-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda03-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda03-141">CommonParameters</span></span>
<span data-ttu-id="eda03-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda03-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda03-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eda03-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda03-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eda03-144">INPUTS</span></span>

### <span data-ttu-id="eda03-145">System. String</span><span class="sxs-lookup"><span data-stu-id="eda03-145">System.String</span></span>

### <span data-ttu-id="eda03-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="eda03-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="eda03-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="eda03-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="eda03-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eda03-148">OUTPUTS</span></span>

### <span data-ttu-id="eda03-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eda03-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="eda03-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="eda03-150">NOTES</span></span>

## <span data-ttu-id="eda03-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eda03-151">RELATED LINKS</span></span>

[<span data-ttu-id="eda03-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eda03-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="eda03-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eda03-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="eda03-154">Neu – AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eda03-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
