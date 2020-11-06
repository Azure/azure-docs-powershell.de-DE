---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478669"
---
# <span data-ttu-id="8fc22-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="8fc22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fc22-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc22-103">Erstellt einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8fc22-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc22-104">SYNTAX</span></span>

### <span data-ttu-id="8fc22-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fc22-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc22-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc22-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc22-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fc22-107">DESCRIPTION</span></span>
<span data-ttu-id="8fc22-108">Das Cmdlet **New-AzureRmCdnEndpoint** erstellt einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8fc22-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8fc22-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fc22-109">EXAMPLES</span></span>

## <span data-ttu-id="8fc22-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fc22-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc22-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8fc22-111">-CdnProfile</span></span>
<span data-ttu-id="8fc22-112">Gibt das CDN-Profilobjekt an, dem der Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc22-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="8fc22-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="8fc22-114">Gibt ein Array von Inhaltstypen an, die vom Edge-Knoten zum Client komprimiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8fc22-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc22-115">-DefaultProfile</span></span>
<span data-ttu-id="8fc22-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8fc22-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="8fc22-117">-EndpointName</span></span>
<span data-ttu-id="8fc22-118">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-119">-Geofilter</span><span class="sxs-lookup"><span data-stu-id="8fc22-119">-GeoFilters</span></span>
<span data-ttu-id="8fc22-120">Die Liste der Geo-Filter, die für diesen Endpunkt gelten.</span><span class="sxs-lookup"><span data-stu-id="8fc22-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-121">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="8fc22-121">-HttpPort</span></span>
<span data-ttu-id="8fc22-122">Gibt die HTTP-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="8fc22-123">-HttpsPort</span></span>
<span data-ttu-id="8fc22-124">Gibt die HTTPS-Portnummer auf dem Ursprungsserver an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="8fc22-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="8fc22-126">Gibt an, ob die Komprimierung für den Endpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8fc22-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="8fc22-127">-IsHttpAllowed</span></span>
<span data-ttu-id="8fc22-128">Gibt an, ob der Endpunkt HTTP-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8fc22-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="8fc22-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="8fc22-130">Gibt an, ob der Endpunkt HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8fc22-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="8fc22-131">-Location</span></span>
<span data-ttu-id="8fc22-132">Gibt den Ressourcenspeicherort des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="8fc22-133">-OptimizationType</span></span>
<span data-ttu-id="8fc22-134">Gibt jede Optimierung an, die dieser Endpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="8fc22-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="8fc22-135">-OriginHostHeader</span></span>
<span data-ttu-id="8fc22-136">Gibt den Ursprungshost Kopf des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="8fc22-137">-OriginHostName</span></span>
<span data-ttu-id="8fc22-138">Gibt den Hostnamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="8fc22-139">-OriginName</span></span>
<span data-ttu-id="8fc22-140">Gibt den Ressourcennamen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="8fc22-141">-OriginPath</span></span>
<span data-ttu-id="8fc22-142">Gibt den Pfad des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-143">-Profilname</span><span class="sxs-lookup"><span data-stu-id="8fc22-143">-ProfileName</span></span>
<span data-ttu-id="8fc22-144">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="8fc22-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="8fc22-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="8fc22-146">Gibt das Verhalten des CDN-Endpunkts an, wenn sich eine Abfragezeichenfolge in der Anforderungs-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="8fc22-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc22-147">-ResourceGroupName</span></span>
<span data-ttu-id="8fc22-148">Gibt den Namen der Ressourcengruppe an, zu der dieser Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="8fc22-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="8fc22-149">-Tag</span></span>
<span data-ttu-id="8fc22-150">Die Tags, die dem Azure CDN-Endpunkt zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8fc22-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fc22-151">-Confirm</span></span>
<span data-ttu-id="8fc22-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fc22-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc22-153">-WhatIf</span></span>
<span data-ttu-id="8fc22-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc22-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc22-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fc22-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc22-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc22-156">CommonParameters</span></span>
<span data-ttu-id="8fc22-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc22-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc22-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc22-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc22-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fc22-159">INPUTS</span></span>

### <span data-ttu-id="8fc22-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="8fc22-160">PSProfile</span></span>
<span data-ttu-id="8fc22-161">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fc22-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="8fc22-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fc22-162">OUTPUTS</span></span>

### <span data-ttu-id="8fc22-163">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8fc22-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fc22-164">NOTES</span></span>

## <span data-ttu-id="8fc22-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fc22-165">RELATED LINKS</span></span>

[<span data-ttu-id="8fc22-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8fc22-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8fc22-168">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8fc22-169">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8fc22-170">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fc22-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


