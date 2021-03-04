---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6d9ec806c1456f572991f7c72189c47abbe9ffe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936472"
---
# <span data-ttu-id="58976-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="58976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58976-102">SYNOPSIS</span></span>
<span data-ttu-id="58976-103">Erstellt einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="58976-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="58976-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58976-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58976-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58976-105">DESCRIPTION</span></span>
<span data-ttu-id="58976-106">Das **Cmdlet New-AzTrafficManagerEndpoint** erstellt einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="58976-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="58976-107">Mit diesem Cmdlet wird jeder neue Endpunkt an den Traffic Manager-Dienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="58976-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="58976-108">Um einem lokalen Traffic Manager-Profilobjekt mehrere Endpunkte hinzuzufügen und Änderungen in einem einzelnen Vorgang zu commiten, verwenden Sie das cmdlet Add-AzTrafficManagerEndpointConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58976-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="58976-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58976-109">EXAMPLES</span></span>

### <span data-ttu-id="58976-110">Beispiel 1: Erstellen eines externen Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="58976-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="58976-111">Mit diesem Befehl wird ein externer Endpunkt namens contoso im Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" erstellt.</span><span class="sxs-lookup"><span data-stu-id="58976-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="58976-112">Beispiel 2: Erstellen eines Azure-Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="58976-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="58976-113">Mit diesem Befehl wird ein Azure-Endpunkt namens contoso im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11 erstellt.</span><span class="sxs-lookup"><span data-stu-id="58976-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="58976-114">Der Azure-Endpunkt verweist auf die Azure Web App, deren Azure Resource Manager-ID vom URI-Pfad in *TargetResourceId angegeben wird.*</span><span class="sxs-lookup"><span data-stu-id="58976-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="58976-115">Der Befehl gibt den *Parameter EndpointLocation* nicht an, da die Web App-Ressource den Speicherort liefert.</span><span class="sxs-lookup"><span data-stu-id="58976-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="58976-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="58976-116">PARAMETERS</span></span>

### <span data-ttu-id="58976-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="58976-117">-CustomHeader</span></span>
<span data-ttu-id="58976-118">Liste der benutzerdefinierten Headernamen und Wertpaare für Prüfanforderungen.</span><span class="sxs-lookup"><span data-stu-id="58976-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="58976-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58976-119">-DefaultProfile</span></span>
<span data-ttu-id="58976-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58976-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58976-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="58976-121">-EndpointLocation</span></span>
<span data-ttu-id="58976-122">Gibt den Speicherort des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58976-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="58976-123">Dieser Parameter gilt nur für Endpunkte des Typs ExternalEndpoints oder NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="58976-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="58976-124">Sie müssen diesen Parameter angeben, wenn die Performance Traffic-Routing-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58976-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="58976-125">Geben Sie einen Azure-Regionnamen an.</span><span class="sxs-lookup"><span data-stu-id="58976-125">Specify an Azure region name.</span></span>
<span data-ttu-id="58976-126">Eine vollständige Liste der Azure-Regionen finden Sie unter Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="58976-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="58976-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="58976-127">-EndpointStatus</span></span>
<span data-ttu-id="58976-128">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="58976-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="58976-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="58976-129">Valid values are:</span></span> 

- <span data-ttu-id="58976-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="58976-130">Enabled</span></span> 
- <span data-ttu-id="58976-131">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="58976-131">Disabled</span></span> 

