---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006000"
---
# <span data-ttu-id="569e8-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="569e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="569e8-102">SYNOPSIS</span></span>
<span data-ttu-id="569e8-103">Aktualisiert die Eigenschaften eines Traffic Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="569e8-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="569e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="569e8-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="569e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="569e8-105">DESCRIPTION</span></span>
<span data-ttu-id="569e8-106">Das Cmdlet " **Satz-AzureTrafficManagerProfile** " aktualisiert die Eigenschaften eines Microsoft Azure Traffic Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="569e8-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="569e8-107">Bei Profilen, für die Sie den *LoadBalancingMethod* -Wert auf "Failover" festgelegt haben, können Sie die Failover-Reihenfolge der Endpunkte ermitteln, die Sie mit dem Add-AzureTrafficManagerEndpoint-Cmdlet zu Ihrem Profil hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="569e8-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="569e8-108">Weitere Informationen finden Sie unten in Beispiel 3.</span><span class="sxs-lookup"><span data-stu-id="569e8-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="569e8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="569e8-109">EXAMPLES</span></span>

### <span data-ttu-id="569e8-110">Beispiel 1: Einrichten der TTL für ein Traffic Manager-Profil</span><span class="sxs-lookup"><span data-stu-id="569e8-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="569e8-111">Mit diesem Befehl wird die TTL auf 60 Sekunden für das Traffic Manager-Profilobjekt MyTrafficManagerProfile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="569e8-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="569e8-112">Beispiel 2: setzen mehrerer Werte für ein Profil</span><span class="sxs-lookup"><span data-stu-id="569e8-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="569e8-113">Dieser Befehl ruft mit dem Cmdlet **Get-AzureTrafficManagerProfile** ein Traffic Manager-Profil mit dem Namen myProfile ab.</span><span class="sxs-lookup"><span data-stu-id="569e8-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="569e8-114">Das Profil verwendet die Roundrobin-Lastenausgleichsmethode, einen TTL-Wert von 30 Sekunden, das Monitor Protokoll http, den Monitor-Port und den relativen Pfad für ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="569e8-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="569e8-115">Beispiel 3: Neuanordnung von Endpunkten in der gewünschten Failover-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="569e8-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="569e8-116">In diesem Beispiel werden die zu myProfile hinzugefügten Endpunkte der gewünschten Failover-Reihenfolge neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="569e8-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="569e8-117">Der erste Befehl ruft das Traffic Manager-Profilobjekt mit dem Namen myProfile ab und speichert das Objekt in der $Profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="569e8-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="569e8-118">Der zweite Befehl ordnet die Endpunkte aus dem Array Endpunkte erneut an die Reihenfolge an, in der ein Failover erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="569e8-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="569e8-119">Mit dem letzten Befehl wird das in $Profile gespeicherte Traffic Manager-Profil mit der neuen Endpunkt Reihenfolge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="569e8-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="569e8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="569e8-120">PARAMETERS</span></span>

### <span data-ttu-id="569e8-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="569e8-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="569e8-122">Gibt die Methode zum Lastenausgleich an, mit der die Verbindung verteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="569e8-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="569e8-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="569e8-123">Valid values are:</span></span> 

- <span data-ttu-id="569e8-124">Leistung</span><span class="sxs-lookup"><span data-stu-id="569e8-124">Performance</span></span>
- <span data-ttu-id="569e8-125">Failover</span><span class="sxs-lookup"><span data-stu-id="569e8-125">Failover</span></span>
- <span data-ttu-id="569e8-126">Roundrobin</span><span class="sxs-lookup"><span data-stu-id="569e8-126">RoundRobin</span></span>

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

### <span data-ttu-id="569e8-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="569e8-127">-MonitorPort</span></span>
<span data-ttu-id="569e8-128">Gibt den Port an, der zum Überwachen der Endpunkt Integrität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="569e8-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="569e8-129">Gültige Werte sind ganzzahlige Werte, die größer als 0 und kleiner oder gleich 65.535 sind.</span><span class="sxs-lookup"><span data-stu-id="569e8-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="569e8-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="569e8-130">-MonitorProtocol</span></span>
<span data-ttu-id="569e8-131">Gibt das Protokoll an, das zum Überwachen der Endpunkt Integrität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="569e8-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="569e8-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="569e8-132">Valid values are:</span></span> 

- <span data-ttu-id="569e8-133">Http</span><span class="sxs-lookup"><span data-stu-id="569e8-133">Http</span></span>
- <span data-ttu-id="569e8-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="569e8-134">Https</span></span>

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

### <span data-ttu-id="569e8-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="569e8-135">-MonitorRelativePath</span></span>
<span data-ttu-id="569e8-136">Gibt den Pfad relativ zum Endpunkt Domänennamen an, um den Integritätsstatus zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="569e8-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="569e8-137">Der Pfad muss die folgenden Einschränkungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="569e8-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="569e8-138">Der Pfad muss zwischen 1 und 1000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="569e8-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="569e8-139">Sie muss mit einem Schrägstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="569e8-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="569e8-140">Sie darf keine XML-Elemente enthalten \<\> .</span><span class="sxs-lookup"><span data-stu-id="569e8-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="569e8-141">Sie darf keine doppelten Schrägstriche//aufweisen.</span><span class="sxs-lookup"><span data-stu-id="569e8-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="569e8-142">Sie darf keine ungültigen HTML-Escape-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="569e8-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="569e8-143">Beispiel:% XY.</span><span class="sxs-lookup"><span data-stu-id="569e8-143">For example, %XY.</span></span>

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

### <span data-ttu-id="569e8-144">-Name</span><span class="sxs-lookup"><span data-stu-id="569e8-144">-Name</span></span>
<span data-ttu-id="569e8-145">Gibt den Namen des zu aktualisierenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="569e8-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569e8-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="569e8-146">-Profile</span></span>
<span data-ttu-id="569e8-147">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="569e8-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="569e8-148">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="569e8-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="569e8-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="569e8-150">Gibt das Datenverkehrs Manager-Profilobjekt an, mit dem Sie das Profil festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="569e8-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="569e8-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="569e8-151">-Ttl</span></span>
<span data-ttu-id="569e8-152">Gibt die DNS-Gültigkeitsdauer (Time-to-Live, TTL) an, die die lokalen DNS-Konfliktlöser darüber informiert, wie lange DNS-Einträge zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="569e8-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="569e8-153">Gültige Werte sind eine ganze Zahl von 30 bis 999.999.</span><span class="sxs-lookup"><span data-stu-id="569e8-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="569e8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569e8-154">CommonParameters</span></span>
<span data-ttu-id="569e8-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569e8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569e8-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569e8-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569e8-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="569e8-157">INPUTS</span></span>

## <span data-ttu-id="569e8-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="569e8-158">OUTPUTS</span></span>

### <span data-ttu-id="569e8-159">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="569e8-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="569e8-160">Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="569e8-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="569e8-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="569e8-161">NOTES</span></span>

## <span data-ttu-id="569e8-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="569e8-162">RELATED LINKS</span></span>

[<span data-ttu-id="569e8-163">Deaktivieren-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="569e8-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="569e8-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="569e8-166">Neu – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="569e8-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="569e8-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


