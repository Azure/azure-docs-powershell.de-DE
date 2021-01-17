---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470989"
---
# <span data-ttu-id="be2dc-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="be2dc-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="be2dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="be2dc-103">Aktualisiert einen CDN-Origin-Server.</span><span class="sxs-lookup"><span data-stu-id="be2dc-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="be2dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be2dc-104">SYNTAX</span></span>

### <span data-ttu-id="be2dc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="be2dc-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be2dc-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2dc-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be2dc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2dc-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be2dc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be2dc-108">DESCRIPTION</span></span>
<span data-ttu-id="be2dc-109">Das **Cmdlet Set-AzCdnOrigin** aktualisiert einen Azure Content Delivery Network (CDN)-Origin-Server.</span><span class="sxs-lookup"><span data-stu-id="be2dc-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="be2dc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be2dc-110">EXAMPLES</span></span>

## <span data-ttu-id="be2dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be2dc-111">PARAMETERS</span></span>

### <span data-ttu-id="be2dc-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="be2dc-112">-CdnOrigin</span></span>
<span data-ttu-id="be2dc-113">Gibt den Ursprungsserver an, der von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="be2dc-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="be2dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2dc-114">-DefaultProfile</span></span>
<span data-ttu-id="be2dc-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="be2dc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be2dc-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="be2dc-116">-EndpointName</span></span>
<span data-ttu-id="be2dc-117">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="be2dc-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="be2dc-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="be2dc-118">-HostName</span></span>
<span data-ttu-id="be2dc-119">Hostname des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="be2dc-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="be2dc-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="be2dc-120">-HttpPort</span></span>
<span data-ttu-id="be2dc-121">Httpport des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="be2dc-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="be2dc-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="be2dc-122">-HttpsPort</span></span>
<span data-ttu-id="be2dc-123">Https-Port des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="be2dc-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="be2dc-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="be2dc-124">-OriginHostHeader</span></span>
<span data-ttu-id="be2dc-125">Azure CDN-Origin-Hostheader.</span><span class="sxs-lookup"><span data-stu-id="be2dc-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="be2dc-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="be2dc-126">-OriginName</span></span>
<span data-ttu-id="be2dc-127">Azure CDN-Origin-Name.</span><span class="sxs-lookup"><span data-stu-id="be2dc-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="be2dc-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="be2dc-128">-Priority</span></span>
<span data-ttu-id="be2dc-129">Azure CDN-Origin-Priorität.</span><span class="sxs-lookup"><span data-stu-id="be2dc-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="be2dc-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="be2dc-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="be2dc-131">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung eingeschlossen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="be2dc-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="be2dc-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="be2dc-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="be2dc-133">Speicherort für private Links des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="be2dc-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="be2dc-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="be2dc-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="be2dc-135">Ressourcen-ID für privaten Link des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="be2dc-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="be2dc-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="be2dc-136">-ProfileName</span></span>
<span data-ttu-id="be2dc-137">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="be2dc-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="be2dc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be2dc-138">-ResourceGroupName</span></span>
<span data-ttu-id="be2dc-139">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="be2dc-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="be2dc-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="be2dc-140">-Weight</span></span>
<span data-ttu-id="be2dc-141">Azure CDN Origin Weight.</span><span class="sxs-lookup"><span data-stu-id="be2dc-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="be2dc-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be2dc-142">-Confirm</span></span>
<span data-ttu-id="be2dc-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be2dc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2dc-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="be2dc-144">-WhatIf</span></span>
<span data-ttu-id="be2dc-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be2dc-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be2dc-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be2dc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2dc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2dc-147">CommonParameters</span></span>
<span data-ttu-id="be2dc-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2dc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2dc-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be2dc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2dc-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be2dc-150">INPUTS</span></span>

### <span data-ttu-id="be2dc-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="be2dc-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="be2dc-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be2dc-152">OUTPUTS</span></span>

### <span data-ttu-id="be2dc-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="be2dc-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="be2dc-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be2dc-154">NOTES</span></span>

## <span data-ttu-id="be2dc-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be2dc-155">RELATED LINKS</span></span>

[<span data-ttu-id="be2dc-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="be2dc-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


