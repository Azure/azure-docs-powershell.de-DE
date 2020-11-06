---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500914"
---
# <span data-ttu-id="c341d-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="c341d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c341d-102">SYNOPSIS</span></span>
<span data-ttu-id="c341d-103">Erstellt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c341d-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c341d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c341d-104">SYNTAX</span></span>

### <span data-ttu-id="c341d-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c341d-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c341d-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="c341d-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c341d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c341d-107">DESCRIPTION</span></span>
<span data-ttu-id="c341d-108">Das Cmdlet **New-AzureRmCdnEndpoint** erstellt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c341d-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c341d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c341d-109">EXAMPLES</span></span>

## <span data-ttu-id="c341d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c341d-110">PARAMETERS</span></span>

### <span data-ttu-id="c341d-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c341d-111">-CdnProfile</span></span>
<span data-ttu-id="c341d-112">Gibt das CDN-Profilobjekt an, dem der Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c341d-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="c341d-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="c341d-114">Gibt ein Array von Inhaltstypen an, die vom Edge-Knoten zum Client komprimiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c341d-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="c341d-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="c341d-115">-EndpointName</span></span>
<span data-ttu-id="c341d-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c341d-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="c341d-117">-Geofilter</span><span class="sxs-lookup"><span data-stu-id="c341d-117">-GeoFilters</span></span>
<span data-ttu-id="c341d-118">Die Liste der Geo-Filter, die für diesen Endpunkt gelten.</span><span class="sxs-lookup"><span data-stu-id="c341d-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="c341d-119">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="c341d-119">-HttpPort</span></span>
<span data-ttu-id="c341d-120">Gibt die HTTP-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="c341d-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="c341d-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c341d-121">-HttpsPort</span></span>
<span data-ttu-id="c341d-122">Gibt die HTTPS-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="c341d-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="c341d-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="c341d-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="c341d-124">Gibt an, ob die Komprimierung für den Endpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c341d-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="c341d-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="c341d-125">-IsHttpAllowed</span></span>
<span data-ttu-id="c341d-126">Gibt an, ob der Endpunkt HTTP-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c341d-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="c341d-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="c341d-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="c341d-128">Gibt an, ob der Endpunkt HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c341d-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="c341d-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="c341d-129">-Location</span></span>
<span data-ttu-id="c341d-130">Gibt den Ressourcenspeicherort des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c341d-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="c341d-131">-OptimizationType</span></span>
<span data-ttu-id="c341d-132">Gibt jede Optimierung an, die dieser Endpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="c341d-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="c341d-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="c341d-133">-OriginHostHeader</span></span>
<span data-ttu-id="c341d-134">Gibt den Ursprungshost Kopf des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c341d-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="c341d-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="c341d-135">-OriginHostName</span></span>
<span data-ttu-id="c341d-136">Gibt den Hostnamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="c341d-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="c341d-137">-OriginName</span><span class="sxs-lookup"><span data-stu-id="c341d-137">-OriginName</span></span>
<span data-ttu-id="c341d-138">Gibt den Ressourcennamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="c341d-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="c341d-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="c341d-139">-OriginPath</span></span>
<span data-ttu-id="c341d-140">Gibt den Pfad des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="c341d-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="c341d-141">-Profilname</span><span class="sxs-lookup"><span data-stu-id="c341d-141">-ProfileName</span></span>
<span data-ttu-id="c341d-142">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="c341d-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="c341d-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="c341d-144">Gibt das Verhalten des CDN-Endpunkts an, wenn sich eine Abfragezeichenfolge in der Anforderungs-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="c341d-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="c341d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c341d-145">-ResourceGroupName</span></span>
<span data-ttu-id="c341d-146">Gibt den Namen der Ressourcengruppe an, zu der dieser Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="c341d-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-147">-Tags</span><span class="sxs-lookup"><span data-stu-id="c341d-147">-Tags</span></span>
<span data-ttu-id="c341d-148">Gibt eine Hashtabelle der Transponder an, die dieser Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c341d-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="c341d-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c341d-149">-Confirm</span></span>
<span data-ttu-id="c341d-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c341d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c341d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c341d-151">-WhatIf</span></span>
<span data-ttu-id="c341d-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c341d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c341d-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c341d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c341d-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c341d-154">-DefaultProfile</span></span>
<span data-ttu-id="c341d-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c341d-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c341d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c341d-156">CommonParameters</span></span>
<span data-ttu-id="c341d-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c341d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c341d-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c341d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c341d-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c341d-159">INPUTS</span></span>

### <span data-ttu-id="c341d-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="c341d-160">PSProfile</span></span>
<span data-ttu-id="c341d-161">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c341d-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="c341d-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c341d-162">OUTPUTS</span></span>

### <span data-ttu-id="c341d-163">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c341d-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="c341d-164">NOTES</span></span>

## <span data-ttu-id="c341d-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c341d-165">RELATED LINKS</span></span>

[<span data-ttu-id="c341d-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c341d-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c341d-168">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c341d-169">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c341d-170">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c341d-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


