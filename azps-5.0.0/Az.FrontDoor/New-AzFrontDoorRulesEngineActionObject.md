---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177618"
---
# <span data-ttu-id="ac68a-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="ac68a-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="ac68a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac68a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac68a-103">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regelmodul Regel.</span><span class="sxs-lookup"><span data-stu-id="ac68a-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="ac68a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac68a-104">SYNTAX</span></span>

### <span data-ttu-id="ac68a-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac68a-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac68a-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac68a-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac68a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac68a-107">DESCRIPTION</span></span>
<span data-ttu-id="ac68a-108">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regelmodul Regel.</span><span class="sxs-lookup"><span data-stu-id="ac68a-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="ac68a-109">Verwenden Sie das Cmdlet "New-AzFrontDoorHeaderActionObject", um PSHeaderObjects zu erstellen, das an die Parameter "-RequestHeaderActions" und "-ResponseHeaderActions" übergeben wird. "</span><span class="sxs-lookup"><span data-stu-id="ac68a-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="ac68a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac68a-110">EXAMPLES</span></span>

### <span data-ttu-id="ac68a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac68a-111">Example 1</span></span>
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

<span data-ttu-id="ac68a-112">Erstellen Sie eine Regelmodul Aktion, und zeigen Sie an, wie die Eigenschaften der erstellten Regelmodul Aktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ac68a-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="ac68a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac68a-113">PARAMETERS</span></span>

### <span data-ttu-id="ac68a-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="ac68a-114">-BackendPoolName</span></span>
<span data-ttu-id="ac68a-115">Der Name des BackendPool, zu dem diese Regel weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ac68a-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="ac68a-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="ac68a-116">-CustomForwardingPath</span></span>
<span data-ttu-id="ac68a-117">Der benutzerdefinierte Pfad, der zum Umschreiben von Ressourcenpfaden verwendet wird, die dieser Regel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ac68a-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="ac68a-118">Leer lassen, um den eingehenden Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac68a-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="ac68a-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="ac68a-119">-CustomFragment</span></span>
<span data-ttu-id="ac68a-120">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac68a-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="ac68a-121">Fragment ist der Teil der URL, der hinter # steht.</span><span class="sxs-lookup"><span data-stu-id="ac68a-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="ac68a-122">Schließen Sie nicht das # ein.</span><span class="sxs-lookup"><span data-stu-id="ac68a-122">Do not include the #.</span></span>

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

### <span data-ttu-id="ac68a-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="ac68a-123">-CustomHost</span></span>
<span data-ttu-id="ac68a-124">Host zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="ac68a-124">Host to redirect.</span></span>
<span data-ttu-id="ac68a-125">Leer lassen, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac68a-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="ac68a-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="ac68a-126">-CustomPath</span></span>
<span data-ttu-id="ac68a-127">Der vollständige Pfad zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="ac68a-127">The full path to redirect.</span></span>
<span data-ttu-id="ac68a-128">Path darf nicht leer sein und muss mit/beginnen.</span><span class="sxs-lookup"><span data-stu-id="ac68a-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="ac68a-129">Leer lassen, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac68a-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="ac68a-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="ac68a-130">-CustomQueryString</span></span>
<span data-ttu-id="ac68a-131">Der Satz von Abfragezeichenfolgen, der in die Redirect-URL gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac68a-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="ac68a-132">Wenn Sie diesen Wert festlegen, wird jede vorhandene Abfragezeichenfolge ersetzt. leer lassen, um die eingehende Abfragezeichenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="ac68a-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="ac68a-133">Die Abfragezeichenfolge muss im \<key\> = \<value\> Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="ac68a-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="ac68a-134">Der erste?</span><span class="sxs-lookup"><span data-stu-id="ac68a-134">The first ?</span></span>
<span data-ttu-id="ac68a-135">und & werden automatisch hinzugefügt, sodass Sie nicht im Vordergrund enthalten sind, sondern mehrere Abfragezeichenfolgen mit & getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="ac68a-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="ac68a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac68a-136">-DefaultProfile</span></span>
<span data-ttu-id="ac68a-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac68a-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac68a-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="ac68a-138">-DynamicCompression</span></span>
<span data-ttu-id="ac68a-139">Gibt an, ob die dynamische Komprimierung für zwischengespeicherte Inhalte aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac68a-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="ac68a-140">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="ac68a-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="ac68a-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="ac68a-141">-EnableCaching</span></span>
<span data-ttu-id="ac68a-142">Gibt an, ob die Zwischenspeicherung für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac68a-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="ac68a-143">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="ac68a-143">Default value is false</span></span>

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

### <span data-ttu-id="ac68a-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="ac68a-144">-ForwardingProtocol</span></span>
<span data-ttu-id="ac68a-145">Das Protokoll, das diese Regel verwendet, wenn Datenverkehr an Backends weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ac68a-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="ac68a-146">Der Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="ac68a-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="ac68a-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ac68a-147">-FrontDoorName</span></span>
<span data-ttu-id="ac68a-148">Der Name der Haustür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="ac68a-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="ac68a-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="ac68a-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="ac68a-150">Die Behandlung von URL-Abfrageausdrücken beim bilden des Cacheschlüssels</span><span class="sxs-lookup"><span data-stu-id="ac68a-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="ac68a-151">Der Standardwert ist StripAll</span><span class="sxs-lookup"><span data-stu-id="ac68a-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="ac68a-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="ac68a-152">-RedirectProtocol</span></span>
<span data-ttu-id="ac68a-153">Das Protokoll des Ziels an die Stelle, an der der Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ac68a-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="ac68a-154">Der Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="ac68a-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="ac68a-155">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="ac68a-155">-RedirectType</span></span>
<span data-ttu-id="ac68a-156">Der Redirect-Typ, der von der Regel beim Umleiten von Datenverkehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac68a-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="ac68a-157">Standardwert wird verschoben</span><span class="sxs-lookup"><span data-stu-id="ac68a-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="ac68a-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="ac68a-158">-RequestHeaderAction</span></span>
<span data-ttu-id="ac68a-159">Eine Liste der Überschriften Aktionen, die von der Anforderung von "ausgehend" auf den Ursprung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac68a-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="ac68a-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac68a-160">-ResourceGroupName</span></span>
<span data-ttu-id="ac68a-161">Der Ressourcengruppenname, in dem der RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ac68a-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="ac68a-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="ac68a-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="ac68a-163">Eine Liste der Überschriften Aktionen, die von der Antwort von "ausgehend" auf den Client angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac68a-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="ac68a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac68a-164">CommonParameters</span></span>
<span data-ttu-id="ac68a-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac68a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac68a-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac68a-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac68a-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac68a-167">INPUTS</span></span>

### <span data-ttu-id="ac68a-168">Keine</span><span class="sxs-lookup"><span data-stu-id="ac68a-168">None</span></span>

## <span data-ttu-id="ac68a-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac68a-169">OUTPUTS</span></span>

### <span data-ttu-id="ac68a-170">Microsoft. Azure. Commands. Haustür. Models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="ac68a-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="ac68a-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac68a-171">NOTES</span></span>

## <span data-ttu-id="ac68a-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac68a-172">RELATED LINKS</span></span>
