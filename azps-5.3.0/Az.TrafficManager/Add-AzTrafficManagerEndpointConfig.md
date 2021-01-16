---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375821"
---
# <span data-ttu-id="c1513-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c1513-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="c1513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1513-102">SYNOPSIS</span></span>
<span data-ttu-id="c1513-103">Fügt einem lokalen Traffic -Manager-Profilobjekt einen Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1513-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="c1513-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1513-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1513-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1513-105">DESCRIPTION</span></span>
<span data-ttu-id="c1513-106">Das **Cmdlet "Add-AzTrafficManagerEndpointConfig"** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1513-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="c1513-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1513-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="c1513-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1513-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="c1513-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="c1513-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="c1513-110">Verwenden Sie zum Erstellen eines Endpunkts und Zum Commit der Änderung in einem einzigen Vorgang das New-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1513-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="c1513-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1513-111">EXAMPLES</span></span>

### <span data-ttu-id="c1513-112">Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="c1513-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="c1513-113">Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ab.</span><span class="sxs-lookup"><span data-stu-id="c1513-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="c1513-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="c1513-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="c1513-115">Mit dem zweiten Befehl wird dem in der Datei gespeicherten Profil ein Endpunkt namens "contoso" $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c1513-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="c1513-116">Der Befehl enthält Konfigurationsdaten für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c1513-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="c1513-117">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="c1513-117">This command changes only the local object.</span></span>

<span data-ttu-id="c1513-118">Der letzte Befehl aktualisiert das Datenverkehrs-Manager-Profil in Azure so, dass es mit dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c1513-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="c1513-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1513-119">PARAMETERS</span></span>

### <span data-ttu-id="c1513-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="c1513-120">-CustomHeader</span></span>
<span data-ttu-id="c1513-121">Liste von benutzerdefinierten Headernamen- und Wertpaaren für Probeanforderungen.</span><span class="sxs-lookup"><span data-stu-id="c1513-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-122">-DefaultProfile</span></span>
<span data-ttu-id="c1513-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1513-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1513-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="c1513-124">-EndpointLocation</span></span>
<span data-ttu-id="c1513-125">Gibt die Position des Endpunkts an, der in der Datenverkehrsroutingmethode "Performance" verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1513-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="c1513-126">Dieser Parameter gilt nur für Endpunkte des Typs "ExternalEndpoints" oder "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="c1513-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="c1513-127">Sie müssen diesen Parameter angeben, wenn die Datenverkehrsroutingmethode für die Leistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1513-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="c1513-128">Geben Sie einen Namen für die Region Azure an.</span><span class="sxs-lookup"><span data-stu-id="c1513-128">Specify an Azure region name.</span></span>
<span data-ttu-id="c1513-129">Eine vollständige Liste der Azure-Regionen finden Sie unter "Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="c1513-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="c1513-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c1513-130">-EndpointName</span></span>
<span data-ttu-id="c1513-131">Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c1513-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c1513-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="c1513-132">-EndpointStatus</span></span>
<span data-ttu-id="c1513-133">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c1513-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="c1513-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c1513-134">Valid values are:</span></span> 

- <span data-ttu-id="c1513-135">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="c1513-135">Enabled</span></span> 
- <span data-ttu-id="c1513-136">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="c1513-136">Disabled</span></span> 

