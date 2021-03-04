---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 34d5b4dccb43f604625652f1c39b2250926058d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943123"
---
# <span data-ttu-id="94f07-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="94f07-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="94f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f07-102">SYNOPSIS</span></span>
<span data-ttu-id="94f07-103">Erstellt eine neue CDN-Ursprungsgruppe</span><span class="sxs-lookup"><span data-stu-id="94f07-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="94f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94f07-104">SYNTAX</span></span>

### <span data-ttu-id="94f07-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="94f07-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94f07-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94f07-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f07-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94f07-107">DESCRIPTION</span></span>
<span data-ttu-id="94f07-108">Die New-AzCdnOriginGroup erstellt eine neue Ursprungsgruppe innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="94f07-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="94f07-109">Wenn dies die erste Ursprungsgruppe für Endpunkt ist, muss auch die DefaultOriginGroup-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="94f07-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="94f07-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94f07-110">EXAMPLES</span></span>

### <span data-ttu-id="94f07-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94f07-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="94f07-112">Dieses Cmdlet erstellt eine neue Ursprungsgruppe innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="94f07-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="94f07-113">Dabei werden die angegebenen Ursprungs-IDn als Herkunftssatz verwendet.</span><span class="sxs-lookup"><span data-stu-id="94f07-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="94f07-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94f07-114">PARAMETERS</span></span>

### <span data-ttu-id="94f07-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="94f07-115">-CdnOriginGroup</span></span>
<span data-ttu-id="94f07-116">Das CDN-Ursprungsgruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="94f07-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f07-117">-DefaultProfile</span></span>
<span data-ttu-id="94f07-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94f07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f07-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="94f07-119">-EndpointName</span></span>
<span data-ttu-id="94f07-120">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="94f07-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="94f07-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="94f07-121">-OriginGroupName</span></span>
<span data-ttu-id="94f07-122">Azure CDN-Ursprungsgruppenname.</span><span class="sxs-lookup"><span data-stu-id="94f07-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="94f07-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="94f07-123">-OriginId</span></span>
<span data-ttu-id="94f07-124">Azure CDN-Ursprungsgruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="94f07-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="94f07-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="94f07-126">Die Anzahl der Sekunden zwischen Integritätssonden.</span><span class="sxs-lookup"><span data-stu-id="94f07-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="94f07-127">-ProbePath</span></span>
<span data-ttu-id="94f07-128">Der Pfad relativ zum Ursprung, der verwendet wird, um den Zustand des Ursprungs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="94f07-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="94f07-129">-ProbeProtocol</span></span>
<span data-ttu-id="94f07-130">Protokoll, das für die Integritätsprobe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f07-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="94f07-131">-ProbeRequestType</span></span>
<span data-ttu-id="94f07-132">Der Typ der Integritätstestanforderung, die gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="94f07-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f07-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="94f07-133">-ProfileName</span></span>
<span data-ttu-id="94f07-134">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="94f07-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="94f07-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f07-135">-ResourceGroupName</span></span>
<span data-ttu-id="94f07-136">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="94f07-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="94f07-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94f07-137">-Confirm</span></span>
<span data-ttu-id="94f07-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94f07-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f07-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f07-139">-WhatIf</span></span>
<span data-ttu-id="94f07-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94f07-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94f07-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94f07-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f07-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f07-142">CommonParameters</span></span>
<span data-ttu-id="94f07-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f07-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f07-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94f07-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f07-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94f07-145">INPUTS</span></span>

### <span data-ttu-id="94f07-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="94f07-146">System.Object</span></span>

## <span data-ttu-id="94f07-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94f07-147">OUTPUTS</span></span>

### <span data-ttu-id="94f07-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="94f07-148">System.Object</span></span>

## <span data-ttu-id="94f07-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94f07-149">NOTES</span></span>

## <span data-ttu-id="94f07-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94f07-150">RELATED LINKS</span></span>
