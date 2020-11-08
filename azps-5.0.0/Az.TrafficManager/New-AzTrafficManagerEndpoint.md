---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176519"
---
# <span data-ttu-id="ad85a-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ad85a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad85a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad85a-103">Erstellt einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="ad85a-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="ad85a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad85a-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad85a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad85a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad85a-106">Das Cmdlet **New-AzTrafficManagerEndpoint** erstellt einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="ad85a-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="ad85a-107">Dieses Cmdlet übergibt jeden neuen Endpunkt an den Traffic Manager-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ad85a-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="ad85a-108">Verwenden Sie das Add-AzTrafficManagerEndpointConfig-Cmdlet, um mehrere Endpunkte zu einem lokalen Traffic Manager-Profilobjekt hinzuzufügen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="ad85a-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="ad85a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad85a-109">EXAMPLES</span></span>

### <span data-ttu-id="ad85a-110">Beispiel 1: Erstellen eines externen Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="ad85a-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="ad85a-111">Dieser Befehl erstellt einen externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad85a-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ad85a-112">Beispiel 2: Erstellen eines Azure-Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="ad85a-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="ad85a-113">Dieser Befehl erstellt einen Azure-Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppen-ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad85a-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="ad85a-114">Der Azure-Endpunkt verweist auf die Azure Web App, deren Azure Resource Manager-ID durch den URI-Pfad in *TargetResourceId* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="ad85a-115">Der Befehl gibt keinen *EndpointLocation* -Parameter an, weil die Web App-Ressource den Speicherort bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ad85a-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="ad85a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad85a-116">PARAMETERS</span></span>

### <span data-ttu-id="ad85a-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="ad85a-117">-CustomHeader</span></span>
<span data-ttu-id="ad85a-118">Liste der benutzerdefinierten Headername-und Wert-Paare für Prüf Punkt Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad85a-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="ad85a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad85a-119">-DefaultProfile</span></span>
<span data-ttu-id="ad85a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad85a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad85a-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="ad85a-121">-EndpointLocation</span></span>
<span data-ttu-id="ad85a-122">Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad85a-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="ad85a-123">Dieser Parameter ist nur auf Endpunkte des ExternalEndpoints-oder NestedEndpoints-Typs anwendbar.</span><span class="sxs-lookup"><span data-stu-id="ad85a-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="ad85a-124">Sie müssen diesen Parameter angeben, wenn die Methode zur Datenverkehrs Weiterleitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="ad85a-125">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-125">Specify an Azure region name.</span></span>
<span data-ttu-id="ad85a-126">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="ad85a-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="ad85a-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="ad85a-127">-EndpointStatus</span></span>
<span data-ttu-id="ad85a-128">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="ad85a-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ad85a-129">Valid values are:</span></span> 

- <span data-ttu-id="ad85a-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ad85a-130">Enabled</span></span> 
- <span data-ttu-id="ad85a-131">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="ad85a-131">Disabled</span></span> 

