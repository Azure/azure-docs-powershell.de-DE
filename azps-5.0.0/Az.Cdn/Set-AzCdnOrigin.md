---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177850"
---
# <span data-ttu-id="84486-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="84486-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="84486-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84486-102">SYNOPSIS</span></span>
<span data-ttu-id="84486-103">Aktualisiert einen CDN-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="84486-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="84486-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84486-104">SYNTAX</span></span>

### <span data-ttu-id="84486-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="84486-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84486-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="84486-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84486-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84486-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84486-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84486-108">DESCRIPTION</span></span>
<span data-ttu-id="84486-109">Das Cmdlet " **Satz-AzCdnOrigin** " aktualisiert einen Server mit Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="84486-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="84486-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84486-110">EXAMPLES</span></span>

## <span data-ttu-id="84486-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="84486-111">PARAMETERS</span></span>

### <span data-ttu-id="84486-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="84486-112">-CdnOrigin</span></span>
<span data-ttu-id="84486-113">Gibt den Ursprungsserver an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="84486-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="84486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84486-114">-DefaultProfile</span></span>
<span data-ttu-id="84486-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="84486-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84486-116">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="84486-116">-EndpointName</span></span>
<span data-ttu-id="84486-117">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="84486-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="84486-118">-Hostname</span><span class="sxs-lookup"><span data-stu-id="84486-118">-HostName</span></span>
<span data-ttu-id="84486-119">Azure CDN-Ursprungshost Name.</span><span class="sxs-lookup"><span data-stu-id="84486-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="84486-120">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="84486-120">-HttpPort</span></span>
<span data-ttu-id="84486-121">Azure CDN Origin-HTTP-Port.</span><span class="sxs-lookup"><span data-stu-id="84486-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="84486-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="84486-122">-HttpsPort</span></span>
<span data-ttu-id="84486-123">Azure CDN-Ursprungs HTTPS-Port.</span><span class="sxs-lookup"><span data-stu-id="84486-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="84486-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="84486-124">-OriginHostHeader</span></span>
<span data-ttu-id="84486-125">Azure CDN-Ursprungshost Header.</span><span class="sxs-lookup"><span data-stu-id="84486-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="84486-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="84486-126">-OriginName</span></span>
<span data-ttu-id="84486-127">Azure CDN-Ursprungsname.</span><span class="sxs-lookup"><span data-stu-id="84486-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="84486-128">-Priorität</span><span class="sxs-lookup"><span data-stu-id="84486-128">-Priority</span></span>
<span data-ttu-id="84486-129">Azure CDN-Ursprungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="84486-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="84486-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="84486-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="84486-131">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="84486-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="84486-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="84486-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="84486-133">Azure CDN Origin-Speicherort für private Links.</span><span class="sxs-lookup"><span data-stu-id="84486-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="84486-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="84486-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="84486-135">Azure CDN Origin-Ressourcen-ID für private Links.</span><span class="sxs-lookup"><span data-stu-id="84486-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="84486-136">-Profilname</span><span class="sxs-lookup"><span data-stu-id="84486-136">-ProfileName</span></span>
<span data-ttu-id="84486-137">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="84486-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="84486-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84486-138">-ResourceGroupName</span></span>
<span data-ttu-id="84486-139">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="84486-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="84486-140">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="84486-140">-Weight</span></span>
<span data-ttu-id="84486-141">Azure CDN-Ursprungs Gewicht.</span><span class="sxs-lookup"><span data-stu-id="84486-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="84486-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84486-142">-Confirm</span></span>
<span data-ttu-id="84486-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84486-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84486-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84486-144">-WhatIf</span></span>
<span data-ttu-id="84486-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84486-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84486-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84486-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84486-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84486-147">CommonParameters</span></span>
<span data-ttu-id="84486-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84486-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84486-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84486-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84486-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84486-150">INPUTS</span></span>

### <span data-ttu-id="84486-151">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="84486-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="84486-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84486-152">OUTPUTS</span></span>

### <span data-ttu-id="84486-153">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="84486-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="84486-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="84486-154">NOTES</span></span>

## <span data-ttu-id="84486-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84486-155">RELATED LINKS</span></span>

[<span data-ttu-id="84486-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="84486-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


