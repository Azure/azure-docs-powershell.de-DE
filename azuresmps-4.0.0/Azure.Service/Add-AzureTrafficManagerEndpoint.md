---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006582"
---
# <span data-ttu-id="5ec8b-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ec8b-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5ec8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ec8b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec8b-103">Fügt einen Endpunkt zu einem Traffic Manager-Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="5ec8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ec8b-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ec8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ec8b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec8b-106">Mit dem Cmdlet **Add-AzureTrafficManagerEndpoint** wird ein Endpunkt zu einem Microsoft Azure Traffic Manager-Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5ec8b-107">Nachdem Sie einen Endpunkt hinzugefügt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".</span><span class="sxs-lookup"><span data-stu-id="5ec8b-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5ec8b-108">Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="5ec8b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ec8b-109">EXAMPLES</span></span>

### <span data-ttu-id="5ec8b-110">Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="5ec8b-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="5ec8b-111">Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="5ec8b-112">Mit dem zweiten Befehl wird ein Endpunkt zu Traffic Manager-Profil hinzugefügt, das in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="5ec8b-113">Der Endpunkt hat den Domänennamen Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="5ec8b-114">Der Befehl gibt auch an, ob er aktiviert ist und welchen Typ er hat.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="5ec8b-115">Der Befehl übergibt das Profilobjekt an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="5ec8b-116">Beispiel 2: Hinzufügen eines Endpunkts mit einer angegebenen Position und Gewichtung</span><span class="sxs-lookup"><span data-stu-id="5ec8b-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="5ec8b-117">Mit diesem Befehl wird ein Endpunkt zu einem Traffic Manager-Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="5ec8b-118">Der Endpunkt hat den Domänennamen Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="5ec8b-119">Der Befehl gibt auch an, ob er aktiviert ist und welchen Typ er hat.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="5ec8b-120">Mit dem Befehl werden auch die Gewichtung und die Position für den Endpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="5ec8b-121">Der Befehl übergibt das Profilobjekt an **AzureTrafficManagerProfile** , um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="5ec8b-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ec8b-122">PARAMETERS</span></span>

### <span data-ttu-id="5ec8b-123">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="5ec8b-123">-DomainName</span></span>
<span data-ttu-id="5ec8b-124">Gibt den Domänennamen des hinzuzufügenden Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="5ec8b-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="5ec8b-125">-Location</span></span>
<span data-ttu-id="5ec8b-126">Gibt den Speicherort des vom Cmdlet hinzugefügten Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="5ec8b-127">Dies muss eine Azure-Position sein.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-127">This must be an Azure location.</span></span>

<span data-ttu-id="5ec8b-128">Dieser Parameter muss einen Wert für Endpunkte des Typs "Any" oder des Typs "Trafficmanager" in einem Profil enthalten, bei dem die Load Balancing-Methode auf "Leistung" festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="5ec8b-129">Mögliche Werte sind die Namen der Azure-Region, wie unter aufgeführt https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="5ec8b-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="5ec8b-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="5ec8b-130">-MinChildEndpoints</span></span>
<span data-ttu-id="5ec8b-131">Gibt die Mindestanzahl von Endpunkten an, die das verschachtelte Profil Online haben muss, damit dieser Endpunkt als Online betrachtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="5ec8b-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ec8b-132">-Profile</span></span>
<span data-ttu-id="5ec8b-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5ec8b-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ec8b-135">-Status</span><span class="sxs-lookup"><span data-stu-id="5ec8b-135">-Status</span></span>
<span data-ttu-id="5ec8b-136">Gibt den Status des Überwachungs Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="5ec8b-137">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5ec8b-137">Valid values are:</span></span> 

- <span data-ttu-id="5ec8b-138">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5ec8b-138">Enabled</span></span>
- <span data-ttu-id="5ec8b-139">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="5ec8b-139">Disabled</span></span>

<span data-ttu-id="5ec8b-140">Wenn Sie den Wert enabled angeben, überwacht Traffic Manager den Endpunkt, und die Load-Balancing-Methode berücksichtigt ihn beim Verwalten von Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="5ec8b-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5ec8b-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="5ec8b-142">Gibt das Traffic Manager-Profilobjekt an, dem der Endpunkt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="5ec8b-143">-Typ</span><span class="sxs-lookup"><span data-stu-id="5ec8b-143">-Type</span></span>
<span data-ttu-id="5ec8b-144">Gibt den Typ des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="5ec8b-145">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5ec8b-145">Valid values are:</span></span> 

- <span data-ttu-id="5ec8b-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="5ec8b-146">CloudService</span></span>
- <span data-ttu-id="5ec8b-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5ec8b-147">AzureWebsite</span></span>
- <span data-ttu-id="5ec8b-148">Trafficmanager</span><span class="sxs-lookup"><span data-stu-id="5ec8b-148">TrafficManager</span></span>

- <span data-ttu-id="5ec8b-149">Alle</span><span class="sxs-lookup"><span data-stu-id="5ec8b-149">Any</span></span> 

<span data-ttu-id="5ec8b-150">Wenn mehr als ein AzureWebsite-Endpunkt vorhanden ist, müssen sich die Endpunkte in unterschiedlichen Rechenzentren befinden.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="5ec8b-151">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="5ec8b-151">-Weight</span></span>
<span data-ttu-id="5ec8b-152">Gibt die Gewichtung des vom Cmdlet hinzugefügten Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="5ec8b-153">Der gültige Wertebereich für diesen Parameter ist \[ 1.000 \] .</span><span class="sxs-lookup"><span data-stu-id="5ec8b-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="5ec8b-154">Dieser Parameter wird nur für Roundrobin-Lastenausgleichsrichtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="5ec8b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec8b-155">CommonParameters</span></span>
<span data-ttu-id="5ec8b-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec8b-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec8b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec8b-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ec8b-158">INPUTS</span></span>

## <span data-ttu-id="5ec8b-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ec8b-159">OUTPUTS</span></span>

### <span data-ttu-id="5ec8b-160">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="5ec8b-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="5ec8b-161">Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt, das Informationen über das aktualisierte Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="5ec8b-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="5ec8b-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ec8b-162">NOTES</span></span>

## <span data-ttu-id="5ec8b-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ec8b-163">RELATED LINKS</span></span>

[<span data-ttu-id="5ec8b-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ec8b-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="5ec8b-165">Satz-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ec8b-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="5ec8b-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5ec8b-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="5ec8b-167">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5ec8b-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


