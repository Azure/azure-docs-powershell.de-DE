---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 4d13df2e498dd3af0c0a29660673e61233e1d4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928099"
---
# <span data-ttu-id="a4d72-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="a4d72-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="a4d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d72-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d72-103">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regelmodulregel.</span><span class="sxs-lookup"><span data-stu-id="a4d72-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="a4d72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4d72-104">SYNTAX</span></span>

### <span data-ttu-id="a4d72-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4d72-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4d72-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4d72-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4d72-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4d72-107">DESCRIPTION</span></span>
<span data-ttu-id="a4d72-108">Erstellen Sie ein PSRulesEngineAction-Objekt zum Erstellen einer Regelmodulregel.</span><span class="sxs-lookup"><span data-stu-id="a4d72-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="a4d72-109">Verwenden Sie das Cmdlet "New-AzFrontDoorHeaderActionObject", um PSHeaderObjects zu erstellen, um die Parameter "-RequestHeaderActions" und "-ResponseHeaderActions" zu übergeben."</span><span class="sxs-lookup"><span data-stu-id="a4d72-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="a4d72-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4d72-110">EXAMPLES</span></span>

### <span data-ttu-id="a4d72-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4d72-111">Example 1</span></span>
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

<span data-ttu-id="a4d72-112">Erstellen Sie eine Regelmodulaktion, und zeigen Sie, wie Sie die Eigenschaften der erstellten Regelmodulaktion anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="a4d72-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4d72-113">PARAMETERS</span></span>

### <span data-ttu-id="a4d72-114">-Back-EndPoolName</span><span class="sxs-lookup"><span data-stu-id="a4d72-114">-BackendPoolName</span></span>
<span data-ttu-id="a4d72-115">Der Name des Back-EndPools, zu dem diese Regel weitergeleitet wird</span><span class="sxs-lookup"><span data-stu-id="a4d72-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="a4d72-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="a4d72-116">-CustomForwardingPath</span></span>
<span data-ttu-id="a4d72-117">Der benutzerdefinierte Pfad zum Neuschreiben von Ressourcenpfaden, der mit dieser Regel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="a4d72-118">Lassen Sie leer, um den posteingangspfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4d72-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="a4d72-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="a4d72-119">-CustomFragment</span></span>
<span data-ttu-id="a4d72-120">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4d72-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="a4d72-121">Fragment ist der Teil der URL, der nach #kommt.</span><span class="sxs-lookup"><span data-stu-id="a4d72-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="a4d72-122">Schließen Sie das -Zeichen #nicht ein.</span><span class="sxs-lookup"><span data-stu-id="a4d72-122">Do not include the #.</span></span>

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

### <span data-ttu-id="a4d72-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="a4d72-123">-CustomHost</span></span>
<span data-ttu-id="a4d72-124">Host zum Umleiten.</span><span class="sxs-lookup"><span data-stu-id="a4d72-124">Host to redirect.</span></span>
<span data-ttu-id="a4d72-125">Lassen Sie leer, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4d72-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="a4d72-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="a4d72-126">-CustomPath</span></span>
<span data-ttu-id="a4d72-127">Der vollständige Umleitungspfad.</span><span class="sxs-lookup"><span data-stu-id="a4d72-127">The full path to redirect.</span></span>
<span data-ttu-id="a4d72-128">Pfad darf nicht leer sein und muss mit /beginnen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="a4d72-129">Lassen Sie leer, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4d72-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="a4d72-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="a4d72-130">-CustomQueryString</span></span>
<span data-ttu-id="a4d72-131">Die Gruppe der Abfragezeichenfolgen, die in der Umleitungs-URL platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="a4d72-132">Durch Festlegen dieses Werts wird jede vorhandene Abfragezeichenfolge ersetzt. lassen Sie leer, um die eingehende Abfragezeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4d72-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="a4d72-133">Die Abfragezeichenfolge muss im Format \<key\> = \<value\> vorliegen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="a4d72-134">Das erste ?</span><span class="sxs-lookup"><span data-stu-id="a4d72-134">The first ?</span></span>
<span data-ttu-id="a4d72-135">und & werden automatisch hinzugefügt, sodass Sie sie nicht in den Vordermann nehmen, sondern mehrere Abfragezeichenfolgen durch &.</span><span class="sxs-lookup"><span data-stu-id="a4d72-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="a4d72-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d72-136">-DefaultProfile</span></span>
<span data-ttu-id="a4d72-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4d72-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d72-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="a4d72-138">-DynamicCompression</span></span>
<span data-ttu-id="a4d72-139">Aktivieren der dynamischen Komprimierung für zwischengespeicherte Inhalte</span><span class="sxs-lookup"><span data-stu-id="a4d72-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="a4d72-140">Standardwert ist Aktiviert</span><span class="sxs-lookup"><span data-stu-id="a4d72-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="a4d72-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="a4d72-141">-EnableCaching</span></span>
<span data-ttu-id="a4d72-142">Gibt an, ob die Zwischenspeicherung für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4d72-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="a4d72-143">Standardwert ist falsch</span><span class="sxs-lookup"><span data-stu-id="a4d72-143">Default value is false</span></span>

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

### <span data-ttu-id="a4d72-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="a4d72-144">-ForwardingProtocol</span></span>
<span data-ttu-id="a4d72-145">Das Protokoll, das diese Regel verwendet, wenn Datenverkehr an Back-End-Ends weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a4d72-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="a4d72-146">Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="a4d72-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="a4d72-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a4d72-147">-FrontDoorName</span></span>
<span data-ttu-id="a4d72-148">Der Name der Eingangstür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="a4d72-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="a4d72-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="a4d72-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="a4d72-150">Die Behandlung von URL-Abfragebegriffen beim Erstellen des Cacheschlüssels.</span><span class="sxs-lookup"><span data-stu-id="a4d72-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="a4d72-151">Standardwert ist StripAll</span><span class="sxs-lookup"><span data-stu-id="a4d72-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="a4d72-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="a4d72-152">-RedirectProtocol</span></span>
<span data-ttu-id="a4d72-153">Das Protokoll des Ziels, an das der Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a4d72-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="a4d72-154">Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="a4d72-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="a4d72-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="a4d72-155">-RedirectType</span></span>
<span data-ttu-id="a4d72-156">Der Umleitungstyp, den die Regel beim Umleiten von Datenverkehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4d72-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="a4d72-157">Standardwert wird verschoben</span><span class="sxs-lookup"><span data-stu-id="a4d72-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="a4d72-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="a4d72-158">-RequestHeaderAction</span></span>
<span data-ttu-id="a4d72-159">Eine Liste der Headeraktionen, die von der Anforderung von AFD auf den Ursprung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="a4d72-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d72-160">-ResourceGroupName</span></span>
<span data-ttu-id="a4d72-161">Der Ressourcengruppenname, in dem die RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4d72-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="a4d72-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="a4d72-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="a4d72-163">Eine Liste der Headeraktionen, die aus der Antwort von AFD auf den Client angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4d72-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="a4d72-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d72-164">CommonParameters</span></span>
<span data-ttu-id="a4d72-165">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d72-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d72-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4d72-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d72-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4d72-167">INPUTS</span></span>

### <span data-ttu-id="a4d72-168">Keine</span><span class="sxs-lookup"><span data-stu-id="a4d72-168">None</span></span>

## <span data-ttu-id="a4d72-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4d72-169">OUTPUTS</span></span>

### <span data-ttu-id="a4d72-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="a4d72-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="a4d72-171">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4d72-171">NOTES</span></span>

## <span data-ttu-id="a4d72-172">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4d72-172">RELATED LINKS</span></span>
