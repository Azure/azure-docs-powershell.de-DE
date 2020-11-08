---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006263"
---
# <span data-ttu-id="b0e90-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0e90-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="b0e90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0e90-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e90-103">Ändert einen Endpunkt, der einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b0e90-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="b0e90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e90-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b0e90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0e90-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e90-106">Das Cmdlet " **Satz-AzureEndpoint** " ändert einen Endpunkt, der einem Azure Virtual Machine zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b0e90-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="b0e90-107">Sie können Änderungen an einem Endpunkt angeben, bei dem es sich nicht um einen Lastenausgleich handelt.</span><span class="sxs-lookup"><span data-stu-id="b0e90-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="b0e90-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0e90-108">EXAMPLES</span></span>

### <span data-ttu-id="b0e90-109">Beispiel 1: Ändern eines Endpunkts, um einen Port zu überwachen</span><span class="sxs-lookup"><span data-stu-id="b0e90-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="b0e90-110">Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine01 ab.</span><span class="sxs-lookup"><span data-stu-id="b0e90-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b0e90-111">Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e90-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0e90-112">Mit diesem Cmdlet wird der Endpunkt mit dem Namen Web so geändert, dass er Port 443 überwacht.</span><span class="sxs-lookup"><span data-stu-id="b0e90-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="b0e90-113">Der Befehl übergibt das Objekt des virtuellen Computers an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="b0e90-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="b0e90-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0e90-114">PARAMETERS</span></span>

### <span data-ttu-id="b0e90-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="b0e90-115">-ACL</span></span>
<span data-ttu-id="b0e90-116">Gibt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) an, das dieses Cmdlet auf den Endpunkt anwendet.</span><span class="sxs-lookup"><span data-stu-id="b0e90-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="b0e90-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="b0e90-117">-DirectServerReturn</span></span>
<span data-ttu-id="b0e90-118">Gibt an, ob dieses Cmdlet die direkte Server Rückgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b0e90-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="b0e90-119">Geben Sie $true an, die aktiviert werden soll, oder deaktivieren Sie $false.</span><span class="sxs-lookup"><span data-stu-id="b0e90-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="b0e90-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b0e90-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b0e90-121">Gibt den TCP-Leerlauftimeout Zeitraum (in Minuten) für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="b0e90-122">-Information</span><span class="sxs-lookup"><span data-stu-id="b0e90-122">-InformationAction</span></span>
<span data-ttu-id="b0e90-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b0e90-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b0e90-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b0e90-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0e90-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b0e90-125">Continue</span></span>
- <span data-ttu-id="b0e90-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b0e90-126">Ignore</span></span>
- <span data-ttu-id="b0e90-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b0e90-127">Inquire</span></span>
- <span data-ttu-id="b0e90-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b0e90-128">SilentlyContinue</span></span>
- <span data-ttu-id="b0e90-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="b0e90-129">Stop</span></span>
- <span data-ttu-id="b0e90-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b0e90-130">Suspend</span></span>

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

### <span data-ttu-id="b0e90-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b0e90-131">-InformationVariable</span></span>
<span data-ttu-id="b0e90-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b0e90-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b0e90-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="b0e90-134">Gibt den Namen des internen Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="b0e90-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="b0e90-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="b0e90-136">Gibt den Verteilungs Algorithmus des Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="b0e90-137">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b0e90-137">Valid values are:</span></span> 

- <span data-ttu-id="b0e90-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="b0e90-138">sourceIP.</span></span>
<span data-ttu-id="b0e90-139">Zwei Tupel-Affinität: Quell-IP, Ziel-IP</span><span class="sxs-lookup"><span data-stu-id="b0e90-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="b0e90-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="b0e90-140">sourceIPProtocol.</span></span>
<span data-ttu-id="b0e90-141">Eine drei-Tupel-Affinität: Quell-IP, Ziel-IP, Protokoll</span><span class="sxs-lookup"><span data-stu-id="b0e90-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="b0e90-142">keine.</span><span class="sxs-lookup"><span data-stu-id="b0e90-142">none.</span></span>
<span data-ttu-id="b0e90-143">Eine fünf-Tupel-Affinität: Quell-IP, Quell-Port, Ziel-IP, Ziel-Port, Protokoll</span><span class="sxs-lookup"><span data-stu-id="b0e90-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="b0e90-144">Der Standardwert ist None.</span><span class="sxs-lookup"><span data-stu-id="b0e90-144">The default value is none.</span></span>

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

### <span data-ttu-id="b0e90-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="b0e90-145">-LocalPort</span></span>
<span data-ttu-id="b0e90-146">Gibt den lokalen, privaten Port an, den dieser Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0e90-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="b0e90-147">Anwendungen innerhalb des virtuellen Computers lauschen diesem Port für Dienst Eingabeanforderungen für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b0e90-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e90-148">-Name</span><span class="sxs-lookup"><span data-stu-id="b0e90-148">-Name</span></span>
<span data-ttu-id="b0e90-149">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b0e90-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="b0e90-150">-Profile</span></span>
<span data-ttu-id="b0e90-151">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b0e90-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0e90-152">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b0e90-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0e90-153">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b0e90-153">-Protocol</span></span>
<span data-ttu-id="b0e90-154">Gibt das Protokoll des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b0e90-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="b0e90-155">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b0e90-155">Valid values are:</span></span> 

- <span data-ttu-id="b0e90-156">TCP</span><span class="sxs-lookup"><span data-stu-id="b0e90-156">tcp</span></span> 
- <span data-ttu-id="b0e90-157">UDP</span><span class="sxs-lookup"><span data-stu-id="b0e90-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e90-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="b0e90-158">-PublicPort</span></span>
<span data-ttu-id="b0e90-159">Gibt den öffentlichen Port an, den der Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0e90-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="b0e90-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="b0e90-160">-VirtualIPName</span></span>
<span data-ttu-id="b0e90-161">Gibt den Namen einer virtuellen IP-Adresse an, die Azure dem Endpunkt zuordnet.</span><span class="sxs-lookup"><span data-stu-id="b0e90-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="b0e90-162">Ihr Dienst kann mehrere virtuelle IPS aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b0e90-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="b0e90-163">Verwenden Sie zum Erstellen von virtuellen IPS das Cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="b0e90-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="b0e90-164">-VM</span><span class="sxs-lookup"><span data-stu-id="b0e90-164">-VM</span></span>
<span data-ttu-id="b0e90-165">Gibt den virtuellen Computer an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b0e90-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b0e90-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e90-166">CommonParameters</span></span>
<span data-ttu-id="b0e90-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e90-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e90-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e90-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e90-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0e90-169">INPUTS</span></span>

## <span data-ttu-id="b0e90-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0e90-170">OUTPUTS</span></span>

### <span data-ttu-id="b0e90-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="b0e90-171">System.Object</span></span>

## <span data-ttu-id="b0e90-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0e90-172">NOTES</span></span>

## <span data-ttu-id="b0e90-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0e90-173">RELATED LINKS</span></span>

[<span data-ttu-id="b0e90-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0e90-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="b0e90-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="b0e90-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="b0e90-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0e90-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="b0e90-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b0e90-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b0e90-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0e90-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="b0e90-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b0e90-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


