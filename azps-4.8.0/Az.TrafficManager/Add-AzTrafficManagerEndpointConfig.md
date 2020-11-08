---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007650"
---
# <span data-ttu-id="2c09b-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2c09b-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="2c09b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c09b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c09b-103">Fügt einen Endpunkt zu einem lokalen Traffic Manager-Profilobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2c09b-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="2c09b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c09b-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c09b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c09b-105">DESCRIPTION</span></span>
<span data-ttu-id="2c09b-106">Mit dem Cmdlet **Add-AzTrafficManagerEndpointConfig** wird ein Endpunkt zu einem lokalen Azure Traffic Manager-Profilobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2c09b-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2c09b-107">Sie können ein Profil mithilfe der Cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="2c09b-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="2c09b-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="2c09b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2c09b-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="2c09b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2c09b-110">Verwenden Sie das New-AzTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu erstellen und die Änderung in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2c09b-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="2c09b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c09b-111">EXAMPLES</span></span>

### <span data-ttu-id="2c09b-112">Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="2c09b-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2c09b-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="2c09b-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2c09b-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="2c09b-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="2c09b-115">Der zweite Befehl fügt dem in $TrafficManagerProfile gespeicherten Profil einen Endpunkt mit dem Namen "Contoso" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2c09b-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2c09b-116">Der Befehl enthält Konfigurationsdaten für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2c09b-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="2c09b-117">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="2c09b-117">This command changes only the local object.</span></span>

<span data-ttu-id="2c09b-118">Der endgültige Befehl aktualisiert das Traffic Manager-Profil in Azure so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c09b-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2c09b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c09b-119">PARAMETERS</span></span>

### <span data-ttu-id="2c09b-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="2c09b-120">-CustomHeader</span></span>
<span data-ttu-id="2c09b-121">Liste der benutzerdefinierten Headername-und Wert-Paare für Prüf Punkt Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c09b-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="2c09b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-122">-DefaultProfile</span></span>
<span data-ttu-id="2c09b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c09b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c09b-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="2c09b-124">-EndpointLocation</span></span>
<span data-ttu-id="2c09b-125">Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c09b-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="2c09b-126">Dieser Parameter ist nur für Endpunkte der ExternalEndpoints oder des NestedEndpoints-Typs anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2c09b-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="2c09b-127">Sie müssen diesen Parameter angeben, wenn die Methode zur Datenverkehrs Weiterleitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c09b-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="2c09b-128">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-128">Specify an Azure region name.</span></span>
<span data-ttu-id="2c09b-129">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="2c09b-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="2c09b-130">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2c09b-130">-EndpointName</span></span>
<span data-ttu-id="2c09b-131">Gibt den Namen des vom Cmdlet hinzugefügten Traffic Manager-Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="2c09b-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="2c09b-132">-EndpointStatus</span></span>
<span data-ttu-id="2c09b-133">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="2c09b-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2c09b-134">Valid values are:</span></span> 

- <span data-ttu-id="2c09b-135">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2c09b-135">Enabled</span></span> 
- <span data-ttu-id="2c09b-136">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="2c09b-136">Disabled</span></span> 

<span data-ttu-id="2c09b-137">Wenn der Status aktiviert ist, wird der Endpunkt nach Endpunkt Integrität untersucht und in die Datenverkehrs Routingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="2c09b-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="2c09b-138">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="2c09b-138">-GeoMapping</span></span>
<span data-ttu-id="2c09b-139">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c09b-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="2c09b-140">Eine [vollständige Liste der akzeptierten Werte](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)finden Sie in der Dokumentation des Traffic-Managers.</span><span class="sxs-lookup"><span data-stu-id="2c09b-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="2c09b-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="2c09b-141">-MinChildEndpoints</span></span>
<span data-ttu-id="2c09b-142">Die Mindestanzahl von Endpunkten, die im untergeordneten Profil verfügbar sein müssen, damit der geschachtelte Endpunkt im übergeordneten Profil als verfügbar betrachtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c09b-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="2c09b-143">Gilt nur für den Endpunkt des Typs "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="2c09b-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="2c09b-144">-Priorität</span><span class="sxs-lookup"><span data-stu-id="2c09b-144">-Priority</span></span>
<span data-ttu-id="2c09b-145">Gibt die Priorität an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="2c09b-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="2c09b-146">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority-Datenverkehrs Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2c09b-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="2c09b-147">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="2c09b-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="2c09b-148">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="2c09b-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="2c09b-149">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2c09b-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="2c09b-150">Wenn Sie keine Prioritäten angeben, weist der Datenverkehrs-Manager den Endpunkten Standard Prioritätswerte zu, beginnend mit einem (1), in der Reihenfolge, in der das Profil die Endpunkte aufführt.</span><span class="sxs-lookup"><span data-stu-id="2c09b-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="2c09b-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="2c09b-151">-SubnetMapping</span></span>
<span data-ttu-id="2c09b-152">Die Liste der Adressbereiche oder Subnetze, die diesem Endpunkt zugeordnet sind, wenn die Datenverkehrs Routingmethode "Subnetz" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c09b-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="2c09b-153">-Target</span><span class="sxs-lookup"><span data-stu-id="2c09b-153">-Target</span></span>
<span data-ttu-id="2c09b-154">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="2c09b-155">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c09b-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="2c09b-156">Geben Sie diesen Parameter nur für den ExternalEndpoints-Endpunkttyp an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="2c09b-157">Geben Sie bei anderen Endpunkttypen stattdessen den *TargetResourceId* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="2c09b-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2c09b-158">-TargetResourceId</span></span>
<span data-ttu-id="2c09b-159">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="2c09b-160">Geben Sie diesen Parameter nur für die AzureEndpoints-und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="2c09b-161">Geben Sie für den ExternalEndpoints-Endpunkttyp stattdessen den *target* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="2c09b-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="2c09b-163">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2c09b-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2c09b-164">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c09b-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2c09b-165">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c09b-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2c09b-166">-Typ</span><span class="sxs-lookup"><span data-stu-id="2c09b-166">-Type</span></span>
<span data-ttu-id="2c09b-167">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Azure Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2c09b-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2c09b-168">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2c09b-168">Valid values are:</span></span> 

- <span data-ttu-id="2c09b-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2c09b-169">AzureEndpoints</span></span>
- <span data-ttu-id="2c09b-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2c09b-170">ExternalEndpoints</span></span>
- <span data-ttu-id="2c09b-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2c09b-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="2c09b-172">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="2c09b-172">-Weight</span></span>
<span data-ttu-id="2c09b-173">Gibt die Gewichtung an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="2c09b-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="2c09b-174">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="2c09b-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="2c09b-175">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="2c09b-175">The default value is one (1).</span></span>
<span data-ttu-id="2c09b-176">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der gewichteten Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2c09b-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="2c09b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c09b-177">CommonParameters</span></span>
<span data-ttu-id="2c09b-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c09b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c09b-179">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c09b-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c09b-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c09b-180">INPUTS</span></span>

### <span data-ttu-id="2c09b-181">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2c09b-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c09b-182">OUTPUTS</span></span>

### <span data-ttu-id="2c09b-183">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2c09b-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c09b-184">NOTES</span></span>

## <span data-ttu-id="2c09b-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c09b-185">RELATED LINKS</span></span>

[<span data-ttu-id="2c09b-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2c09b-187">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c09b-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2c09b-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2c09b-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2c09b-189">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2c09b-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


