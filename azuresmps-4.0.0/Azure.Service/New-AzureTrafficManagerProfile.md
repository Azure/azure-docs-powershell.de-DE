---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006408"
---
# <span data-ttu-id="bf278-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="bf278-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf278-102">SYNOPSIS</span></span>
<span data-ttu-id="bf278-103">Erstellt ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="bf278-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="bf278-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf278-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf278-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf278-105">DESCRIPTION</span></span>
<span data-ttu-id="bf278-106">Das Cmdlet **New-AzureTrafficManagerProfile** erstellt ein Microsoft Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="bf278-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="bf278-107">Nachdem Sie ein Profil erstellt haben, in dem Sie den *LoadBalancingMethod* -Wert auf "Failover" festgelegt haben, können Sie die Failover-Reihenfolge der Endpunkte ermitteln, die Sie mit dem Add-AzureTrafficManagerEndpoint-Cmdlet zu Ihrem Profil hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf278-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="bf278-108">Weitere Informationen finden Sie unten im Beispiel 2.</span><span class="sxs-lookup"><span data-stu-id="bf278-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="bf278-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf278-109">EXAMPLES</span></span>

### <span data-ttu-id="bf278-110">Beispiel 1: Erstellen eines Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="bf278-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="bf278-111">Mit diesem Befehl wird in der angegebenen Datenverkehrs-Manager-Domäne mit einer Round-Robin-Lastenausgleichsmethode, einem TTL-Wert von 30 Sekunden, dem http-Überwachungsprotokoll, dem Überwachungs-Port 80 und dem angegebenen Pfad ein Traffic Manager-Profil mit dem Namen "myprofil" erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf278-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="bf278-112">Beispiel 2: Neuanordnung von Endpunkten in der gewünschten Failover-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="bf278-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="bf278-113">In diesem Beispiel werden die zu myProfile hinzugefügten Endpunkte der gewünschten Failover-Reihenfolge neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="bf278-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="bf278-114">Der erste Befehl ruft das Traffic Manager-Profilobjekt mit dem Namen myProfile ab und speichert das Objekt in der $Profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="bf278-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="bf278-115">Der zweite Befehl ordnet die Endpunkte aus dem Array Endpunkte erneut an die Reihenfolge an, in der ein Failover erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="bf278-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="bf278-116">Mit dem letzten Befehl wird das in $Profile gespeicherte Traffic Manager-Profil mit der neuen Endpunkt Reihenfolge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bf278-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="bf278-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf278-117">PARAMETERS</span></span>

### <span data-ttu-id="bf278-118">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="bf278-118">-DomainName</span></span>
<span data-ttu-id="bf278-119">Gibt den Domänennamen des Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="bf278-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="bf278-120">Dies muss eine Unterdomäne von Trafficmanager.net sein.</span><span class="sxs-lookup"><span data-stu-id="bf278-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="bf278-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="bf278-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="bf278-122">Gibt die Methode zum Lastenausgleich an, mit der die Verbindung verteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf278-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="bf278-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bf278-123">Valid values are:</span></span> 

- <span data-ttu-id="bf278-124">Leistung</span><span class="sxs-lookup"><span data-stu-id="bf278-124">Performance</span></span>
- <span data-ttu-id="bf278-125">Failover</span><span class="sxs-lookup"><span data-stu-id="bf278-125">Failover</span></span>
- <span data-ttu-id="bf278-126">Roundrobin</span><span class="sxs-lookup"><span data-stu-id="bf278-126">RoundRobin</span></span>

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

### <span data-ttu-id="bf278-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="bf278-127">-MonitorPort</span></span>
<span data-ttu-id="bf278-128">Gibt den Port an, der zum Überwachen der Endpunkt Integrität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf278-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="bf278-129">Gültige Werte sind ganzzahlige Werte, die größer als 0 und kleiner oder gleich 65.535 sind.</span><span class="sxs-lookup"><span data-stu-id="bf278-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf278-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="bf278-130">-MonitorProtocol</span></span>
<span data-ttu-id="bf278-131">Gibt das Protokoll an, das zum Überwachen der Endpunkt Integrität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf278-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="bf278-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bf278-132">Valid values are:</span></span> 

- <span data-ttu-id="bf278-133">Http</span><span class="sxs-lookup"><span data-stu-id="bf278-133">Http</span></span>

- <span data-ttu-id="bf278-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="bf278-134">Https</span></span>

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

### <span data-ttu-id="bf278-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="bf278-135">-MonitorRelativePath</span></span>
<span data-ttu-id="bf278-136">Gibt den Pfad relativ zum Endpunkt Domänennamen an, um den Integritätsstatus zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bf278-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="bf278-137">Der Pfad muss die folgenden Einschränkungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="bf278-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="bf278-138">Der Pfad muss zwischen 1 und 1000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="bf278-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="bf278-139">Sie muss mit einem Schrägstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="bf278-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="bf278-140">Sie darf keine XML-Elemente enthalten \<\> .</span><span class="sxs-lookup"><span data-stu-id="bf278-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="bf278-141">Sie darf keine doppelten Schrägstriche//aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bf278-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="bf278-142">Sie darf keine ungültigen HTML-Escape-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf278-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="bf278-143">Beispiel:% XY.</span><span class="sxs-lookup"><span data-stu-id="bf278-143">For example, %XY.</span></span>

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

### <span data-ttu-id="bf278-144">-Name</span><span class="sxs-lookup"><span data-stu-id="bf278-144">-Name</span></span>
<span data-ttu-id="bf278-145">Gibt den Namen des zu erstellenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="bf278-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf278-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf278-146">-Profile</span></span>
<span data-ttu-id="bf278-147">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bf278-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bf278-148">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bf278-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf278-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="bf278-149">-Ttl</span></span>
<span data-ttu-id="bf278-150">Gibt die DNS-Gültigkeitsdauer (Time-to-Live, TTL) an, die die lokalen DNS-Konfliktlöser darüber informiert, wie lange DNS-Einträge zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bf278-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="bf278-151">Gültige Werte sind ganze Zahlen von 30 bis 999.999.</span><span class="sxs-lookup"><span data-stu-id="bf278-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf278-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf278-152">CommonParameters</span></span>
<span data-ttu-id="bf278-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf278-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf278-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf278-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf278-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf278-155">INPUTS</span></span>

## <span data-ttu-id="bf278-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf278-156">OUTPUTS</span></span>

### <span data-ttu-id="bf278-157">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="bf278-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="bf278-158">Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="bf278-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="bf278-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf278-159">NOTES</span></span>

## <span data-ttu-id="bf278-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf278-160">RELATED LINKS</span></span>

[<span data-ttu-id="bf278-161">Deaktivieren-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bf278-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bf278-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bf278-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bf278-165">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


