---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006159"
---
# <span data-ttu-id="c4b9a-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="c4b9a-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="c4b9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b9a-103">Ändert alle Endpunkte in einem Load Balancer-Satz innerhalb eines Azure-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="c4b9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4b9a-104">SYNTAX</span></span>

### <span data-ttu-id="c4b9a-105">DefaultProbe (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4b9a-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4b9a-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="c4b9a-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4b9a-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="c4b9a-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4b9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4b9a-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b9a-109">Das Cmdlet " **Satz-AzureLoadBalancedEndpoint** " ändert alle Endpunkte in einem Load Balancer-Satz in einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="c4b9a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b9a-111">Beispiel 1: Ändern der Endpunkte in einem Load Balancer-Satz</span><span class="sxs-lookup"><span data-stu-id="c4b9a-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="c4b9a-112">Dieser Befehl ändert alle Endpunkte im Lastenausgleichs Satz mit dem Namen LBSet01, um das TCP-Protokoll und den privaten Port 80 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="c4b9a-113">Mit dem Befehl wird der Load Balancer-Prüfpunkt so festgelegt, dass das TCP-Protokoll auf Port 8080 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="c4b9a-114">Beispiel 2: Angeben einer anderen virtuellen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="c4b9a-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="c4b9a-115">Mit diesem Befehl wird das Load Balancer geändert, bei dem der Lastenausgleichs Satz-Name für die Verwendung einer virtuellen IP mit dem Namen Vip01 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="c4b9a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4b9a-116">PARAMETERS</span></span>

### <span data-ttu-id="c4b9a-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="c4b9a-117">-ACL</span></span>
<span data-ttu-id="c4b9a-118">Gibt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) an, das dieses Cmdlet auf die Endpunkte anwendet.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="c4b9a-119">-DirectServerReturn</span></span>
<span data-ttu-id="c4b9a-120">Gibt an, ob dieses Cmdlet die direkte Server Rückgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="c4b9a-121">Geben Sie $true an, die aktiviert werden soll, oder deaktivieren Sie $false.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c4b9a-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c4b9a-123">Gibt den TCP-Leerlauftimeout Zeitraum (in Minuten) für die Endpunkte an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-124">-Information</span><span class="sxs-lookup"><span data-stu-id="c4b9a-124">-InformationAction</span></span>
<span data-ttu-id="c4b9a-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4b9a-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c4b9a-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4b9a-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c4b9a-127">Continue</span></span>
- <span data-ttu-id="c4b9a-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c4b9a-128">Ignore</span></span>
- <span data-ttu-id="c4b9a-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c4b9a-129">Inquire</span></span>
- <span data-ttu-id="c4b9a-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4b9a-130">SilentlyContinue</span></span>
- <span data-ttu-id="c4b9a-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="c4b9a-131">Stop</span></span>
- <span data-ttu-id="c4b9a-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c4b9a-132">Suspend</span></span>

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

### <span data-ttu-id="c4b9a-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4b9a-133">-InformationVariable</span></span>
<span data-ttu-id="c4b9a-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4b9a-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c4b9a-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="c4b9a-136">Gibt den Namen des internen Lastenausgleichs an, den dieses Cmdlet in die Konfiguration einschließt.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="c4b9a-137">-LBSetName</span></span>
<span data-ttu-id="c4b9a-138">Gibt den Namen des Load Balancer-Satzes an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="c4b9a-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="c4b9a-140">Gibt den Verteilungs Algorithmus des Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="c4b9a-141">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c4b9a-141">Valid values are:</span></span> 

- <span data-ttu-id="c4b9a-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-142">sourceIP.</span></span>
<span data-ttu-id="c4b9a-143">Zwei Tupel-Affinität: Quell-IP, Ziel-IP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="c4b9a-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-144">sourceIPProtocol.</span></span>
<span data-ttu-id="c4b9a-145">Eine drei-Tupel-Affinität: Quell-IP, Ziel-IP, Protokoll</span><span class="sxs-lookup"><span data-stu-id="c4b9a-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="c4b9a-146">keine.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-146">none.</span></span>
<span data-ttu-id="c4b9a-147">Eine fünf-Tupel-Affinität: Quell-IP, Quell-Port, Ziel-IP, Ziel-Port, Protokoll</span><span class="sxs-lookup"><span data-stu-id="c4b9a-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="c4b9a-148">Der Standardwert ist None.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-148">The default value is none.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="c4b9a-149">-LocalPort</span></span>
<span data-ttu-id="c4b9a-150">Gibt den lokalen, privaten Port an, den diese Endpunkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="c4b9a-151">Anwendungen auf dem virtuellen Computer überwachen diesen Port für Dienst Eingabeanforderungen für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4b9a-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="c4b9a-153">Gibt das Prüfpunkt-Abrufintervall für die Endpunkte in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="c4b9a-154">-ProbePath</span></span>
<span data-ttu-id="c4b9a-155">Gibt den relativen Pfad des http-Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="c4b9a-156">-ProbePort</span></span>
<span data-ttu-id="c4b9a-157">Gibt den Port an, der vom Load Balancer-Prüfpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="c4b9a-159">Gibt an, dass die Load Balancer-Endpunkte eine HTTP-Sonde verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="c4b9a-161">Gibt an, dass die Load Balancer-Endpunkte eine TCP-Sonde verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4b9a-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="c4b9a-163">Gibt das Polling-Timeout für Sonden in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-164">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4b9a-164">-Profile</span></span>
<span data-ttu-id="c4b9a-165">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4b9a-166">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4b9a-167">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c4b9a-167">-Protocol</span></span>
<span data-ttu-id="c4b9a-168">Gibt das Protokoll der Endpunkte an.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="c4b9a-169">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c4b9a-169">Valid values are:</span></span> 

- <span data-ttu-id="c4b9a-170">TCP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-170">TCP</span></span> 
- <span data-ttu-id="c4b9a-171">UDP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-171">UDP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="c4b9a-172">-PublicPort</span></span>
<span data-ttu-id="c4b9a-173">Gibt den öffentlichen Port an, den der Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="c4b9a-174">Wenn Sie keinen Wert angeben, weist Azure einen verfügbaren Port zu.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-174">If you do not specify a value, Azure assigns an available port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4b9a-175">-ServiceName</span></span>
<span data-ttu-id="c4b9a-176">Gibt den Namen des Azure-Diensts an, der die Endpunkte enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c4b9a-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="c4b9a-177">-VirtualIPName</span></span>
<span data-ttu-id="c4b9a-178">Gibt den Namen einer virtuellen IP-Adresse an, die Azure den Endpunkten zuordnet.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="c4b9a-179">Wenn Sie Ihrem Dienst virtuelles IPS hinzufügen möchten, verwenden Sie das Cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="c4b9a-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b9a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b9a-180">CommonParameters</span></span>
<span data-ttu-id="c4b9a-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b9a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b9a-182">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b9a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b9a-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4b9a-183">INPUTS</span></span>

## <span data-ttu-id="c4b9a-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4b9a-184">OUTPUTS</span></span>

## <span data-ttu-id="c4b9a-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4b9a-185">NOTES</span></span>

## <span data-ttu-id="c4b9a-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4b9a-186">RELATED LINKS</span></span>

[<span data-ttu-id="c4b9a-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="c4b9a-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="c4b9a-188">Satz-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4b9a-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