<span data-ttu-id="58976-132">Wenn der Status Aktiviert ist, wird der Endpunkt auf den Endpunktstatus untersucht und in die Datenverkehrsroutingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="58976-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="58976-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="58976-133">-GeoMapping</span></span>
<span data-ttu-id="58976-134">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die Routingmethode "Geografischer" Datenverkehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58976-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="58976-135">Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation zu Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="58976-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="58976-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="58976-136">-MinChildEndpoints</span></span>
<span data-ttu-id="58976-137">Geben Sie einen Azure-Regionnamen an.</span><span class="sxs-lookup"><span data-stu-id="58976-137">Specify an Azure region name.</span></span>
<span data-ttu-id="58976-138">Eine vollständige Liste der Azure-Regionen finden Sie unter Azure-Regionen http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="58976-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="58976-139">-Name</span><span class="sxs-lookup"><span data-stu-id="58976-139">-Name</span></span>
<span data-ttu-id="58976-140">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="58976-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="58976-141">-Priorität</span><span class="sxs-lookup"><span data-stu-id="58976-141">-Priority</span></span>
<span data-ttu-id="58976-142">Gibt die Priorität an, die Traffic Manager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="58976-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="58976-143">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="58976-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="58976-144">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="58976-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="58976-145">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="58976-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="58976-146">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="58976-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="58976-147">Wenn Sie keine Prioritäten angeben, weist Traffic Manager den Endpunkten Standardwerte zu, beginnend mit einem (1), in der Reihenfolge, in der die Endpunkte im Profil aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="58976-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="58976-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="58976-148">-ProfileName</span></span>
<span data-ttu-id="58976-149">Gibt den Namen eines Traffic Manager-Profils an, dem dieses Cmdlet einen Endpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="58976-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="58976-150">Verwenden Sie zum Abrufen eines Profils die New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile cmdlets.</span><span class="sxs-lookup"><span data-stu-id="58976-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="58976-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58976-151">-ResourceGroupName</span></span>
<span data-ttu-id="58976-152">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="58976-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="58976-153">Dieses Cmdlet erstellt einen Traffic Manager-Endpunkt in der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58976-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="58976-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="58976-154">-SubnetMapping</span></span>
<span data-ttu-id="58976-155">Die Liste der Adressbereiche oder Subnetze, die diesem Endpunkt zugeordnet sind, wenn die Routingmethode "Subnetz" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58976-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="58976-156">-Target</span><span class="sxs-lookup"><span data-stu-id="58976-156">-Target</span></span>
<span data-ttu-id="58976-157">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="58976-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="58976-158">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="58976-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="58976-159">Geben Sie diesen Parameter nur für den Endpunkttyp ExternalEndpoints an.</span><span class="sxs-lookup"><span data-stu-id="58976-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="58976-160">Geben Sie bei anderen Endpunkttypen stattdessen den *Parameter TargetResourceId* an.</span><span class="sxs-lookup"><span data-stu-id="58976-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="58976-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="58976-161">-TargetResourceId</span></span>
<span data-ttu-id="58976-162">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="58976-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="58976-163">Geben Sie diesen Parameter nur für die AzureEndpoints- und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="58976-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="58976-164">Geben Sie für den Endpunkttyp ExternalEndpoints stattdessen den *Parameter Target* an.</span><span class="sxs-lookup"><span data-stu-id="58976-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="58976-165">-Type</span><span class="sxs-lookup"><span data-stu-id="58976-165">-Type</span></span>
<span data-ttu-id="58976-166">Gibt den Endpunkttyp an, den dieses Cmdlet dem Traffic Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="58976-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="58976-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="58976-167">Valid values are:</span></span> 

- <span data-ttu-id="58976-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="58976-168">AzureEndpoints</span></span>
- <span data-ttu-id="58976-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="58976-169">ExternalEndpoints</span></span>
- <span data-ttu-id="58976-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="58976-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="58976-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="58976-171">-Weight</span></span>
<span data-ttu-id="58976-172">Gibt die Gewichtung an, die Traffic Manager dem Endpunkt zugibt.</span><span class="sxs-lookup"><span data-stu-id="58976-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="58976-173">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="58976-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="58976-174">Der Standardwert ist ein Wert (1).</span><span class="sxs-lookup"><span data-stu-id="58976-174">The default value is one (1).</span></span>
<span data-ttu-id="58976-175">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der Methode "Gewichteter Datenverkehrsrouting" konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="58976-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="58976-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58976-176">CommonParameters</span></span>
<span data-ttu-id="58976-177">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58976-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58976-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58976-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58976-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58976-179">INPUTS</span></span>

### <span data-ttu-id="58976-180">Keine</span><span class="sxs-lookup"><span data-stu-id="58976-180">None</span></span>

## <span data-ttu-id="58976-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58976-181">OUTPUTS</span></span>

### <span data-ttu-id="58976-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="58976-183">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="58976-183">NOTES</span></span>

## <span data-ttu-id="58976-184">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="58976-184">RELATED LINKS</span></span>

[<span data-ttu-id="58976-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="58976-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="58976-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="58976-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58976-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="58976-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58976-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="58976-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="58976-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="58976-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58976-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


