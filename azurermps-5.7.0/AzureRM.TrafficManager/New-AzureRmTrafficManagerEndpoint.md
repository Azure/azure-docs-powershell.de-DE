---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663407"
---
# <span data-ttu-id="b4ea0-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b4ea0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ea0-103">Erstellt einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4ea0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4ea0-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4ea0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4ea0-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ea0-106">Das Cmdlet **New-AzureRmTrafficManagerEndpoint** erstellt einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b4ea0-107">Dieses Cmdlet übergibt jeden neuen Endpunkt an den Traffic Manager-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="b4ea0-108">Verwenden Sie das Add-AzureRmTrafficManagerEndpointConfig-Cmdlet, um mehrere Endpunkte zu einem lokalen Traffic Manager-Profilobjekt hinzuzufügen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="b4ea0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4ea0-109">EXAMPLES</span></span>

### <span data-ttu-id="b4ea0-110">Beispiel 1: Erstellen eines externen Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="b4ea0-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="b4ea0-111">Dieser Befehl erstellt einen externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b4ea0-112">Beispiel 2: Erstellen eines Azure-Endpunkts für ein Profil</span><span class="sxs-lookup"><span data-stu-id="b4ea0-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="b4ea0-113">Dieser Befehl erstellt einen Azure-Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppen-ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="b4ea0-114">Der Azure-Endpunkt verweist auf die Azure Web App, deren Azure Resource Manager-ID durch den URI-Pfad in *TargetResourceId* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="b4ea0-115">Der Befehl gibt keinen *EndpointLocation* -Parameter an, weil die Web App-Ressource den Speicherort bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="b4ea0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4ea0-116">PARAMETERS</span></span>

### <span data-ttu-id="b4ea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ea0-117">-DefaultProfile</span></span>
<span data-ttu-id="b4ea0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="b4ea0-119">-EndpointLocation</span></span>
<span data-ttu-id="b4ea0-120">Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="b4ea0-121">Dieser Parameter ist nur auf Endpunkte des ExternalEndpoints-oder NestedEndpoints-Typs anwendbar.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="b4ea0-122">Sie müssen diesen Parameter angeben, wenn die Methode zur Datenverkehrs Weiterleitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="b4ea0-123">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-123">Specify an Azure region name.</span></span>
<span data-ttu-id="b4ea0-124">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="b4ea0-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="b4ea0-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="b4ea0-125">-EndpointStatus</span></span>
<span data-ttu-id="b4ea0-126">Gibt den Status des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="b4ea0-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b4ea0-127">Valid values are:</span></span> 

- <span data-ttu-id="b4ea0-128">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b4ea0-128">Enabled</span></span> 
- <span data-ttu-id="b4ea0-129">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="b4ea0-129">Disabled</span></span> 

<span data-ttu-id="b4ea0-130">Wenn der Status aktiviert ist, wird der Endpunkt nach Endpunkt Integrität untersucht und in die Datenverkehrs Routingmethode einbezogen.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-131">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="b4ea0-131">-GeoMapping</span></span>
<span data-ttu-id="b4ea0-132">Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="b4ea0-133">Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation des Traffic-Managers.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="b4ea0-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="b4ea0-134">-MinChildEndpoints</span></span>
<span data-ttu-id="b4ea0-135">Geben Sie den Namen eines Azure-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-135">Specify an Azure region name.</span></span>
<span data-ttu-id="b4ea0-136">Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="b4ea0-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="b4ea0-137">-Name</span></span>
<span data-ttu-id="b4ea0-138">Gibt den Namen des vom Cmdlet erstellten Traffic Manager-Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b4ea0-139">-Priorität</span><span class="sxs-lookup"><span data-stu-id="b4ea0-139">-Priority</span></span>
<span data-ttu-id="b4ea0-140">Gibt die Priorität an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b4ea0-141">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority-Datenverkehrs Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="b4ea0-142">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b4ea0-143">Niedrigere Werte stellen eine höhere Priorität dar.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="b4ea0-144">Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="b4ea0-145">Wenn Sie keine Prioritäten angeben, weist der Datenverkehrs-Manager den Endpunkten Standard Prioritätswerte zu, beginnend mit einem (1), in der Reihenfolge, in der das Profil die Endpunkte aufführt.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-146">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b4ea0-146">-ProfileName</span></span>
<span data-ttu-id="b4ea0-147">Gibt den Namen eines Traffic Manager-Profils an, dem dieses Cmdlet einen Endpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="b4ea0-148">Verwenden Sie zum Abrufen eines Profils die New-AzureRmTrafficManagerProfile-oder Get-AzureRmTrafficManagerProfile-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="b4ea0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ea0-149">-ResourceGroupName</span></span>
<span data-ttu-id="b4ea0-150">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b4ea0-151">Dieses Cmdlet erstellt einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4ea0-152">-Target</span><span class="sxs-lookup"><span data-stu-id="b4ea0-152">-Target</span></span>
<span data-ttu-id="b4ea0-153">Gibt den vollqualifizierten DNS-Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="b4ea0-154">Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="b4ea0-155">Geben Sie diesen Parameter nur für den ExternalEndpoints-Endpunkttyp an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="b4ea0-156">Geben Sie bei anderen Endpunkttypen stattdessen den *TargetResourceId* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="b4ea0-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ea0-157">-TargetResourceId</span></span>
<span data-ttu-id="b4ea0-158">Gibt die Ressourcen-ID des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="b4ea0-159">Geben Sie diesen Parameter nur für die AzureEndpoints-und NestedEndpoints-Endpunkttypen an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="b4ea0-160">Geben Sie für den ExternalEndpoints-Endpunkttyp stattdessen den *target* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="b4ea0-161">-Typ</span><span class="sxs-lookup"><span data-stu-id="b4ea0-161">-Type</span></span>
<span data-ttu-id="b4ea0-162">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b4ea0-163">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b4ea0-163">Valid values are:</span></span> 

- <span data-ttu-id="b4ea0-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b4ea0-164">AzureEndpoints</span></span>
- <span data-ttu-id="b4ea0-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b4ea0-165">ExternalEndpoints</span></span>
- <span data-ttu-id="b4ea0-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b4ea0-166">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-167">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="b4ea0-167">-Weight</span></span>
<span data-ttu-id="b4ea0-168">Gibt die Gewichtung an, die der Datenverkehrs-Manager dem Endpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b4ea0-169">Gültige Werte sind ganze Zahlen von 1 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b4ea0-170">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="b4ea0-170">The default value is one (1).</span></span>
<span data-ttu-id="b4ea0-171">Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der gewichteten Traffic-Routing-Methode konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea0-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ea0-172">CommonParameters</span></span>
<span data-ttu-id="b4ea0-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ea0-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ea0-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ea0-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4ea0-175">INPUTS</span></span>

### <span data-ttu-id="b4ea0-176">Keine</span><span class="sxs-lookup"><span data-stu-id="b4ea0-176">None</span></span>
<span data-ttu-id="b4ea0-177">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4ea0-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4ea0-178">OUTPUTS</span></span>

### <span data-ttu-id="b4ea0-179">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b4ea0-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4ea0-180">NOTES</span></span>

## <span data-ttu-id="b4ea0-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4ea0-181">RELATED LINKS</span></span>

[<span data-ttu-id="b4ea0-182">Deaktivieren-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b4ea0-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b4ea0-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b4ea0-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b4ea0-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b4ea0-186">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b4ea0-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b4ea0-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4ea0-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b4ea0-188">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b4ea0-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


