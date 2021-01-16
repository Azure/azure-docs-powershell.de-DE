---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306632"
---
# <span data-ttu-id="3afaf-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3afaf-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="3afaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3afaf-102">SYNOPSIS</span></span>
<span data-ttu-id="3afaf-103">Erstellt einen neuen CDN-Ursprung.</span><span class="sxs-lookup"><span data-stu-id="3afaf-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="3afaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3afaf-104">SYNTAX</span></span>

### <span data-ttu-id="3afaf-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3afaf-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3afaf-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="3afaf-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3afaf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3afaf-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3afaf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3afaf-108">DESCRIPTION</span></span>
<span data-ttu-id="3afaf-109">Die New-AzCdnOrigin erstellt einen neuen CDN-Ursprung innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3afaf-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="3afaf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3afaf-110">EXAMPLES</span></span>

### <span data-ttu-id="3afaf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3afaf-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="3afaf-112">Dieses Cmdlet erstellt einen neuen CDN-Ursprung für den angegebenen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="3afaf-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="3afaf-113">Dabei wird der bereitgestellte Hostname als Ursprung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3afaf-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="3afaf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3afaf-114">PARAMETERS</span></span>

### <span data-ttu-id="3afaf-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3afaf-115">-CdnOrigin</span></span>
<span data-ttu-id="3afaf-116">Das CDN-Origin-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3afaf-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="3afaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afaf-117">-DefaultProfile</span></span>
<span data-ttu-id="3afaf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3afaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3afaf-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3afaf-119">-EndpointName</span></span>
<span data-ttu-id="3afaf-120">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3afaf-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3afaf-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="3afaf-121">-HostName</span></span>
<span data-ttu-id="3afaf-122">Hostname des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="3afaf-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="3afaf-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="3afaf-123">-HttpPort</span></span>
<span data-ttu-id="3afaf-124">Httpport des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="3afaf-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="3afaf-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="3afaf-125">-HttpsPort</span></span>
<span data-ttu-id="3afaf-126">Https-Port des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="3afaf-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="3afaf-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="3afaf-127">-OriginHostHeader</span></span>
<span data-ttu-id="3afaf-128">Azure CDN-Origin-Hostheader.</span><span class="sxs-lookup"><span data-stu-id="3afaf-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="3afaf-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="3afaf-129">-OriginName</span></span>
<span data-ttu-id="3afaf-130">Azure CDN-Origin-Name.</span><span class="sxs-lookup"><span data-stu-id="3afaf-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="3afaf-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="3afaf-131">-Priority</span></span>
<span data-ttu-id="3afaf-132">Azure CDN-Origin-Priorität.</span><span class="sxs-lookup"><span data-stu-id="3afaf-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="3afaf-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="3afaf-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="3afaf-134">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung eingeschlossen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3afaf-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="3afaf-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="3afaf-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="3afaf-136">Speicherort für private Azure CDN-Origin-Links.</span><span class="sxs-lookup"><span data-stu-id="3afaf-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="3afaf-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="3afaf-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="3afaf-138">Ressourcen-ID für privaten Link des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="3afaf-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="3afaf-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3afaf-139">-ProfileName</span></span>
<span data-ttu-id="3afaf-140">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="3afaf-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3afaf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afaf-141">-ResourceGroupName</span></span>
<span data-ttu-id="3afaf-142">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="3afaf-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3afaf-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="3afaf-143">-Weight</span></span>
<span data-ttu-id="3afaf-144">Azure CDN Origin Weight.</span><span class="sxs-lookup"><span data-stu-id="3afaf-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="3afaf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3afaf-145">-Confirm</span></span>
<span data-ttu-id="3afaf-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3afaf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3afaf-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3afaf-147">-WhatIf</span></span>
<span data-ttu-id="3afaf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3afaf-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3afaf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3afaf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3afaf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afaf-150">CommonParameters</span></span>
<span data-ttu-id="3afaf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afaf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afaf-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3afaf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afaf-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3afaf-153">INPUTS</span></span>

### <span data-ttu-id="3afaf-154">Keine</span><span class="sxs-lookup"><span data-stu-id="3afaf-154">None</span></span>

## <span data-ttu-id="3afaf-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3afaf-155">OUTPUTS</span></span>

### <span data-ttu-id="3afaf-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="3afaf-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="3afaf-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3afaf-157">NOTES</span></span>

## <span data-ttu-id="3afaf-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3afaf-158">RELATED LINKS</span></span>
