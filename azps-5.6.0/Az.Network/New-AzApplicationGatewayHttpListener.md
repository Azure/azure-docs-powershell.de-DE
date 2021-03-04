---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942155"
---
# <span data-ttu-id="b09e3-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b09e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b09e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b09e3-103">Erstellt einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b09e3-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="b09e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b09e3-104">SYNTAX</span></span>

### <span data-ttu-id="b09e3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b09e3-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b09e3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b09e3-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b09e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b09e3-107">DESCRIPTION</span></span>
<span data-ttu-id="b09e3-108">Das **Cmdlet New-AzApplicationGatewayHttpListener** erstellt einen HTTP-Listener für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b09e3-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b09e3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b09e3-109">EXAMPLES</span></span>

### <span data-ttu-id="b09e3-110">Beispiel 1: Erstellen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="b09e3-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="b09e3-111">Mit diesem Befehl wird ein HTTP-Listener namens Listener01 erstellt und das Ergebnis in der Variablen namens $Listener.</span><span class="sxs-lookup"><span data-stu-id="b09e3-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b09e3-112">Beispiel 2: Erstellen eines HTTP-Listeners mit SSL</span><span class="sxs-lookup"><span data-stu-id="b09e3-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b09e3-113">Mit diesem Befehl wird ein HTTP-Listener erstellt, der SSL-Offload verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="b09e3-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="b09e3-114">Der Befehl speichert das Ergebnis in der Variablen namens $Listener.</span><span class="sxs-lookup"><span data-stu-id="b09e3-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b09e3-115">Beispiel 3: Erstellen eines HTTP-Listeners mit Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b09e3-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="b09e3-116">Mit diesem Befehl wird ein HTTP-Listener namens Listener01, FirewallPolicy als $firewallPolicy erstellt und das Ergebnis in der Variablen namens $Listener.</span><span class="sxs-lookup"><span data-stu-id="b09e3-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b09e3-117">Beispiel 4: Hinzufügen eines HTTPS-Listeners mit SSL und HostNamen</span><span class="sxs-lookup"><span data-stu-id="b09e3-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="b09e3-118">Mit diesem Befehl wird ein HTTP-Listener erstellt, der SSL-Offload verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable zusammen mit zwei Hostnamen zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="b09e3-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="b09e3-119">Der Befehl speichert das Ergebnis in der Variablen namens $Listener.</span><span class="sxs-lookup"><span data-stu-id="b09e3-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="b09e3-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b09e3-120">PARAMETERS</span></span>

### <span data-ttu-id="b09e3-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b09e3-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b09e3-122">Kundenfehler eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="b09e3-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09e3-123">-DefaultProfile</span></span>
<span data-ttu-id="b09e3-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b09e3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b09e3-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b09e3-125">-FirewallPolicy</span></span>
<span data-ttu-id="b09e3-126">Gibt den Objektverweis auf eine Firewallrichtlinie der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="b09e3-127">Der Objektverweis kann mithilfe des cmdlets New-AzApplicationGatewayWebApplicationFirewallPolicy werden.</span><span class="sxs-lookup"><span data-stu-id="b09e3-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="b09e3-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Eine Firewallrichtlinie, die mit dem obigen Befehllet erstellt wurde, kann auf pfadregelebene verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b09e3-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="b09e3-129">Der obige Befehl würde eine Standardrichtlinieneinstellungen und verwaltete Regeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="b09e3-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="b09e3-130">Anstelle der Standardwerte können Benutzer "PolicySettings", "ManagedRules" New-AzApplicationGatewayFirewallPolicySettings und New-AzApplicationGatewayFirewallPolicyManagedRules angeben.</span><span class="sxs-lookup"><span data-stu-id="b09e3-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b09e3-131">-FirewallPolicyId</span></span>
<span data-ttu-id="b09e3-132">Gibt die ID einer vorhandenen Webanwendungsfirewallressource der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="b09e3-133">Firewallrichtlinien-IDs können über das cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b09e3-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="b09e3-134">Nachdem wir die ID haben, können Sie den *Parameter FirewallPolicyId* anstelle des *FirewallPolicy-Parameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="b09e3-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="b09e3-135">Beispiel: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="b09e3-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="b09e3-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b09e3-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b09e3-137">Gibt das Front-End-IP-Konfigurationsobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b09e3-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b09e3-139">Gibt die ID der Front-End-IP-Konfiguration für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="b09e3-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b09e3-140">-FrontendPort</span></span>
<span data-ttu-id="b09e3-141">Gibt den Front-End-Port für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b09e3-142">-FrontendPortId</span></span>
<span data-ttu-id="b09e3-143">Gibt die ID des Front-End-Portobjekts für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="b09e3-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="b09e3-144">-HostName</span></span>
<span data-ttu-id="b09e3-145">Gibt den Hostnamen des HTTP-Listeners für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="b09e3-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="b09e3-146">-HostNames</span></span>
<span data-ttu-id="b09e3-147">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="b09e3-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-148">-Name</span><span class="sxs-lookup"><span data-stu-id="b09e3-148">-Name</span></span>
<span data-ttu-id="b09e3-149">Gibt den Namen des VON diesem Cmdlet erstellten HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b09e3-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b09e3-150">-Protocol</span></span>
<span data-ttu-id="b09e3-151">Gibt das Protokoll an, das vom HTTP-Listener verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b09e3-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b09e3-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b09e3-153">-SslCertificate</span></span>
<span data-ttu-id="b09e3-154">Gibt das SSL-Zertifikatobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b09e3-155">-SslCertificateId</span></span>
<span data-ttu-id="b09e3-156">Gibt die ID des SSL-Zertifikats für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="b09e3-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="b09e3-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b09e3-157">-SslProfile</span></span>
<span data-ttu-id="b09e3-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="b09e3-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09e3-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b09e3-159">-SslProfileId</span></span>
<span data-ttu-id="b09e3-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b09e3-160">SslProfileId</span></span>

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

### <span data-ttu-id="b09e3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09e3-161">CommonParameters</span></span>
<span data-ttu-id="b09e3-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09e3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09e3-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b09e3-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09e3-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b09e3-164">INPUTS</span></span>

### <span data-ttu-id="b09e3-165">Keine</span><span class="sxs-lookup"><span data-stu-id="b09e3-165">None</span></span>

## <span data-ttu-id="b09e3-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b09e3-166">OUTPUTS</span></span>

### <span data-ttu-id="b09e3-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b09e3-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b09e3-168">NOTES</span></span>

## <span data-ttu-id="b09e3-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b09e3-169">RELATED LINKS</span></span>

[<span data-ttu-id="b09e3-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b09e3-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b09e3-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b09e3-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b09e3-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


