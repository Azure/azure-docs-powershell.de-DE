---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167524"
---
# <span data-ttu-id="26608-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="26608-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="26608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26608-102">SYNOPSIS</span></span>
<span data-ttu-id="26608-103">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regel des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="26608-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="26608-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26608-104">SYNTAX</span></span>

### <span data-ttu-id="26608-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="26608-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26608-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26608-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26608-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26608-107">DESCRIPTION</span></span>
<span data-ttu-id="26608-108">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regel des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="26608-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="26608-109">Verwenden Sie das Cmdlet "New-AzFrontDheaderActionObject", um PSHeaderObjects zu erstellen, um an die Parameter "-RequestHeaderActions" und "-ResponseHeaderActions" zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="26608-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="26608-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26608-110">EXAMPLES</span></span>

### <span data-ttu-id="26608-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26608-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="26608-112">Erstellen Sie eine Aktion des Regelmoduls, und zeigen Sie, wie die Eigenschaften der erstellten Aktion des Regelmoduls angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="26608-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="26608-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26608-113">PARAMETERS</span></span>

### <span data-ttu-id="26608-114">-Back-EndPoolName</span><span class="sxs-lookup"><span data-stu-id="26608-114">-BackendPoolName</span></span>
<span data-ttu-id="26608-115">Der Name des Back-EndPool-Speichers, an den diese Regel weitergeleitet wird</span><span class="sxs-lookup"><span data-stu-id="26608-115">The name of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="26608-116">-CustomForwardingPath</span></span>
<span data-ttu-id="26608-117">Der benutzerdefinierte Pfad, der zum Neuschreiben von Ressourcenpfaden verwendet wird, die dieser Regel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="26608-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="26608-118">Lassen Sie das Feld leer, um den eingehenden Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26608-118">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="26608-119">-CustomFragment</span></span>
<span data-ttu-id="26608-120">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26608-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="26608-121">Fragment ist der Teil der URL, der hinter "#" steht.</span><span class="sxs-lookup"><span data-stu-id="26608-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="26608-122">Schließen Sie nicht die Datei "#" ein.</span><span class="sxs-lookup"><span data-stu-id="26608-122">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="26608-123">-CustomHost</span></span>
<span data-ttu-id="26608-124">Hosten Sie die Umleitung.</span><span class="sxs-lookup"><span data-stu-id="26608-124">Host to redirect.</span></span>
<span data-ttu-id="26608-125">Lassen Sie das Feld leer, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26608-125">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="26608-126">-CustomPath</span></span>
<span data-ttu-id="26608-127">Der vollständige Pfad zur Umleitung.</span><span class="sxs-lookup"><span data-stu-id="26608-127">The full path to redirect.</span></span>
<span data-ttu-id="26608-128">"Path" darf nicht leer sein und muss mit "/" beginnen.</span><span class="sxs-lookup"><span data-stu-id="26608-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="26608-129">Lassen Sie das Feld leer, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26608-129">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="26608-130">-CustomQueryString</span></span>
<span data-ttu-id="26608-131">Der Satz von Abfragezeichenfolgen, die in die Umleitungs-URL gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26608-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="26608-132">Durch festlegen dieses Werts wird jede vorhandene Abfragezeichenfolge ersetzt. leer lassen, um die eingehende Abfragezeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="26608-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="26608-133">Die Abfragezeichenfolge muss im Format \<key\> = \<value\> vorliegen.</span><span class="sxs-lookup"><span data-stu-id="26608-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="26608-134">Das erste?</span><span class="sxs-lookup"><span data-stu-id="26608-134">The first ?</span></span>
<span data-ttu-id="26608-135">und & werden automatisch hinzugefügt. Fügen Sie sie daher nicht in den Vorder-/Hintergrund ein, sondern trennen Sie mehrere Abfragezeichenfolgen durch &.</span><span class="sxs-lookup"><span data-stu-id="26608-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26608-136">-DefaultProfile</span></span>
<span data-ttu-id="26608-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26608-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26608-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="26608-138">-DynamicCompression</span></span>
<span data-ttu-id="26608-139">Gibt an, ob die dynamische Komprimierung für zwischengespeicherte Inhalte aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26608-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="26608-140">Der Standardwert ist "Enabled".</span><span class="sxs-lookup"><span data-stu-id="26608-140">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="26608-141">-EnableCaching</span></span>
<span data-ttu-id="26608-142">Gibt an, ob zwischenspeichern für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26608-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="26608-143">Der Standardwert ist falsch.</span><span class="sxs-lookup"><span data-stu-id="26608-143">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="26608-144">-ForwardingProtocol</span></span>
<span data-ttu-id="26608-145">Das Protokoll, das diese Regel beim Weiterleiten von Datenverkehr an Back-End-Back-Ends verwendet.</span><span class="sxs-lookup"><span data-stu-id="26608-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="26608-146">Der Standardwert ist "MatchRequest".</span><span class="sxs-lookup"><span data-stu-id="26608-146">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-147">-FrontD anderenName</span><span class="sxs-lookup"><span data-stu-id="26608-147">-FrontDoorName</span></span>
<span data-ttu-id="26608-148">Der Name der Eingangstür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="26608-148">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="26608-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="26608-150">Die Behandlung von URL-Abfragebegriffen beim Erstellen des Cacheschlüssels.</span><span class="sxs-lookup"><span data-stu-id="26608-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="26608-151">Der Standardwert ist "StripAll".</span><span class="sxs-lookup"><span data-stu-id="26608-151">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="26608-152">-RedirectProtocol</span></span>
<span data-ttu-id="26608-153">Das Protokoll des Ziels, an das der Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="26608-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="26608-154">Der Standardwert ist "MatchRequest".</span><span class="sxs-lookup"><span data-stu-id="26608-154">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="26608-155">-RedirectType</span></span>
<span data-ttu-id="26608-156">Der Umleitungstyp, den die Regel beim Umleiten von Datenverkehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="26608-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="26608-157">Der Standardwert wird verschoben.</span><span class="sxs-lookup"><span data-stu-id="26608-157">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="26608-158">-RequestHeaderAction</span></span>
<span data-ttu-id="26608-159">Eine Liste der Headeraktionen, die von der Anforderung von AFD an den Ursprung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26608-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26608-160">-ResourceGroupName</span></span>
<span data-ttu-id="26608-161">Der Name der Ressourcengruppe, in der die RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="26608-161">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="26608-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="26608-163">Eine Liste der Headeraktionen, die aus der Antwort von AFD an den Client angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26608-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26608-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26608-164">CommonParameters</span></span>
<span data-ttu-id="26608-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26608-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26608-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26608-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26608-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26608-167">INPUTS</span></span>

### <span data-ttu-id="26608-168">Keine</span><span class="sxs-lookup"><span data-stu-id="26608-168">None</span></span>

## <span data-ttu-id="26608-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26608-169">OUTPUTS</span></span>

### <span data-ttu-id="26608-170">Microsoft.Azure.Commands.FrontDando.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="26608-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="26608-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26608-171">NOTES</span></span>

## <span data-ttu-id="26608-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26608-172">RELATED LINKS</span></span>
