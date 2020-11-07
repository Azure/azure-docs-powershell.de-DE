---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652289"
---
# <span data-ttu-id="4a483-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="4a483-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="4a483-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a483-102">SYNOPSIS</span></span>
<span data-ttu-id="4a483-103">Erstellt eine Zustellungs Aktion.</span><span class="sxs-lookup"><span data-stu-id="4a483-103">Creates a delivery action.</span></span>

## <span data-ttu-id="4a483-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a483-104">SYNTAX</span></span>

### <span data-ttu-id="4a483-105">CacheExpirationActionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a483-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a483-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a483-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a483-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a483-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a483-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a483-108">DESCRIPTION</span></span>
<span data-ttu-id="4a483-109">Das Cmdlet **New-AzCdnDeliveryRule** erstellt eine Übermittlungs Regel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="4a483-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="4a483-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a483-110">EXAMPLES</span></span>

### <span data-ttu-id="4a483-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a483-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="4a483-112">Erstellen einer einfachen Übermittlungs Regel</span><span class="sxs-lookup"><span data-stu-id="4a483-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="4a483-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a483-113">PARAMETERS</span></span>

### <span data-ttu-id="4a483-114">– Aktion</span><span class="sxs-lookup"><span data-stu-id="4a483-114">-Action</span></span>
<span data-ttu-id="4a483-115">Auszuführende Aktion</span><span class="sxs-lookup"><span data-stu-id="4a483-115">Action to perform.</span></span>

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

### <span data-ttu-id="4a483-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="4a483-116">-CacheBehavior</span></span>
<span data-ttu-id="4a483-117">Zwischenspeicherungsverhalten für die Aktion</span><span class="sxs-lookup"><span data-stu-id="4a483-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="4a483-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="4a483-118">-CacheDuration</span></span>
<span data-ttu-id="4a483-119">Die Dauer, für die der Inhalt zwischengespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4a483-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="4a483-120">Das zulässige Format ist \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="4a483-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="4a483-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="4a483-121">-CustomFragment</span></span>
<span data-ttu-id="4a483-122">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a483-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="4a483-123">Fragment ist der Teil der URL, der hinter # steht.</span><span class="sxs-lookup"><span data-stu-id="4a483-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="4a483-124">Schließen Sie nicht das # ein.</span><span class="sxs-lookup"><span data-stu-id="4a483-124">Do not include the #.</span></span>

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

### <span data-ttu-id="4a483-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="4a483-125">-CustomHostname</span></span>
<span data-ttu-id="4a483-126">Host zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="4a483-126">Host to redirect.</span></span>
<span data-ttu-id="4a483-127">Leer lassen, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a483-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="4a483-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="4a483-128">-CustomPath</span></span>
<span data-ttu-id="4a483-129">Der vollständige Pfad zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="4a483-129">The full path to redirect.</span></span>
<span data-ttu-id="4a483-130">Path darf nicht leer sein und muss mit/beginnen.</span><span class="sxs-lookup"><span data-stu-id="4a483-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="4a483-131">Leer lassen, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a483-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="4a483-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="4a483-132">-CustomQueryString</span></span>
<span data-ttu-id="4a483-133">Der Satz von Abfragezeichenfolgen, der in die Redirect-URL gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a483-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="4a483-134">Wenn Sie diesen Wert festlegen, wird jede vorhandene Abfragezeichenfolge ersetzt. leer lassen, um die eingehende Abfragezeichenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4a483-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="4a483-135">Die Abfragezeichenfolge muss im \< Schlüssel \> = \< Wert \> Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="4a483-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="4a483-136">?</span><span class="sxs-lookup"><span data-stu-id="4a483-136">?</span></span> <span data-ttu-id="4a483-137">und & werden automatisch hinzugefügt, damit Sie nicht einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4a483-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="4a483-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a483-138">-DefaultProfile</span></span>
<span data-ttu-id="4a483-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a483-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a483-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="4a483-140">-DestinationProtocol</span></span>
<span data-ttu-id="4a483-141">Das für die Umleitung zu verwendende Protokoll.</span><span class="sxs-lookup"><span data-stu-id="4a483-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="4a483-142">Der Standardwert ist MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="4a483-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="4a483-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="4a483-143">-HeaderActionType</span></span>
<span data-ttu-id="4a483-144">Ob der Anforderungs Kopf oder der Antwortheader geändert werden soll</span><span class="sxs-lookup"><span data-stu-id="4a483-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="4a483-145">-Headername</span><span class="sxs-lookup"><span data-stu-id="4a483-145">-HeaderName</span></span>
<span data-ttu-id="4a483-146">Der Name der zu ändernden Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="4a483-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="4a483-147">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="4a483-147">-RedirectType</span></span>
<span data-ttu-id="4a483-148">Der Redirect-Typ, der von der Regel beim Umleiten von Datenverkehr verwendet wird</span><span class="sxs-lookup"><span data-stu-id="4a483-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="4a483-149">-Wert</span><span class="sxs-lookup"><span data-stu-id="4a483-149">-Value</span></span>
<span data-ttu-id="4a483-150">Der Wert für die angegebene Aktion.</span><span class="sxs-lookup"><span data-stu-id="4a483-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="4a483-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a483-151">CommonParameters</span></span>
<span data-ttu-id="4a483-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a483-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a483-153">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a483-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a483-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a483-154">INPUTS</span></span>

### <span data-ttu-id="4a483-155">Keine</span><span class="sxs-lookup"><span data-stu-id="4a483-155">None</span></span>

## <span data-ttu-id="4a483-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a483-156">OUTPUTS</span></span>

### <span data-ttu-id="4a483-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="4a483-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="4a483-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a483-158">NOTES</span></span>

## <span data-ttu-id="4a483-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a483-159">RELATED LINKS</span></span>
