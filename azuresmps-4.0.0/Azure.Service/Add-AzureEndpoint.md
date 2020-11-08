---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005939"
---
# <span data-ttu-id="5b5fa-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b5fa-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="5b5fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5fa-103">Fügt einen Endpunkt zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="5b5fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b5fa-104">SYNTAX</span></span>

### <span data-ttu-id="5b5fa-105">NoLB (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b5fa-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b5fa-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="5b5fa-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b5fa-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="5b5fa-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b5fa-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="5b5fa-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5b5fa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b5fa-109">DESCRIPTION</span></span>
<span data-ttu-id="5b5fa-110">Mit dem Cmdlet **Add-AzureEndpoint** wird ein Endpunkt zu einem Azure Virtual Machine-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="5b5fa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b5fa-111">EXAMPLES</span></span>

### <span data-ttu-id="5b5fa-112">Beispiel 1: Hinzufügen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="5b5fa-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="5b5fa-113">Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine01 ab.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="5b5fa-114">Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b5fa-115">Mit diesem Cmdlet wird ein Endpunkt mit dem Namen httpin hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="5b5fa-116">Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="5b5fa-117">Der Befehl übergibt das Objekt des virtuellen Computers an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="5b5fa-118">Beispiel 2: Hinzufügen eines Endpunkts, der zu einer Lastenausgleichs Gruppe gehört</span><span class="sxs-lookup"><span data-stu-id="5b5fa-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="5b5fa-119">Dieser Befehl ruft die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5b5fa-120">Das aktuelle Cmdlet fügt einen Endpunkt mit dem Namen httpin hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="5b5fa-121">Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="5b5fa-122">Der Endpunkt gehört zur Gruppe Shared Load Balanced mit dem Namen Webfarm.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="5b5fa-123">Eine HTTP-Sonde auf Port 80 mit dem Pfad "/" überwacht die Verfügbarkeit des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="5b5fa-124">Der Befehl implementiert Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-124">The command implements your changes.</span></span>

### <span data-ttu-id="5b5fa-125">Beispiel 3: Zuordnen einer virtuellen IP zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5b5fa-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="5b5fa-126">Dieser Befehl ruft die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine25 ab.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="5b5fa-127">Das aktuelle Cmdlet fügt einen Endpunkt mit dem Namen httpin hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="5b5fa-128">Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="5b5fa-129">Dieser Befehl ordnet dem Endpunkt eine virtuelle IP-Adresse zu.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="5b5fa-130">Der Befehl implementiert Ihre Änderungen.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-130">The command implements your changes.</span></span>

## <span data-ttu-id="5b5fa-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b5fa-131">PARAMETERS</span></span>

### <span data-ttu-id="5b5fa-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="5b5fa-132">-ACL</span></span>
<span data-ttu-id="5b5fa-133">Gibt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="5b5fa-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="5b5fa-134">-DefaultProbe</span></span>
<span data-ttu-id="5b5fa-135">Gibt an, dass dieses Cmdlet die standardmäßige Prüf Punkt Einstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="5b5fa-136">-DirectServerReturn</span></span>
<span data-ttu-id="5b5fa-137">Gibt an, ob dieses Cmdlet die direkte Server Rückgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="5b5fa-138">Geben Sie $true an, die aktiviert werden soll, oder deaktivieren Sie $false.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="5b5fa-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5b5fa-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5b5fa-140">Gibt den TCP-Leerlauftimeout Zeitraum (in Minuten) für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="5b5fa-141">-Information</span><span class="sxs-lookup"><span data-stu-id="5b5fa-141">-InformationAction</span></span>
<span data-ttu-id="5b5fa-142">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5b5fa-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b5fa-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b5fa-144">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5b5fa-144">Continue</span></span>
- <span data-ttu-id="5b5fa-145">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5b5fa-145">Ignore</span></span>
- <span data-ttu-id="5b5fa-146">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5b5fa-146">Inquire</span></span>
- <span data-ttu-id="5b5fa-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5b5fa-147">SilentlyContinue</span></span>
- <span data-ttu-id="5b5fa-148">Beenden</span><span class="sxs-lookup"><span data-stu-id="5b5fa-148">Stop</span></span>
- <span data-ttu-id="5b5fa-149">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5b5fa-149">Suspend</span></span>

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

### <span data-ttu-id="5b5fa-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5b5fa-150">-InformationVariable</span></span>
<span data-ttu-id="5b5fa-151">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5b5fa-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="5b5fa-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="5b5fa-153">Gibt den Namen des internen Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="5b5fa-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="5b5fa-154">-LBSetName</span></span>
<span data-ttu-id="5b5fa-155">Gibt den Namen des Load Balancer-Satzes für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="5b5fa-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="5b5fa-157">Gibt den Verteilungs Algorithmus des Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="5b5fa-158">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5b5fa-158">Valid values are:</span></span> 

