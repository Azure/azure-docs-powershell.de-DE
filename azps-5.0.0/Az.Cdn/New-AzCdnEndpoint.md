---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176472"
---
# <span data-ttu-id="b286d-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="b286d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b286d-102">SYNOPSIS</span></span>
<span data-ttu-id="b286d-103">Erstellt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b286d-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="b286d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b286d-104">SYNTAX</span></span>

### <span data-ttu-id="b286d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b286d-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="b286d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b286d-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="b286d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b286d-107">DESCRIPTION</span></span>
<span data-ttu-id="b286d-108">Das Cmdlet **New-AzCdnEndpoint** erstellt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b286d-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b286d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b286d-109">EXAMPLES</span></span>

## <span data-ttu-id="b286d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b286d-110">PARAMETERS</span></span>

### <span data-ttu-id="b286d-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b286d-111">-CdnProfile</span></span>
<span data-ttu-id="b286d-112">Gibt das CDN-Profilobjekt an, dem der Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b286d-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="b286d-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="b286d-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="b286d-114">Gibt ein Array von Inhaltstypen an, die vom Edge-Knoten zum Client komprimiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b286d-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="b286d-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="b286d-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="b286d-116">Die standardmäßige Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b286d-116">The default origin group.</span></span>

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

### <span data-ttu-id="b286d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b286d-117">-DefaultProfile</span></span>
<span data-ttu-id="b286d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b286d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b286d-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b286d-119">-DeliveryPolicy</span></span>
<span data-ttu-id="b286d-120">Die Zustellungs Richtlinie für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b286d-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="b286d-121">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="b286d-121">-EndpointName</span></span>
<span data-ttu-id="b286d-122">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b286d-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b286d-123">-Geofilter</span><span class="sxs-lookup"><span data-stu-id="b286d-123">-GeoFilters</span></span>
<span data-ttu-id="b286d-124">Die Liste der Geo-Filter, die für diesen Endpunkt gelten.</span><span class="sxs-lookup"><span data-stu-id="b286d-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="b286d-125">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="b286d-125">-HttpPort</span></span>
<span data-ttu-id="b286d-126">Gibt die HTTP-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="b286d-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="b286d-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="b286d-127">-HttpsPort</span></span>
<span data-ttu-id="b286d-128">Gibt die HTTPS-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="b286d-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="b286d-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b286d-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="b286d-130">Gibt an, ob die Komprimierung für den Endpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b286d-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="b286d-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="b286d-131">-IsHttpAllowed</span></span>
<span data-ttu-id="b286d-132">Gibt an, ob der Endpunkt HTTP-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b286d-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="b286d-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="b286d-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="b286d-134">Gibt an, ob der Endpunkt HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b286d-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="b286d-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="b286d-135">-Location</span></span>
<span data-ttu-id="b286d-136">Gibt den Ressourcenspeicherort des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b286d-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="b286d-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="b286d-137">-OptimizationType</span></span>
<span data-ttu-id="b286d-138">Gibt jede Optimierung an, die dieser Endpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="b286d-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="b286d-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="b286d-139">-OriginGroupName</span></span>
<span data-ttu-id="b286d-140">Der Name der Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b286d-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="b286d-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b286d-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="b286d-142">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="b286d-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="b286d-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="b286d-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="b286d-144">Der Pfad relativ zum Ursprung, der verwendet wird, um den Zustand des Ursprungs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b286d-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="b286d-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="b286d-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="b286d-146">Protokoll, das für die Integritätsprüfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b286d-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="b286d-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="b286d-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="b286d-148">Der Typ der ausgestellten Integritäts Prüfpunktanforderung.</span><span class="sxs-lookup"><span data-stu-id="b286d-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="b286d-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="b286d-149">-OriginHostHeader</span></span>
<span data-ttu-id="b286d-150">Gibt den Ursprungshost Kopf des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b286d-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="b286d-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="b286d-151">-OriginHostName</span></span>
<span data-ttu-id="b286d-152">Gibt den Hostnamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b286d-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="b286d-153">-Origin-Nr</span><span class="sxs-lookup"><span data-stu-id="b286d-153">-OriginId</span></span>
<span data-ttu-id="b286d-154">Azure CDN-Ursprungs Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="b286d-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="b286d-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b286d-155">-OriginName</span></span>
<span data-ttu-id="b286d-156">Gibt den Ressourcennamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b286d-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="b286d-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="b286d-157">-OriginPath</span></span>
<span data-ttu-id="b286d-158">Gibt den Pfad des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="b286d-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="b286d-159">-Priorität</span><span class="sxs-lookup"><span data-stu-id="b286d-159">-Priority</span></span>
<span data-ttu-id="b286d-160">Azure CDN-Ursprungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="b286d-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="b286d-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="b286d-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="b286d-162">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b286d-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="b286d-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="b286d-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="b286d-164">Azure CDN Origin-Speicherort für private Links.</span><span class="sxs-lookup"><span data-stu-id="b286d-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="b286d-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="b286d-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="b286d-166">Azure CDN Origin-Ressourcen-ID für private Links.</span><span class="sxs-lookup"><span data-stu-id="b286d-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="b286d-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="b286d-167">-ProbePath</span></span>
<span data-ttu-id="b286d-168">Gibt den Prüfpunkt-Pfad für die dynamische Website Beschleunigung an</span><span class="sxs-lookup"><span data-stu-id="b286d-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="b286d-169">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b286d-169">-ProfileName</span></span>
<span data-ttu-id="b286d-170">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="b286d-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b286d-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="b286d-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="b286d-172">Gibt das Verhalten des CDN-Endpunkts an, wenn sich eine Abfragezeichenfolge in der Anforderungs-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="b286d-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="b286d-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b286d-173">-ResourceGroupName</span></span>
<span data-ttu-id="b286d-174">Gibt den Namen der Ressourcengruppe an, zu der dieser Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="b286d-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="b286d-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="b286d-175">-Tag</span></span>
<span data-ttu-id="b286d-176">Die Tags, die dem Azure CDN-Endpunkt zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b286d-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="b286d-177">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="b286d-177">-Weight</span></span>
<span data-ttu-id="b286d-178">Azure CDN-Ursprungs Gewicht.</span><span class="sxs-lookup"><span data-stu-id="b286d-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="b286d-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b286d-179">-Confirm</span></span>
<span data-ttu-id="b286d-180">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b286d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b286d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b286d-181">-WhatIf</span></span>
<span data-ttu-id="b286d-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b286d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b286d-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b286d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b286d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b286d-184">CommonParameters</span></span>
<span data-ttu-id="b286d-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b286d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b286d-186">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b286d-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b286d-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b286d-187">INPUTS</span></span>

### <span data-ttu-id="b286d-188">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b286d-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b286d-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b286d-189">OUTPUTS</span></span>

### <span data-ttu-id="b286d-190">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b286d-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="b286d-191">NOTES</span></span>

## <span data-ttu-id="b286d-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b286d-192">RELATED LINKS</span></span>

[<span data-ttu-id="b286d-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b286d-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b286d-195">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b286d-196">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b286d-197">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b286d-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


