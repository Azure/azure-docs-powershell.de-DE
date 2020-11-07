---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821523"
---
# <span data-ttu-id="13527-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="13527-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="13527-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13527-102">SYNOPSIS</span></span>
<span data-ttu-id="13527-103">Erstellt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="13527-103">Creates a private link service</span></span>

## <span data-ttu-id="13527-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13527-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13527-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13527-105">DESCRIPTION</span></span>
<span data-ttu-id="13527-106">Das Cmdlet " **New-AzPrivateLinkService** " erstellt einen privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="13527-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="13527-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13527-107">EXAMPLES</span></span>

### <span data-ttu-id="13527-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13527-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="13527-109">In diesem Beispiel wird ein privater Link-Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="13527-109">This example creates a private link service.</span></span>

## <span data-ttu-id="13527-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13527-110">PARAMETERS</span></span>

### <span data-ttu-id="13527-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13527-111">-AsJob</span></span>
<span data-ttu-id="13527-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="13527-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13527-113">– Autoapproval</span><span class="sxs-lookup"><span data-stu-id="13527-113">-AutoApproval</span></span>
<span data-ttu-id="13527-114">Die automatischen Genehmigungs Abonnements für den privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="13527-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="13527-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13527-115">-DefaultProfile</span></span>
<span data-ttu-id="13527-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13527-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13527-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13527-117">-Force</span></span>
<span data-ttu-id="13527-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="13527-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="13527-119">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="13527-119">-IpConfiguration</span></span>
<span data-ttu-id="13527-120">Die IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="13527-120">The ip configurations</span></span>

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

### <span data-ttu-id="13527-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="13527-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="13527-122">Die Front-End-IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="13527-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="13527-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="13527-123">-Location</span></span>
<span data-ttu-id="13527-124">Lage.</span><span class="sxs-lookup"><span data-stu-id="13527-124">location.</span></span>

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

### <span data-ttu-id="13527-125">-Name</span><span class="sxs-lookup"><span data-stu-id="13527-125">-Name</span></span>
<span data-ttu-id="13527-126">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="13527-126">The name of the service.</span></span>

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

### <span data-ttu-id="13527-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13527-127">-ResourceGroupName</span></span>
<span data-ttu-id="13527-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13527-128">The resource group name.</span></span>

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

### <span data-ttu-id="13527-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="13527-129">-Tag</span></span>
<span data-ttu-id="13527-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="13527-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="13527-131">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="13527-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="13527-132">– Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="13527-132">-Visibility</span></span>
<span data-ttu-id="13527-133">Die Sichtbarkeits Abonnements für den privaten Link Dienst</span><span class="sxs-lookup"><span data-stu-id="13527-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="13527-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13527-134">-Confirm</span></span>
<span data-ttu-id="13527-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13527-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13527-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13527-136">-WhatIf</span></span>
<span data-ttu-id="13527-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13527-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13527-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13527-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13527-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13527-139">CommonParameters</span></span>
<span data-ttu-id="13527-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13527-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13527-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13527-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13527-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13527-142">INPUTS</span></span>

### <span data-ttu-id="13527-143">System. String</span><span class="sxs-lookup"><span data-stu-id="13527-143">System.String</span></span>

### <span data-ttu-id="13527-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="13527-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="13527-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="13527-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="13527-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13527-146">OUTPUTS</span></span>

### <span data-ttu-id="13527-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="13527-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="13527-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="13527-148">NOTES</span></span>

## <span data-ttu-id="13527-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13527-149">RELATED LINKS</span></span>

[<span data-ttu-id="13527-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="13527-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="13527-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="13527-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="13527-152">Neu – AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="13527-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
