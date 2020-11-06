---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499713"
---
# <span data-ttu-id="5631b-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5631b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5631b-102">SYNOPSIS</span></span>
<span data-ttu-id="5631b-103">Erstellt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5631b-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5631b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5631b-104">SYNTAX</span></span>

### <span data-ttu-id="5631b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5631b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5631b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5631b-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5631b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5631b-107">DESCRIPTION</span></span>
<span data-ttu-id="5631b-108">Das Cmdlet **New-AzureRmCdnEndpoint** erstellt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5631b-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5631b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5631b-109">EXAMPLES</span></span>

## <span data-ttu-id="5631b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5631b-110">PARAMETERS</span></span>

### <span data-ttu-id="5631b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5631b-111">-CdnProfile</span></span>
<span data-ttu-id="5631b-112">Gibt das CDN-Profilobjekt an, dem der Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5631b-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="5631b-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="5631b-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="5631b-114">Gibt ein Array von Inhaltstypen an, die vom Edge-Knoten zum Client komprimiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5631b-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="5631b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5631b-115">-DefaultProfile</span></span>
<span data-ttu-id="5631b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5631b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5631b-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5631b-117">-DeliveryPolicy</span></span>
<span data-ttu-id="5631b-118">Die Zustellungs Richtlinie für diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5631b-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="5631b-119">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="5631b-119">-EndpointName</span></span>
<span data-ttu-id="5631b-120">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5631b-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="5631b-121">-Geofilter</span><span class="sxs-lookup"><span data-stu-id="5631b-121">-GeoFilters</span></span>
<span data-ttu-id="5631b-122">Die Liste der Geo-Filter, die für diesen Endpunkt gelten.</span><span class="sxs-lookup"><span data-stu-id="5631b-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="5631b-123">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="5631b-123">-HttpPort</span></span>
<span data-ttu-id="5631b-124">Gibt die HTTP-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="5631b-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="5631b-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5631b-125">-HttpsPort</span></span>
<span data-ttu-id="5631b-126">Gibt die HTTPS-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="5631b-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="5631b-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="5631b-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="5631b-128">Gibt an, ob die Komprimierung für den Endpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5631b-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="5631b-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="5631b-129">-IsHttpAllowed</span></span>
<span data-ttu-id="5631b-130">Gibt an, ob der Endpunkt HTTP-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5631b-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="5631b-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="5631b-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="5631b-132">Gibt an, ob der Endpunkt HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5631b-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="5631b-133">-Standort</span><span class="sxs-lookup"><span data-stu-id="5631b-133">-Location</span></span>
<span data-ttu-id="5631b-134">Gibt den Ressourcenspeicherort des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5631b-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="5631b-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="5631b-135">-OptimizationType</span></span>
<span data-ttu-id="5631b-136">Gibt jede Optimierung an, die dieser Endpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="5631b-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="5631b-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5631b-137">-OriginHostHeader</span></span>
<span data-ttu-id="5631b-138">Gibt den Ursprungshost Kopf des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="5631b-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="5631b-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="5631b-139">-OriginHostName</span></span>
<span data-ttu-id="5631b-140">Gibt den Hostnamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="5631b-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="5631b-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5631b-141">-OriginName</span></span>
<span data-ttu-id="5631b-142">Gibt den Ressourcennamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="5631b-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="5631b-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="5631b-143">-OriginPath</span></span>
<span data-ttu-id="5631b-144">Gibt den Pfad des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="5631b-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="5631b-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="5631b-145">-ProbePath</span></span>
<span data-ttu-id="5631b-146">Gibt den Prüfpunkt-Pfad für die dynamische Website Beschleunigung an</span><span class="sxs-lookup"><span data-stu-id="5631b-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="5631b-147">-Profilname</span><span class="sxs-lookup"><span data-stu-id="5631b-147">-ProfileName</span></span>
<span data-ttu-id="5631b-148">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="5631b-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="5631b-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="5631b-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="5631b-150">Gibt das Verhalten des CDN-Endpunkts an, wenn sich eine Abfragezeichenfolge in der Anforderungs-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="5631b-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="5631b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5631b-151">-ResourceGroupName</span></span>
<span data-ttu-id="5631b-152">Gibt den Namen der Ressourcengruppe an, zu der dieser Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="5631b-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="5631b-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="5631b-153">-Tag</span></span>
<span data-ttu-id="5631b-154">Die Tags, die dem Azure CDN-Endpunkt zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5631b-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="5631b-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5631b-155">-Confirm</span></span>
<span data-ttu-id="5631b-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5631b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5631b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5631b-157">-WhatIf</span></span>
<span data-ttu-id="5631b-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5631b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5631b-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5631b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5631b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5631b-160">CommonParameters</span></span>
<span data-ttu-id="5631b-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5631b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5631b-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5631b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5631b-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5631b-163">INPUTS</span></span>

### <span data-ttu-id="5631b-164">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5631b-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="5631b-165">Parameter: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5631b-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="5631b-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5631b-166">OUTPUTS</span></span>

### <span data-ttu-id="5631b-167">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5631b-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="5631b-168">NOTES</span></span>

## <span data-ttu-id="5631b-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5631b-169">RELATED LINKS</span></span>

[<span data-ttu-id="5631b-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5631b-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5631b-172">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5631b-173">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5631b-174">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5631b-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


