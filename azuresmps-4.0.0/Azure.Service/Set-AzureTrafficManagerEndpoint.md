---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005640"
---
# <span data-ttu-id="630c6-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="630c6-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="630c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="630c6-102">SYNOPSIS</span></span>
<span data-ttu-id="630c6-103">Aktualisiert die Eigenschaften eines Endpunkts in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="630c6-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="630c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="630c6-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="630c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="630c6-105">DESCRIPTION</span></span>
<span data-ttu-id="630c6-106">Das Cmdlet " **Satz-AzureTrafficManagerEndpoint** " aktualisiert die Eigenschaften eines Endpunkts in einem Microsoft Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="630c6-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="630c6-107">Wenn der Endpunkt im aktuellen Profil nicht vorhanden ist, wird dieser vom Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="630c6-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="630c6-108">Nachdem Sie einen Endpunkt hinzugefügt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".</span><span class="sxs-lookup"><span data-stu-id="630c6-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="630c6-109">Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="630c6-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="630c6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="630c6-110">EXAMPLES</span></span>

### <span data-ttu-id="630c6-111">Beispiel 1: Aktualisieren eines Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="630c6-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="630c6-112">Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="630c6-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="630c6-113">Mit dem zweiten Befehl wird der Endpunkt im Profil des Datenverkehrs-Managers aktualisiert, der in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="630c6-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="630c6-114">Der Endpunkt hat den Domänennamen ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="630c6-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="630c6-115">Der Befehl gibt auch den Status, den Typ, die Gewichtung und die Position des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="630c6-116">Der Befehl übergibt das geänderte Profil an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="630c6-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="630c6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="630c6-117">PARAMETERS</span></span>

### <span data-ttu-id="630c6-118">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="630c6-118">-DomainName</span></span>
<span data-ttu-id="630c6-119">Gibt den Domänennamen des zu ändernden Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="630c6-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="630c6-120">-Location</span></span>
<span data-ttu-id="630c6-121">Gibt den Speicherort des vom Cmdlet hinzugefügten Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="630c6-122">Dies muss eine Azure-Position sein.</span><span class="sxs-lookup"><span data-stu-id="630c6-122">This must be an Azure location.</span></span>

<span data-ttu-id="630c6-123">Dieser Parameter muss einen Wert für Endpunkte des Typs "Any" oder des Typs "Trafficmanager" in einem Profil enthalten, bei dem die Load Balancing-Methode auf "Leistung" festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="630c6-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="630c6-124">Mögliche Werte sind die Namen der Azure-Region, wie unter aufgeführt  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="630c6-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="630c6-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="630c6-125">-MinChildEndpoints</span></span>
<span data-ttu-id="630c6-126">Gibt die Mindestanzahl von Endpunkten an, die das verschachtelte Profil Online haben muss, damit dieser Endpunkt als Online betrachtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="630c6-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="630c6-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="630c6-127">-Profile</span></span>
<span data-ttu-id="630c6-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="630c6-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="630c6-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="630c6-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="630c6-130">-Status</span><span class="sxs-lookup"><span data-stu-id="630c6-130">-Status</span></span>
<span data-ttu-id="630c6-131">Gibt den Status des Überwachungs Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="630c6-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="630c6-132">Valid values are:</span></span> 

- <span data-ttu-id="630c6-133">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="630c6-133">Enabled</span></span>
- <span data-ttu-id="630c6-134">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="630c6-134">Disabled</span></span>

<span data-ttu-id="630c6-135">Wenn Sie den Wert enabled angeben, überwacht Traffic Manager den Endpunkt, und die Load-Balancing-Methode berücksichtigt ihn beim Verwalten von Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="630c6-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="630c6-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="630c6-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="630c6-137">Gibt das Traffic Manager-Profilobjekt an, für das der Endpunkt geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="630c6-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="630c6-138">-Typ</span><span class="sxs-lookup"><span data-stu-id="630c6-138">-Type</span></span>
<span data-ttu-id="630c6-139">Gibt den Typ des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="630c6-140">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="630c6-140">Valid values are:</span></span> 

- <span data-ttu-id="630c6-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="630c6-141">CloudService</span></span>
- <span data-ttu-id="630c6-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="630c6-142">AzureWebsite</span></span>
- <span data-ttu-id="630c6-143">Trafficmanager</span><span class="sxs-lookup"><span data-stu-id="630c6-143">TrafficManager</span></span>

- <span data-ttu-id="630c6-144">Alle</span><span class="sxs-lookup"><span data-stu-id="630c6-144">Any</span></span> 

<span data-ttu-id="630c6-145">Wenn mehr als ein AzureWebsite-Endpunkt vorhanden ist, müssen sich die Endpunkte in unterschiedlichen Rechenzentren befinden.</span><span class="sxs-lookup"><span data-stu-id="630c6-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="630c6-146">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="630c6-146">-Weight</span></span>
<span data-ttu-id="630c6-147">Gibt die Gewichtung des vom Cmdlet hinzugefügten Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="630c6-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="630c6-148">Der gültige Wertebereich für diesen Parameter ist \[ 1.000 \] .</span><span class="sxs-lookup"><span data-stu-id="630c6-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="630c6-149">Dieser Parameter wird nur für Roundrobin-Lastenausgleichsrichtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="630c6-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="630c6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630c6-150">CommonParameters</span></span>
<span data-ttu-id="630c6-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630c6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630c6-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630c6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630c6-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="630c6-153">INPUTS</span></span>

## <span data-ttu-id="630c6-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="630c6-154">OUTPUTS</span></span>

### <span data-ttu-id="630c6-155">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="630c6-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="630c6-156">Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt, das Informationen über das aktualisierte Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="630c6-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="630c6-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="630c6-157">NOTES</span></span>

## <span data-ttu-id="630c6-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="630c6-158">RELATED LINKS</span></span>

[<span data-ttu-id="630c6-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="630c6-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="630c6-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="630c6-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="630c6-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="630c6-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="630c6-162">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="630c6-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


