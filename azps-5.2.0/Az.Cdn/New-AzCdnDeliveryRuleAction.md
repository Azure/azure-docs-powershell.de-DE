---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296740"
---
# <span data-ttu-id="32606-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="32606-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="32606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32606-102">SYNOPSIS</span></span>
<span data-ttu-id="32606-103">Erstellt eine Übermittlungsaktion.</span><span class="sxs-lookup"><span data-stu-id="32606-103">Creates a delivery action.</span></span>

## <span data-ttu-id="32606-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32606-104">SYNTAX</span></span>

### <span data-ttu-id="32606-105">CacheExpirationActionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32606-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32606-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="32606-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32606-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="32606-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32606-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="32606-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32606-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="32606-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32606-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32606-110">DESCRIPTION</span></span>
<span data-ttu-id="32606-111">Das **Cmdlet "New-AzCdnDeliveryRule"** erstellt eine Zustellungsregel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="32606-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="32606-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32606-112">EXAMPLES</span></span>

### <span data-ttu-id="32606-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32606-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="32606-114">Erstellen Sie eine einfache Zustellungsregel.</span><span class="sxs-lookup"><span data-stu-id="32606-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="32606-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32606-115">PARAMETERS</span></span>

### <span data-ttu-id="32606-116">-Action</span><span class="sxs-lookup"><span data-stu-id="32606-116">-Action</span></span>
<span data-ttu-id="32606-117">Durchzuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="32606-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="32606-118">-CacheBehavior</span></span>
<span data-ttu-id="32606-119">Zwischenspeicherungsverhalten für die Aktion</span><span class="sxs-lookup"><span data-stu-id="32606-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="32606-120">-CacheDuration</span></span>
<span data-ttu-id="32606-121">Die Dauer, für die der Inhalt zwischengespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="32606-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="32606-122">Das zulässige Format ist \[ d. \] hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="32606-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="32606-123">-CustomFragment</span></span>
<span data-ttu-id="32606-124">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32606-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="32606-125">Fragment ist der Teil der URL, der hinter "#" steht.</span><span class="sxs-lookup"><span data-stu-id="32606-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="32606-126">Schließen Sie die Datei "#" nicht ein.</span><span class="sxs-lookup"><span data-stu-id="32606-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="32606-127">-CustomHostname</span></span>
<span data-ttu-id="32606-128">Hosten Sie die Umleitung.</span><span class="sxs-lookup"><span data-stu-id="32606-128">Host to redirect.</span></span>
<span data-ttu-id="32606-129">Lassen Sie das Feld leer, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="32606-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="32606-130">-CustomPath</span></span>
<span data-ttu-id="32606-131">Der vollständige Pfad zur Umleitung.</span><span class="sxs-lookup"><span data-stu-id="32606-131">The full path to redirect.</span></span>
<span data-ttu-id="32606-132">"Path" darf nicht leer sein und muss mit "/" beginnen.</span><span class="sxs-lookup"><span data-stu-id="32606-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="32606-133">Lassen Sie das Feld leer, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="32606-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="32606-134">-CustomQueryString</span></span>
<span data-ttu-id="32606-135">Der Satz von Abfragezeichenfolgen, die in die Umleitungs-URL gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="32606-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="32606-136">Durch das Festlegen dieses Werts werden alle vorhandenen Abfragezeichenfolgen ersetzt. leer lassen, um die eingehende Abfragezeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="32606-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="32606-137">Die Abfragezeichenfolge muss im Format \<key\> = \<value\> vorliegen.</span><span class="sxs-lookup"><span data-stu-id="32606-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="32606-138">?</span><span class="sxs-lookup"><span data-stu-id="32606-138">?</span></span> <span data-ttu-id="32606-139">und & automatisch hinzugefügt werden, fügen Sie sie daher nicht ein.</span><span class="sxs-lookup"><span data-stu-id="32606-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32606-140">-DefaultProfile</span></span>
<span data-ttu-id="32606-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32606-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32606-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="32606-142">-Destination</span></span>
<span data-ttu-id="32606-143">Definieren Sie die relative URL, auf die die oben genannten Anforderungen umgeschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="32606-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="32606-144">-DestinationProtocol</span></span>
<span data-ttu-id="32606-145">Das Protokoll, das für die Umleitung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32606-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="32606-146">Der Standardwert ist "MatchRequest".</span><span class="sxs-lookup"><span data-stu-id="32606-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="32606-147">-HeaderActionType</span></span>
<span data-ttu-id="32606-148">Ob der Anforderungsheader oder der Antwortheader geändert werden soll</span><span class="sxs-lookup"><span data-stu-id="32606-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="32606-149">-HeaderName</span></span>
<span data-ttu-id="32606-150">Der Name der zu ändernde Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="32606-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="32606-151">-PreservePath</span></span>
<span data-ttu-id="32606-152">Gibt an, ob der nicht übereinstimmende Pfad beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="32606-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="32606-153">-QueryParameter</span></span>
<span data-ttu-id="32606-154">Abfrageparameter zum Ein- oder Ausschließen (durch Kommas getrennt).</span><span class="sxs-lookup"><span data-stu-id="32606-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="32606-155">-QueryStringBehavior</span></span>
<span data-ttu-id="32606-156">QueryString behavior for the requests</span><span class="sxs-lookup"><span data-stu-id="32606-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="32606-157">-RedirectType</span></span>
<span data-ttu-id="32606-158">Der Umleitungstyp, den die Regel beim Umleiten von Datenverkehr verwendet</span><span class="sxs-lookup"><span data-stu-id="32606-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="32606-159">-SourcePattern</span></span>
<span data-ttu-id="32606-160">Definieren Sie ein Anforderungs-URI-Muster, das den Typ der Anforderungen identifiziert, die neu geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="32606-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="32606-161">Wenn der Wert leer ist, werden alle Zeichenfolgen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="32606-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-162">-Value</span><span class="sxs-lookup"><span data-stu-id="32606-162">-Value</span></span>
<span data-ttu-id="32606-163">Wert für die angegebene Aktion.</span><span class="sxs-lookup"><span data-stu-id="32606-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32606-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32606-164">CommonParameters</span></span>
<span data-ttu-id="32606-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32606-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32606-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32606-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32606-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32606-167">INPUTS</span></span>

### <span data-ttu-id="32606-168">Keine</span><span class="sxs-lookup"><span data-stu-id="32606-168">None</span></span>

## <span data-ttu-id="32606-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32606-169">OUTPUTS</span></span>

### <span data-ttu-id="32606-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="32606-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="32606-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32606-171">NOTES</span></span>

## <span data-ttu-id="32606-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32606-172">RELATED LINKS</span></span>
