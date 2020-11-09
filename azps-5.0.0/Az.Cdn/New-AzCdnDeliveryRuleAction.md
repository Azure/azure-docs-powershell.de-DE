---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300387"
---
# <span data-ttu-id="2337e-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="2337e-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="2337e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2337e-102">SYNOPSIS</span></span>
<span data-ttu-id="2337e-103">Erstellt eine Zustellungs Aktion.</span><span class="sxs-lookup"><span data-stu-id="2337e-103">Creates a delivery action.</span></span>

## <span data-ttu-id="2337e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2337e-104">SYNTAX</span></span>

### <span data-ttu-id="2337e-105">CacheExpirationActionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2337e-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337e-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2337e-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337e-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2337e-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337e-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2337e-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337e-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2337e-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2337e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2337e-110">DESCRIPTION</span></span>
<span data-ttu-id="2337e-111">Das Cmdlet **New-AzCdnDeliveryRule** erstellt eine Übermittlungs Regel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="2337e-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="2337e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2337e-112">EXAMPLES</span></span>

### <span data-ttu-id="2337e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2337e-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="2337e-114">Erstellen einer einfachen Übermittlungs Regel</span><span class="sxs-lookup"><span data-stu-id="2337e-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="2337e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2337e-115">PARAMETERS</span></span>

### <span data-ttu-id="2337e-116">– Aktion</span><span class="sxs-lookup"><span data-stu-id="2337e-116">-Action</span></span>
<span data-ttu-id="2337e-117">Auszuführende Aktion</span><span class="sxs-lookup"><span data-stu-id="2337e-117">Action to perform.</span></span>

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

### <span data-ttu-id="2337e-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="2337e-118">-CacheBehavior</span></span>
<span data-ttu-id="2337e-119">Zwischenspeicherungsverhalten für die Aktion</span><span class="sxs-lookup"><span data-stu-id="2337e-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="2337e-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="2337e-120">-CacheDuration</span></span>
<span data-ttu-id="2337e-121">Die Dauer, für die der Inhalt zwischengespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2337e-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="2337e-122">Das zulässige Format ist \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="2337e-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="2337e-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="2337e-123">-CustomFragment</span></span>
<span data-ttu-id="2337e-124">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2337e-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="2337e-125">Fragment ist der Teil der URL, der hinter # steht.</span><span class="sxs-lookup"><span data-stu-id="2337e-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="2337e-126">Schließen Sie nicht das # ein.</span><span class="sxs-lookup"><span data-stu-id="2337e-126">Do not include the #.</span></span>

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

### <span data-ttu-id="2337e-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="2337e-127">-CustomHostname</span></span>
<span data-ttu-id="2337e-128">Host zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="2337e-128">Host to redirect.</span></span>
<span data-ttu-id="2337e-129">Leer lassen, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2337e-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="2337e-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="2337e-130">-CustomPath</span></span>
<span data-ttu-id="2337e-131">Der vollständige Pfad zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="2337e-131">The full path to redirect.</span></span>
<span data-ttu-id="2337e-132">Path darf nicht leer sein und muss mit/beginnen.</span><span class="sxs-lookup"><span data-stu-id="2337e-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="2337e-133">Leer lassen, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2337e-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="2337e-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="2337e-134">-CustomQueryString</span></span>
<span data-ttu-id="2337e-135">Der Satz von Abfragezeichenfolgen, der in die Redirect-URL gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2337e-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="2337e-136">Wenn Sie diesen Wert festlegen, wird jede vorhandene Abfragezeichenfolge ersetzt. leer lassen, um die eingehende Abfragezeichenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="2337e-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="2337e-137">Die Abfragezeichenfolge muss im \<key\> = \<value\> Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="2337e-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="2337e-138">?</span><span class="sxs-lookup"><span data-stu-id="2337e-138">?</span></span> <span data-ttu-id="2337e-139">und & werden automatisch hinzugefügt, damit Sie nicht einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="2337e-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="2337e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2337e-140">-DefaultProfile</span></span>
<span data-ttu-id="2337e-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2337e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2337e-142">-Ziel</span><span class="sxs-lookup"><span data-stu-id="2337e-142">-Destination</span></span>
<span data-ttu-id="2337e-143">Definieren Sie die relative URL, mit der die obigen Anforderungen neu geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2337e-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="2337e-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="2337e-144">-DestinationProtocol</span></span>
<span data-ttu-id="2337e-145">Das für die Umleitung zu verwendende Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2337e-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="2337e-146">Der Standardwert ist MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="2337e-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="2337e-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="2337e-147">-HeaderActionType</span></span>
<span data-ttu-id="2337e-148">Ob der Anforderungs Kopf oder der Antwortheader geändert werden soll</span><span class="sxs-lookup"><span data-stu-id="2337e-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="2337e-149">-Headername</span><span class="sxs-lookup"><span data-stu-id="2337e-149">-HeaderName</span></span>
<span data-ttu-id="2337e-150">Der Name der zu ändernden Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="2337e-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="2337e-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="2337e-151">-PreservePath</span></span>
<span data-ttu-id="2337e-152">Gibt an, ob der nicht übereinstimmende Pfad beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="2337e-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="2337e-153">-Queryparameter</span><span class="sxs-lookup"><span data-stu-id="2337e-153">-QueryParameter</span></span>
<span data-ttu-id="2337e-154">Abfrageparameter, die eingefügt oder ausgeschlossen werden sollen (Komma getrennt).</span><span class="sxs-lookup"><span data-stu-id="2337e-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="2337e-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="2337e-155">-QueryStringBehavior</span></span>
<span data-ttu-id="2337e-156">QueryString-Verhalten für die Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2337e-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="2337e-157">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="2337e-157">-RedirectType</span></span>
<span data-ttu-id="2337e-158">Der Redirect-Typ, der von der Regel beim Umleiten von Datenverkehr verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2337e-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="2337e-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="2337e-159">-SourcePattern</span></span>
<span data-ttu-id="2337e-160">Definieren Sie ein Anforderungs-URI-Muster, das die Art der Anforderungen identifiziert, die möglicherweise neu geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2337e-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="2337e-161">Wenn value leer ist, werden alle Zeichenfolgen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2337e-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="2337e-162">-Wert</span><span class="sxs-lookup"><span data-stu-id="2337e-162">-Value</span></span>
<span data-ttu-id="2337e-163">Der Wert für die angegebene Aktion.</span><span class="sxs-lookup"><span data-stu-id="2337e-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="2337e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2337e-164">CommonParameters</span></span>
<span data-ttu-id="2337e-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2337e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2337e-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2337e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2337e-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2337e-167">INPUTS</span></span>

### <span data-ttu-id="2337e-168">Keine</span><span class="sxs-lookup"><span data-stu-id="2337e-168">None</span></span>

## <span data-ttu-id="2337e-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2337e-169">OUTPUTS</span></span>

### <span data-ttu-id="2337e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="2337e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="2337e-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="2337e-171">NOTES</span></span>

## <span data-ttu-id="2337e-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2337e-172">RELATED LINKS</span></span>
