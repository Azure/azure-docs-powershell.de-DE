---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 5636aeef0b1c04ffbb0faa7e44161628824e9f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949603"
---
# <span data-ttu-id="979a5-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="979a5-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="979a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="979a5-102">SYNOPSIS</span></span>
<span data-ttu-id="979a5-103">Aktualisiert einen CDN-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="979a5-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="979a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="979a5-104">SYNTAX</span></span>

### <span data-ttu-id="979a5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="979a5-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979a5-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="979a5-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979a5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="979a5-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="979a5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="979a5-108">DESCRIPTION</span></span>
<span data-ttu-id="979a5-109">Das **Set-AzCdnOrigin-Cmdlet** aktualisiert einen Azure Content Delivery Network (CDN)-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="979a5-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="979a5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="979a5-110">EXAMPLES</span></span>

## <span data-ttu-id="979a5-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="979a5-111">PARAMETERS</span></span>

### <span data-ttu-id="979a5-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="979a5-112">-CdnOrigin</span></span>
<span data-ttu-id="979a5-113">Gibt den Ursprungsserver an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="979a5-113">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979a5-114">-DefaultProfile</span></span>
<span data-ttu-id="979a5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="979a5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="979a5-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="979a5-116">-EndpointName</span></span>
<span data-ttu-id="979a5-117">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="979a5-117">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="979a5-118">-HostName</span></span>
<span data-ttu-id="979a5-119">Azure CDN-Origin-Hostname.</span><span class="sxs-lookup"><span data-stu-id="979a5-119">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="979a5-120">-HttpPort</span></span>
<span data-ttu-id="979a5-121">Azure CDN origin http port.</span><span class="sxs-lookup"><span data-stu-id="979a5-121">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="979a5-122">-HttpsPort</span></span>
<span data-ttu-id="979a5-123">Azure CDN Origin https port.</span><span class="sxs-lookup"><span data-stu-id="979a5-123">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="979a5-124">-OriginHostHeader</span></span>
<span data-ttu-id="979a5-125">Azure CDN-Origin-Hostheader.</span><span class="sxs-lookup"><span data-stu-id="979a5-125">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="979a5-126">-OriginName</span></span>
<span data-ttu-id="979a5-127">Azure CDN-Herkunftsname.</span><span class="sxs-lookup"><span data-stu-id="979a5-127">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-128">-Priorität</span><span class="sxs-lookup"><span data-stu-id="979a5-128">-Priority</span></span>
<span data-ttu-id="979a5-129">Azure CDN-Ursprungspriorität.</span><span class="sxs-lookup"><span data-stu-id="979a5-129">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="979a5-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="979a5-131">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="979a5-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="979a5-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="979a5-133">Privater Linkspeicherort für Azure CDN-Ursprung.</span><span class="sxs-lookup"><span data-stu-id="979a5-133">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="979a5-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="979a5-135">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="979a5-135">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="979a5-136">-ProfileName</span></span>
<span data-ttu-id="979a5-137">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="979a5-137">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979a5-138">-ResourceGroupName</span></span>
<span data-ttu-id="979a5-139">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="979a5-139">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="979a5-140">-Weight</span></span>
<span data-ttu-id="979a5-141">Azure CDN-Ursprungsgewichtung.</span><span class="sxs-lookup"><span data-stu-id="979a5-141">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="979a5-142">-Confirm</span></span>
<span data-ttu-id="979a5-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="979a5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979a5-144">-WhatIf</span></span>
<span data-ttu-id="979a5-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="979a5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="979a5-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="979a5-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979a5-147">CommonParameters</span></span>
<span data-ttu-id="979a5-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979a5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979a5-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="979a5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979a5-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="979a5-150">INPUTS</span></span>

### <span data-ttu-id="979a5-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="979a5-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="979a5-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="979a5-152">OUTPUTS</span></span>

### <span data-ttu-id="979a5-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="979a5-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="979a5-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="979a5-154">NOTES</span></span>

## <span data-ttu-id="979a5-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="979a5-155">RELATED LINKS</span></span>

[<span data-ttu-id="979a5-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="979a5-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