<span data-ttu-id="ad85a-132">Wenn der Status aktiviert ist, wird der Endpunkt nach Endpunkt Integrität untersucht und in die Datenverkehrs Routingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="ad85a-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="ad85a-133">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="ad85a-133">-GeoMapping</span></span>
<span data-ttu-id="ad85a-134">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="ad85a-135">Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation des Traffic-Managers.</span><span class="sxs-lookup"><span data-stu-id="ad85a-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="ad85a-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad85a-136">-MinChildEndpoints</span></span>
<span data-ttu-id="ad85a-137">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-137">Specify an Azure region name.</span></span>
<span data-ttu-id="ad85a-138">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="ad85a-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="ad85a-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ad85a-139">-Name</span></span>
<span data-ttu-id="ad85a-140">Gibt den Namen des vom Cmdlet erstellten Traffic Manager-Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ad85a-141">-Priorität</span><span class="sxs-lookup"><span data-stu-id="ad85a-141">-Priority</span></span>
<span data-ttu-id="ad85a-142">Gibt die Priorität an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="ad85a-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ad85a-143">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority-Datenverkehrs Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ad85a-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="ad85a-144">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="ad85a-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ad85a-145">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="ad85a-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="ad85a-146">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ad85a-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="ad85a-147">Wenn Sie keine Prioritäten angeben, weist der Datenverkehrs-Manager den Endpunkten Standard Prioritätswerte zu, beginnend mit einem (1), in der Reihenfolge, in der das Profil die Endpunkte aufführt.</span><span class="sxs-lookup"><span data-stu-id="ad85a-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="ad85a-148">-Profilname</span><span class="sxs-lookup"><span data-stu-id="ad85a-148">-ProfileName</span></span>
<span data-ttu-id="ad85a-149">Gibt den Namen eines Traffic Manager-Profils an, dem dieses Cmdlet einen Endpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ad85a-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="ad85a-150">Verwenden Sie zum Abrufen eines Profils die New-AzTrafficManagerProfile-oder Get-AzTrafficManagerProfile-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ad85a-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="ad85a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad85a-151">-ResourceGroupName</span></span>
<span data-ttu-id="ad85a-152">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ad85a-153">Dieses Cmdlet erstellt einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ad85a-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ad85a-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="ad85a-154">-SubnetMapping</span></span>
<span data-ttu-id="ad85a-155">Die Liste der Adressbereiche oder Subnetze, die diesem Endpunkt zugeordnet sind, wenn die Datenverkehrs Routingmethode "Subnetz" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="ad85a-156">-Target</span><span class="sxs-lookup"><span data-stu-id="ad85a-156">-Target</span></span>
<span data-ttu-id="ad85a-157">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="ad85a-158">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="ad85a-159">Geben Sie diesen Parameter nur für den ExternalEndpoints-Endpunkttyp an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="ad85a-160">Geben Sie bei anderen Endpunkttypen stattdessen den *TargetResourceId* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="ad85a-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ad85a-161">-TargetResourceId</span></span>
<span data-ttu-id="ad85a-162">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="ad85a-163">Geben Sie diesen Parameter nur für die AzureEndpoints-und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="ad85a-164">Geben Sie für den ExternalEndpoints-Endpunkttyp stattdessen den *target* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ad85a-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="ad85a-165">-Typ</span><span class="sxs-lookup"><span data-stu-id="ad85a-165">-Type</span></span>
<span data-ttu-id="ad85a-166">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ad85a-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ad85a-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ad85a-167">Valid values are:</span></span> 

- <span data-ttu-id="ad85a-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad85a-168">AzureEndpoints</span></span>
- <span data-ttu-id="ad85a-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad85a-169">ExternalEndpoints</span></span>
- <span data-ttu-id="ad85a-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad85a-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="ad85a-171">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="ad85a-171">-Weight</span></span>
<span data-ttu-id="ad85a-172">Gibt die Gewichtung an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="ad85a-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ad85a-173">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="ad85a-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ad85a-174">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="ad85a-174">The default value is one (1).</span></span>
<span data-ttu-id="ad85a-175">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der gewichteten Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ad85a-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="ad85a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad85a-176">CommonParameters</span></span>
<span data-ttu-id="ad85a-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad85a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad85a-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad85a-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad85a-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad85a-179">INPUTS</span></span>

### <span data-ttu-id="ad85a-180">Keine</span><span class="sxs-lookup"><span data-stu-id="ad85a-180">None</span></span>

## <span data-ttu-id="ad85a-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad85a-181">OUTPUTS</span></span>

### <span data-ttu-id="ad85a-182">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ad85a-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad85a-183">NOTES</span></span>

## <span data-ttu-id="ad85a-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad85a-184">RELATED LINKS</span></span>

[<span data-ttu-id="ad85a-185">Deaktivieren-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad85a-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad85a-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad85a-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad85a-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ad85a-189">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad85a-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="ad85a-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad85a-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad85a-191">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad85a-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


