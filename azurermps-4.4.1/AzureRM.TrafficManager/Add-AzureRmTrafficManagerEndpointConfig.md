---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477129"
---
# <span data-ttu-id="922b9-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="922b9-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="922b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="922b9-102">SYNOPSIS</span></span>
<span data-ttu-id="922b9-103">Fügt einen Endpunkt zu einem lokalen Traffic Manager-Profilobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="922b9-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="922b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="922b9-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="922b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="922b9-105">DESCRIPTION</span></span>
<span data-ttu-id="922b9-106">Mit dem Cmdlet **Add-AzureRmTrafficManagerEndpointConfig** wird ein Endpunkt zu einem lokalen Azure Traffic Manager-Profilobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="922b9-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="922b9-107">Sie können ein Profil mithilfe der Cmdlets New-AzureRmTrafficManagerProfile oder Get-AzureRmTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="922b9-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="922b9-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="922b9-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="922b9-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="922b9-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="922b9-110">Verwenden Sie das New-AzureRmTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu erstellen und die Änderung in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="922b9-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="922b9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="922b9-111">EXAMPLES</span></span>

### <span data-ttu-id="922b9-112">Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="922b9-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="922b9-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzureRmTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="922b9-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="922b9-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="922b9-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="922b9-115">Der zweite Befehl fügt dem in $TrafficManagerProfile gespeicherten Profil einen Endpunkt mit dem Namen "Contoso" hinzu.</span><span class="sxs-lookup"><span data-stu-id="922b9-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="922b9-116">Der Befehl enthält Konfigurationsdaten für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="922b9-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="922b9-117">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="922b9-117">This command changes only the local object.</span></span>

<span data-ttu-id="922b9-118">Der endgültige Befehl aktualisiert das Traffic Manager-Profil in Azure so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="922b9-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="922b9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="922b9-119">PARAMETERS</span></span>

### <span data-ttu-id="922b9-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="922b9-120">-EndpointLocation</span></span>
<span data-ttu-id="922b9-121">Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="922b9-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="922b9-122">Dieser Parameter ist nur für Endpunkte der ExternalEndpoints oder des NestedEndpoints-Typs anwendbar.</span><span class="sxs-lookup"><span data-stu-id="922b9-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="922b9-123">Sie müssen diesen Parameter angeben, wenn die Methode zur Datenverkehrs Weiterleitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="922b9-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="922b9-124">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="922b9-124">Specify an Azure region name.</span></span>
<span data-ttu-id="922b9-125">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="922b9-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="922b9-126">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="922b9-126">-EndpointName</span></span>
<span data-ttu-id="922b9-127">Gibt den Namen des vom Cmdlet hinzugefügten Traffic Manager-Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="922b9-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="922b9-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="922b9-128">-EndpointStatus</span></span>
<span data-ttu-id="922b9-129">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="922b9-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="922b9-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="922b9-130">Valid values are:</span></span> 

- <span data-ttu-id="922b9-131">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="922b9-131">Enabled</span></span> 
- <span data-ttu-id="922b9-132">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="922b9-132">Disabled</span></span> 

<span data-ttu-id="922b9-133">Wenn der Status aktiviert ist, wird der Endpunkt nach Endpunkt Integrität untersucht und in die Datenverkehrs Routingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="922b9-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="922b9-134">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="922b9-134">-GeoMapping</span></span>
<span data-ttu-id="922b9-135">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="922b9-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="922b9-136">Eine [vollständige Liste der akzeptierten Werte](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)finden Sie in der Dokumentation des Traffic-Managers.</span><span class="sxs-lookup"><span data-stu-id="922b9-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="922b9-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="922b9-137">-MinChildEndpoints</span></span>
<span data-ttu-id="922b9-138">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="922b9-138">Specify an Azure region name.</span></span>
<span data-ttu-id="922b9-139">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="922b9-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="922b9-140">-Priorität</span><span class="sxs-lookup"><span data-stu-id="922b9-140">-Priority</span></span>
<span data-ttu-id="922b9-141">Gibt die Priorität an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="922b9-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="922b9-142">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority-Datenverkehrs Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="922b9-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="922b9-143">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="922b9-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="922b9-144">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="922b9-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="922b9-145">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="922b9-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="922b9-146">Wenn Sie keine Prioritäten angeben, weist der Datenverkehrs-Manager den Endpunkten Standard Prioritätswerte zu, beginnend mit einem (1), in der Reihenfolge, in der das Profil die Endpunkte aufführt.</span><span class="sxs-lookup"><span data-stu-id="922b9-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="922b9-147">-Target</span><span class="sxs-lookup"><span data-stu-id="922b9-147">-Target</span></span>
<span data-ttu-id="922b9-148">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="922b9-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="922b9-149">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="922b9-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="922b9-150">Geben Sie diesen Parameter nur für den ExternalEndpoints-Endpunkttyp an.</span><span class="sxs-lookup"><span data-stu-id="922b9-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="922b9-151">Geben Sie bei anderen Endpunkttypen stattdessen den *TargetResourceId* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="922b9-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="922b9-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="922b9-152">-TargetResourceId</span></span>
<span data-ttu-id="922b9-153">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="922b9-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="922b9-154">Geben Sie diesen Parameter nur für die AzureEndpoints-und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="922b9-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="922b9-155">Geben Sie für den ExternalEndpoints-Endpunkttyp stattdessen den *target* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="922b9-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="922b9-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="922b9-157">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="922b9-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="922b9-158">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="922b9-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="922b9-159">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="922b9-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="922b9-160">-Typ</span><span class="sxs-lookup"><span data-stu-id="922b9-160">-Type</span></span>
<span data-ttu-id="922b9-161">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Azure Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="922b9-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="922b9-162">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="922b9-162">Valid values are:</span></span> 

- <span data-ttu-id="922b9-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="922b9-163">AzureEndpoints</span></span>
- <span data-ttu-id="922b9-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="922b9-164">ExternalEndpoints</span></span>
- <span data-ttu-id="922b9-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="922b9-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="922b9-166">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="922b9-166">-Weight</span></span>
<span data-ttu-id="922b9-167">Gibt die Gewichtung an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="922b9-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="922b9-168">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="922b9-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="922b9-169">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="922b9-169">The default value is one (1).</span></span>
<span data-ttu-id="922b9-170">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der gewichteten Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="922b9-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="922b9-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-171">-DefaultProfile</span></span>
<span data-ttu-id="922b9-172">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="922b9-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922b9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922b9-173">CommonParameters</span></span>
<span data-ttu-id="922b9-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922b9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922b9-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922b9-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922b9-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="922b9-176">INPUTS</span></span>

### <span data-ttu-id="922b9-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="922b9-178">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922b9-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="922b9-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="922b9-179">OUTPUTS</span></span>

### <span data-ttu-id="922b9-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="922b9-181">Dieses Cmdlet gibt ein geändertes **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="922b9-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="922b9-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="922b9-182">NOTES</span></span>

## <span data-ttu-id="922b9-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="922b9-183">RELATED LINKS</span></span>

[<span data-ttu-id="922b9-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="922b9-185">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="922b9-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="922b9-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="922b9-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="922b9-187">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="922b9-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


