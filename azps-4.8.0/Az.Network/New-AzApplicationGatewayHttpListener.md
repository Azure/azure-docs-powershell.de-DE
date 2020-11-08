---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166295"
---
# <span data-ttu-id="7472e-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7472e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7472e-102">SYNOPSIS</span></span>
<span data-ttu-id="7472e-103">Erstellt einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7472e-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="7472e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7472e-104">SYNTAX</span></span>

### <span data-ttu-id="7472e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7472e-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7472e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7472e-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7472e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7472e-107">DESCRIPTION</span></span>
<span data-ttu-id="7472e-108">Das Cmdlet **New-AzApplicationGatewayHttpListener** erstellt einen HTTP-Listener für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7472e-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="7472e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7472e-109">EXAMPLES</span></span>

### <span data-ttu-id="7472e-110">Beispiel 1: Erstellen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="7472e-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="7472e-111">Dieser Befehl erstellt einen HTTP-Listener mit dem Namen Listener01 und speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="7472e-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7472e-112">Beispiel 2: Erstellen eines HTTP-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="7472e-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="7472e-113">Dieser Befehl erstellt einen HTTP-Listener, der SSL-Entlastung verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7472e-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="7472e-114">Der Befehl speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="7472e-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7472e-115">Beispiel 3: Erstellen eines HTTP-Listeners mit Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="7472e-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="7472e-116">Dieser Befehl erstellt einen HTTP-Listener mit dem Namen Listener01, FirewallPolicy als $firewallPolicy und speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="7472e-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7472e-117">Beispiel 4: Hinzufügen eines HTTPS-Listener mit SSL und Hostnamen</span><span class="sxs-lookup"><span data-stu-id="7472e-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="7472e-118">Dieser Befehl erstellt einen HTTP-Listener, der SSL-Entlastung verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable zusammen mit zwei Hostnamen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7472e-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="7472e-119">Der Befehl speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="7472e-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="7472e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7472e-120">PARAMETERS</span></span>

### <span data-ttu-id="7472e-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7472e-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="7472e-122">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="7472e-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="7472e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7472e-123">-DefaultProfile</span></span>
<span data-ttu-id="7472e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7472e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7472e-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7472e-125">-FirewallPolicy</span></span>
<span data-ttu-id="7472e-126">Gibt den Objektverweis auf eine Firewall-Richtlinie auf oberster Ebene an.</span><span class="sxs-lookup"><span data-stu-id="7472e-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="7472e-127">Der Objektverweis kann mithilfe New-AzApplicationGatewayWebApplicationFirewallPolicy-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7472e-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="7472e-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" eine mit obigem Unifiedgroup erstellte Firewall-Richtlinie kann auf Pfad-Regelebene verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7472e-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="7472e-129">der obige Befehl würde eine Standardrichtlinien Einstellung und verwaltete Regeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="7472e-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="7472e-130">Anstelle der Standardwerte können Benutzer PolicySettings, ManagedRules, mithilfe von New-AzApplicationGatewayFirewallPolicySettings und New-AzApplicationGatewayFirewallPolicyManagedRules angeben.</span><span class="sxs-lookup"><span data-stu-id="7472e-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="7472e-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7472e-131">-FirewallPolicyId</span></span>
<span data-ttu-id="7472e-132">Gibt die ID einer vorhandenen Webanwendungs Firewall-Ressource auf oberster Ebene an.</span><span class="sxs-lookup"><span data-stu-id="7472e-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="7472e-133">Firewall-Richtlinien-IDs können mithilfe des Get-AzApplicationGatewayWebApplicationFirewallPolicy-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7472e-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="7472e-134">Nachdem wir die ID haben, können Sie *FirewallPolicyId* -Parameter anstelle des *FirewallPolicy* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="7472e-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="7472e-135">Beispiel:-FirewallPolicyId/Subscriptions/<Abonnement-ID>/resourceGroups/<Resource-Group-ID>/Providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="7472e-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="7472e-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7472e-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="7472e-137">Gibt das Front-End-IP-Konfigurationsobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7472e-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="7472e-139">Gibt die ID der Front-End-IP-Konfiguration für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7472e-140">-FrontendPort</span></span>
<span data-ttu-id="7472e-141">Gibt den Front-End-Port für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="7472e-142">-FrontendPortId</span></span>
<span data-ttu-id="7472e-143">Gibt die ID des Front-End-Port Objekts für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-144">-Hostname</span><span class="sxs-lookup"><span data-stu-id="7472e-144">-HostName</span></span>
<span data-ttu-id="7472e-145">Gibt den Hostnamen des Application Gateway HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="7472e-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-146">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="7472e-146">-HostNames</span></span>
<span data-ttu-id="7472e-147">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="7472e-147">Host names</span></span>

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

### <span data-ttu-id="7472e-148">-Name</span><span class="sxs-lookup"><span data-stu-id="7472e-148">-Name</span></span>
<span data-ttu-id="7472e-149">Gibt den Namen des vom Cmdlet erstellten HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="7472e-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7472e-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7472e-150">-Protocol</span></span>
<span data-ttu-id="7472e-151">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="7472e-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="7472e-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="7472e-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="7472e-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7472e-153">-SslCertificate</span></span>
<span data-ttu-id="7472e-154">Gibt das SSL-Zertifikatobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="7472e-155">-SslCertificateId</span></span>
<span data-ttu-id="7472e-156">Gibt die ID des SSL-Zertifikats für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7472e-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="7472e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7472e-157">CommonParameters</span></span>
<span data-ttu-id="7472e-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7472e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7472e-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7472e-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7472e-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7472e-160">INPUTS</span></span>

### <span data-ttu-id="7472e-161">Keine</span><span class="sxs-lookup"><span data-stu-id="7472e-161">None</span></span>

## <span data-ttu-id="7472e-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7472e-162">OUTPUTS</span></span>

### <span data-ttu-id="7472e-163">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7472e-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="7472e-164">NOTES</span></span>

## <span data-ttu-id="7472e-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7472e-165">RELATED LINKS</span></span>

[<span data-ttu-id="7472e-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7472e-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7472e-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7472e-169">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7472e-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