<span data-ttu-id="c1513-137">Wenn der Status "Aktiviert" ist, wird der Endpunkt auf den Endpunktstatus untersucht und in die Datenverkehrsroutingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="c1513-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="c1513-138">-GeoMapping</span></span>
<span data-ttu-id="c1513-139">Die Liste der Regionen, die bei Verwendung der Routingmethode "Geografischer" Datenverkehr diesem Endpunkt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c1513-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="c1513-140">Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation [zur Verkehrsverwaltung.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="c1513-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="c1513-141">-MinChildEndpoints</span></span>
<span data-ttu-id="c1513-142">Die minimale Anzahl von Endpunkten, die im untergeordneten Profil verfügbar sein müssen, damit der geschachtelte Endpunkt im übergeordneten Profil als verfügbar betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="c1513-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="c1513-143">Gilt nur für Endpunkte vom Typ "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="c1513-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-144">-Priority</span><span class="sxs-lookup"><span data-stu-id="c1513-144">-Priority</span></span>
<span data-ttu-id="c1513-145">Gibt die Priorität an, die der Verkehrsmanager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="c1513-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c1513-146">Dieser Parameter wird nur verwendet, wenn das Datenverkehrs-Manager-Profil mit der "for Priority Traffic-Routing"-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="c1513-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="c1513-147">Gültige Werte sind ganze Zahlen zwischen 1 und 1000.</span><span class="sxs-lookup"><span data-stu-id="c1513-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c1513-148">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="c1513-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="c1513-149">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und es können keine zwei Endpunkte denselben Prioritätswert verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1513-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="c1513-150">Wenn Sie keine Prioritäten angeben, weist der Verkehrs-Manager den Endpunkten Standardwerte zu, beginnend mit einem (1), in der Reihenfolge, in der die Endpunkte im Profil aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c1513-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="c1513-151">-SubnetMapping</span></span>
<span data-ttu-id="c1513-152">Die Liste der Adressbereiche oder Subnetze, die bei Verwendung der Routingmethode für den Datenverkehr im Subnetz diesem Endpunkt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c1513-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-153">-Target</span><span class="sxs-lookup"><span data-stu-id="c1513-153">-Target</span></span>
<span data-ttu-id="c1513-154">Gibt den vollqualifizierten Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c1513-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="c1513-155">Der Datenverkehrs-Manager gibt diesen Wert in den DNS-Antworten zurück, wenn er den Datenverkehr an diesen Endpunkt weitergibt.</span><span class="sxs-lookup"><span data-stu-id="c1513-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="c1513-156">Geben Sie diesen Parameter nur für den Endpunkttyp "ExternalEndpoints" an.</span><span class="sxs-lookup"><span data-stu-id="c1513-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="c1513-157">Geben Sie für andere Endpunkttypen stattdessen den *Parameter "TargetResourceId"* an.</span><span class="sxs-lookup"><span data-stu-id="c1513-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="c1513-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c1513-158">-TargetResourceId</span></span>
<span data-ttu-id="c1513-159">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="c1513-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="c1513-160">Geben Sie diesen Parameter nur für die Endpunkttypen "AzureEndpoints" und "NestedEndpoints" an.</span><span class="sxs-lookup"><span data-stu-id="c1513-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="c1513-161">Geben Sie für den Endpunkttyp "ExternalEndpoints" stattdessen den *Parameter "Target"* an.</span><span class="sxs-lookup"><span data-stu-id="c1513-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="c1513-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="c1513-163">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c1513-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="c1513-164">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="c1513-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c1513-165">Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1513-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-166">-Type</span><span class="sxs-lookup"><span data-stu-id="c1513-166">-Type</span></span>
<span data-ttu-id="c1513-167">Gibt den Endpunkttyp an, den dieses Cmdlet dem Azure Traffic Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c1513-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c1513-168">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c1513-168">Valid values are:</span></span> 

- <span data-ttu-id="c1513-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c1513-169">AzureEndpoints</span></span>
- <span data-ttu-id="c1513-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c1513-170">ExternalEndpoints</span></span>
- <span data-ttu-id="c1513-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c1513-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="c1513-172">-Weight</span></span>
<span data-ttu-id="c1513-173">Gibt die Gewichtung an, die der Verkehrsmanager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="c1513-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="c1513-174">Gültige Werte sind ganze Zahlen zwischen 1 und 1000.</span><span class="sxs-lookup"><span data-stu-id="c1513-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="c1513-175">Der Standardwert ist "1".</span><span class="sxs-lookup"><span data-stu-id="c1513-175">The default value is one (1).</span></span>
<span data-ttu-id="c1513-176">Dieser Parameter wird nur verwendet, wenn das Datenverkehrs-Manager-Profil mit der Methode "Weighted traffic-routing" konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="c1513-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1513-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1513-177">CommonParameters</span></span>
<span data-ttu-id="c1513-178">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1513-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1513-179">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1513-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1513-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1513-180">INPUTS</span></span>

### <span data-ttu-id="c1513-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c1513-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1513-182">OUTPUTS</span></span>

### <span data-ttu-id="c1513-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c1513-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1513-184">NOTES</span></span>

## <span data-ttu-id="c1513-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1513-185">RELATED LINKS</span></span>

[<span data-ttu-id="c1513-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c1513-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1513-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c1513-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c1513-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="c1513-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1513-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