- <span data-ttu-id="5b5fa-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-159">sourceIP.</span></span>
<span data-ttu-id="5b5fa-160">Zwei Tupel-Affinität: Quell-IP, Ziel-IP</span><span class="sxs-lookup"><span data-stu-id="5b5fa-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="5b5fa-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-161">sourceIPProtocol.</span></span>
<span data-ttu-id="5b5fa-162">Eine drei-Tupel-Affinität: Quell-IP, Ziel-IP, Protokoll</span><span class="sxs-lookup"><span data-stu-id="5b5fa-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="5b5fa-163">keine.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-163">none.</span></span>
<span data-ttu-id="5b5fa-164">Eine fünf-Tupel-Affinität: Quell-IP, Quell-Port, Ziel-IP, Ziel-Port, Protokoll</span><span class="sxs-lookup"><span data-stu-id="5b5fa-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="5b5fa-165">Der Standardwert ist None.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-165">The default value is none.</span></span>

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

### <span data-ttu-id="5b5fa-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="5b5fa-166">-LocalPort</span></span>
<span data-ttu-id="5b5fa-167">Gibt den lokalen, privaten Port an, den dieser Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="5b5fa-168">Anwendungen innerhalb des virtuellen Computers lauschen diesem Port für Dienst Eingabeanforderungen für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-169">-Name</span><span class="sxs-lookup"><span data-stu-id="5b5fa-169">-Name</span></span>
<span data-ttu-id="5b5fa-170">Gibt einen Namen für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-171">-Noprobe</span><span class="sxs-lookup"><span data-stu-id="5b5fa-171">-NoProbe</span></span>
<span data-ttu-id="5b5fa-172">Gibt an, dass dieses Cmdlet die Einstellung keine Sonde verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5b5fa-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="5b5fa-174">Gibt das Abfrageintervall für den Prüfpunkt in Sekunden für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="5b5fa-175">-ProbePath</span></span>
<span data-ttu-id="5b5fa-176">Gibt den relativen Pfad zur http-Sonde an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="5b5fa-177">-ProbePort</span></span>
<span data-ttu-id="5b5fa-178">Gibt den Port an, den der Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="5b5fa-179">-ProbeProtocol</span></span>
<span data-ttu-id="5b5fa-180">Gibt das Port Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-180">Specifies the port protocol.</span></span>
<span data-ttu-id="5b5fa-181">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5b5fa-181">Valid values are:</span></span> 

- <span data-ttu-id="5b5fa-182">TCP</span><span class="sxs-lookup"><span data-stu-id="5b5fa-182">tcp</span></span> 
- <span data-ttu-id="5b5fa-183">http</span><span class="sxs-lookup"><span data-stu-id="5b5fa-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5b5fa-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="5b5fa-185">Gibt den Zeitüberschreitungszeitraum für das Abrufen von Sonden in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-186">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b5fa-186">-Profile</span></span>
<span data-ttu-id="5b5fa-187">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b5fa-188">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b5fa-189">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5b5fa-189">-Protocol</span></span>
<span data-ttu-id="5b5fa-190">Gibt das Protokoll des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="5b5fa-191">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5b5fa-191">Valid values are:</span></span> 

- <span data-ttu-id="5b5fa-192">TCP</span><span class="sxs-lookup"><span data-stu-id="5b5fa-192">tcp</span></span> 
- <span data-ttu-id="5b5fa-193">UDP</span><span class="sxs-lookup"><span data-stu-id="5b5fa-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="5b5fa-194">-PublicPort</span></span>
<span data-ttu-id="5b5fa-195">Gibt den öffentlichen Port an, den der Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="5b5fa-196">Wenn Sie keinen Wert angeben, weist Azure einen verfügbaren Port zu.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="5b5fa-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="5b5fa-197">-VirtualIPName</span></span>
<span data-ttu-id="5b5fa-198">Gibt den Namen einer virtuellen IP-Adresse an, die Azure dem Endpunkt zuordnet.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="5b5fa-199">Ihr Dienst kann mehrere virtuelle IPS aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="5b5fa-200">Verwenden Sie zum Erstellen von virtuellen IPS das Cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="5b5fa-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="5b5fa-201">-VM</span><span class="sxs-lookup"><span data-stu-id="5b5fa-201">-VM</span></span>
<span data-ttu-id="5b5fa-202">Gibt den virtuellen Computer an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5fa-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5fa-203">CommonParameters</span></span>
<span data-ttu-id="5b5fa-204">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5fa-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5fa-205">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b5fa-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5fa-206">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b5fa-206">INPUTS</span></span>

## <span data-ttu-id="5b5fa-207">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b5fa-207">OUTPUTS</span></span>

### <span data-ttu-id="5b5fa-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="5b5fa-208">System.Object</span></span>

## <span data-ttu-id="5b5fa-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b5fa-209">NOTES</span></span>

## <span data-ttu-id="5b5fa-210">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b5fa-210">RELATED LINKS</span></span>

[<span data-ttu-id="5b5fa-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="5b5fa-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="5b5fa-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b5fa-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="5b5fa-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5b5fa-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="5b5fa-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b5fa-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="5b5fa-215">Satz-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b5fa-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="5b5fa-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5b5fa-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


