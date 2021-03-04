---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936523"
---
# <span data-ttu-id="82478-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="82478-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="82478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82478-102">SYNOPSIS</span></span>
<span data-ttu-id="82478-103">Fügt einem lokalen Traffic Manager-Profilobjekt einen Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="82478-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="82478-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82478-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82478-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82478-105">DESCRIPTION</span></span>
<span data-ttu-id="82478-106">Das **Add-AzTrafficManagerEndpointConfig-Cmdlet** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="82478-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="82478-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="82478-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="82478-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="82478-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="82478-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="82478-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="82478-110">Um einen Endpunkt zu erstellen und die Änderung in einem einzigen Vorgang zu commiten, verwenden Sie New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82478-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="82478-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82478-111">EXAMPLES</span></span>

### <span data-ttu-id="82478-112">Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="82478-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="82478-113">Der erste Befehl ruft mithilfe des **Get-AzTrafficManagerProfile-Cmdlets ein Azure Traffic Manager-Profil** ab.</span><span class="sxs-lookup"><span data-stu-id="82478-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="82478-114">Mit dem Befehl wird das lokale Profil in der $TrafficManagerProfile gespeichert.</span><span class="sxs-lookup"><span data-stu-id="82478-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="82478-115">Mit dem zweiten Befehl wird dem profil gespeicherten Profil ein Endpunkt namens contoso $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="82478-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="82478-116">Der Befehl enthält Konfigurationsdaten für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="82478-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="82478-117">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="82478-117">This command changes only the local object.</span></span>

<span data-ttu-id="82478-118">Mit dem letzten Befehl wird das Traffic Manager-Profil in Azure aktualisiert, um dem lokalen Wert in azure $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="82478-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="82478-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82478-119">PARAMETERS</span></span>

### <span data-ttu-id="82478-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="82478-120">-CustomHeader</span></span>
<span data-ttu-id="82478-121">Liste der benutzerdefinierten Headernamen und Wertpaare für Prüfanforderungen.</span><span class="sxs-lookup"><span data-stu-id="82478-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="82478-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82478-122">-DefaultProfile</span></span>
<span data-ttu-id="82478-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82478-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82478-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="82478-124">-EndpointLocation</span></span>
<span data-ttu-id="82478-125">Gibt den Speicherort des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82478-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="82478-126">Dieser Parameter gilt nur für Endpunkte des Typs ExternalEndpoints oder des Typs "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="82478-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="82478-127">Sie müssen diesen Parameter angeben, wenn die Performance Traffic-Routing-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82478-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="82478-128">Geben Sie einen Azure-Regionnamen an.</span><span class="sxs-lookup"><span data-stu-id="82478-128">Specify an Azure region name.</span></span>
<span data-ttu-id="82478-129">Eine vollständige Liste der Azure-Regionen finden Sie unter Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="82478-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="82478-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="82478-130">-EndpointName</span></span>
<span data-ttu-id="82478-131">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="82478-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="82478-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="82478-132">-EndpointStatus</span></span>
<span data-ttu-id="82478-133">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="82478-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="82478-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="82478-134">Valid values are:</span></span> 

- <span data-ttu-id="82478-135">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="82478-135">Enabled</span></span> 
- <span data-ttu-id="82478-136">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="82478-136">Disabled</span></span> 

<span data-ttu-id="82478-137">Wenn der Status Aktiviert ist, wird der Endpunkt auf den Endpunktstatus untersucht und in die Datenverkehrsroutingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="82478-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="82478-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="82478-138">-GeoMapping</span></span>
<span data-ttu-id="82478-139">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die Routingmethode "Geografischer" Datenverkehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82478-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="82478-140">Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation zu Traffic [Manager.](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="82478-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="82478-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="82478-141">-MinChildEndpoints</span></span>
<span data-ttu-id="82478-142">Die Mindestanzahl von Endpunkten, die im untergeordneten Profil verfügbar sein müssen, damit der geschachtelte Endpunkt im übergeordneten Profil als verfügbar betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="82478-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="82478-143">Gilt nur für Endpunkte vom Typ "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="82478-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="82478-144">-Priorität</span><span class="sxs-lookup"><span data-stu-id="82478-144">-Priority</span></span>
<span data-ttu-id="82478-145">Gibt die Priorität an, die Traffic Manager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="82478-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="82478-146">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="82478-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="82478-147">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="82478-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="82478-148">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="82478-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="82478-149">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="82478-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="82478-150">Wenn Sie keine Prioritäten angeben, weist Traffic Manager den Endpunkten Standardwerte zu, beginnend mit einem (1), in der Reihenfolge, in der die Endpunkte im Profil aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="82478-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="82478-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="82478-151">-SubnetMapping</span></span>
<span data-ttu-id="82478-152">Die Liste der Adressbereiche oder Subnetze, die diesem Endpunkt zugeordnet sind, wenn die Routingmethode "Subnetz" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82478-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="82478-153">-Target</span><span class="sxs-lookup"><span data-stu-id="82478-153">-Target</span></span>
<span data-ttu-id="82478-154">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="82478-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="82478-155">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="82478-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="82478-156">Geben Sie diesen Parameter nur für den Endpunkttyp ExternalEndpoints an.</span><span class="sxs-lookup"><span data-stu-id="82478-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="82478-157">Geben Sie bei anderen Endpunkttypen stattdessen den *Parameter TargetResourceId* an.</span><span class="sxs-lookup"><span data-stu-id="82478-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="82478-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="82478-158">-TargetResourceId</span></span>
<span data-ttu-id="82478-159">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="82478-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="82478-160">Geben Sie diesen Parameter nur für die AzureEndpoints- und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="82478-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="82478-161">Geben Sie für den Endpunkttyp ExternalEndpoints stattdessen den *Parameter Target* an.</span><span class="sxs-lookup"><span data-stu-id="82478-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="82478-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="82478-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="82478-163">Gibt ein lokales **TrafficManagerProfile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="82478-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="82478-164">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="82478-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="82478-165">Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82478-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="82478-166">-Type</span><span class="sxs-lookup"><span data-stu-id="82478-166">-Type</span></span>
<span data-ttu-id="82478-167">Gibt den Endpunkttyp an, den dieses Cmdlet dem Azure Traffic Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="82478-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="82478-168">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="82478-168">Valid values are:</span></span> 

- <span data-ttu-id="82478-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="82478-169">AzureEndpoints</span></span>
- <span data-ttu-id="82478-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="82478-170">ExternalEndpoints</span></span>
- <span data-ttu-id="82478-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="82478-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="82478-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="82478-172">-Weight</span></span>
<span data-ttu-id="82478-173">Gibt die Gewichtung an, die Traffic Manager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="82478-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="82478-174">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="82478-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="82478-175">Der Standardwert ist ein Wert (1).</span><span class="sxs-lookup"><span data-stu-id="82478-175">The default value is one (1).</span></span>
<span data-ttu-id="82478-176">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der Methode "Gewichteter Datenverkehrsrouting" konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="82478-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="82478-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82478-177">CommonParameters</span></span>
<span data-ttu-id="82478-178">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82478-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82478-179">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82478-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82478-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82478-180">INPUTS</span></span>

### <span data-ttu-id="82478-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="82478-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="82478-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82478-182">OUTPUTS</span></span>

### <span data-ttu-id="82478-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="82478-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="82478-184">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82478-184">NOTES</span></span>

## <span data-ttu-id="82478-185">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82478-185">RELATED LINKS</span></span>

[<span data-ttu-id="82478-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="82478-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="82478-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="82478-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="82478-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="82478-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="82478-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="82478-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


