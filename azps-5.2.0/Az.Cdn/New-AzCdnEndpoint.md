---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361820"
---
# <span data-ttu-id="84844-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="84844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84844-102">SYNOPSIS</span></span>
<span data-ttu-id="84844-103">Erstellt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="84844-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="84844-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84844-104">SYNTAX</span></span>

### <span data-ttu-id="84844-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="84844-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84844-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84844-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84844-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84844-107">DESCRIPTION</span></span>
<span data-ttu-id="84844-108">Das **Cmdlet "New-AzCdnEndpoint"** erstellt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="84844-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="84844-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84844-109">EXAMPLES</span></span>

## <span data-ttu-id="84844-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84844-110">PARAMETERS</span></span>

### <span data-ttu-id="84844-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="84844-111">-CdnProfile</span></span>
<span data-ttu-id="84844-112">Gibt das CDN-Profilobjekt an, dem der Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="84844-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84844-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="84844-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="84844-114">Gibt ein Array von Inhaltstypen an, die vom Edgeknoten zum Client komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="84844-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="84844-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="84844-116">Die standardmäßige Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="84844-116">The default origin group.</span></span>

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

### <span data-ttu-id="84844-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84844-117">-DefaultProfile</span></span>
<span data-ttu-id="84844-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="84844-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84844-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="84844-119">-DeliveryPolicy</span></span>
<span data-ttu-id="84844-120">Die Zustellungsrichtlinie für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="84844-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="84844-121">-EndpointName</span></span>
<span data-ttu-id="84844-122">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="84844-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="84844-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="84844-123">-GeoFilters</span></span>
<span data-ttu-id="84844-124">Die Liste der Geofilter, die für diesen Endpunkt gelten.</span><span class="sxs-lookup"><span data-stu-id="84844-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="84844-125">-HttpPort</span></span>
<span data-ttu-id="84844-126">Gibt die HTTP-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="84844-126">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="84844-127">-HttpsPort</span></span>
<span data-ttu-id="84844-128">Gibt die HTTPS-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="84844-128">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="84844-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="84844-130">Gibt an, ob die Komprimierung für den Endpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="84844-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="84844-131">-IsHttpAllowed</span></span>
<span data-ttu-id="84844-132">Gibt an, ob der Endpunkt den HTTP-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84844-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="84844-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="84844-134">Gibt an, ob der Endpunkt den HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84844-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-135">-Location</span><span class="sxs-lookup"><span data-stu-id="84844-135">-Location</span></span>
<span data-ttu-id="84844-136">Gibt den Ressourcenspeicherort des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="84844-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="84844-137">-OptimizationType</span></span>
<span data-ttu-id="84844-138">Gibt jede Optimierung an, über die dieser Endpunkt verfügt.</span><span class="sxs-lookup"><span data-stu-id="84844-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="84844-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="84844-139">-OriginGroupName</span></span>
<span data-ttu-id="84844-140">Der Name der Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="84844-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="84844-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="84844-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="84844-142">Die Anzahl von Sekunden zwischen Integritätstest.</span><span class="sxs-lookup"><span data-stu-id="84844-142">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="84844-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="84844-144">Der Pfad relativ zum Ursprung, der zur Ermittlung der Integrität des Ursprungs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84844-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="84844-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="84844-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="84844-146">Protokoll, das für integritätsintepunkt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="84844-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="84844-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="84844-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="84844-148">Der Typ der von der Integritätsintepunktanforderung vorgenommenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="84844-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="84844-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="84844-149">-OriginHostHeader</span></span>
<span data-ttu-id="84844-150">Gibt den Kopf des Endpunkts des Ursprungshosts an.</span><span class="sxs-lookup"><span data-stu-id="84844-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="84844-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="84844-151">-OriginHostName</span></span>
<span data-ttu-id="84844-152">Gibt den Hostnamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="84844-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="84844-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="84844-153">-OriginId</span></span>
<span data-ttu-id="84844-154">Azure CDN-Origin-Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="84844-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="84844-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="84844-155">-OriginName</span></span>
<span data-ttu-id="84844-156">Gibt den Ressourcennamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="84844-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="84844-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="84844-157">-OriginPath</span></span>
<span data-ttu-id="84844-158">Gibt den Pfad des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="84844-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="84844-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="84844-159">-Priority</span></span>
<span data-ttu-id="84844-160">Azure CDN-Origin-Priorität.</span><span class="sxs-lookup"><span data-stu-id="84844-160">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="84844-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="84844-162">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung eingeschlossen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="84844-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="84844-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="84844-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="84844-164">Speicherort für private Azure CDN-Origin-Links.</span><span class="sxs-lookup"><span data-stu-id="84844-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="84844-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="84844-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="84844-166">Ressourcen-ID für privaten Link des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="84844-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="84844-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="84844-167">-ProbePath</span></span>
<span data-ttu-id="84844-168">Gibt den Beispielpfad für die dynamische Websitebeschleunigung an.</span><span class="sxs-lookup"><span data-stu-id="84844-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="84844-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="84844-169">-ProfileName</span></span>
<span data-ttu-id="84844-170">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="84844-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="84844-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="84844-172">Gibt das Verhalten des CDN-Endpunkts an, wenn sich eine Abfragezeichenfolge in der Anforderungs-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="84844-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84844-173">-ResourceGroupName</span></span>
<span data-ttu-id="84844-174">Gibt den Namen der Ressourcengruppe an, zu der dieser Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="84844-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="84844-175">-Tag</span></span>
<span data-ttu-id="84844-176">Die Tags, die dem Azure CDN-Endpunkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="84844-176">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="84844-177">-Weight</span></span>
<span data-ttu-id="84844-178">Azure CDN Origin Weight.</span><span class="sxs-lookup"><span data-stu-id="84844-178">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84844-179">-Confirm</span></span>
<span data-ttu-id="84844-180">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84844-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-181">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="84844-181">-WhatIf</span></span>
<span data-ttu-id="84844-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84844-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84844-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84844-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84844-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84844-184">CommonParameters</span></span>
<span data-ttu-id="84844-185">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84844-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84844-186">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84844-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84844-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84844-187">INPUTS</span></span>

### <span data-ttu-id="84844-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="84844-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="84844-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84844-189">OUTPUTS</span></span>

### <span data-ttu-id="84844-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="84844-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="84844-191">NOTES</span></span>

## <span data-ttu-id="84844-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="84844-192">RELATED LINKS</span></span>

[<span data-ttu-id="84844-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="84844-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="84844-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="84844-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="84844-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84844-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


