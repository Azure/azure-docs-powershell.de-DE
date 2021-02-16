---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168049"
---
# <span data-ttu-id="03c9c-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="03c9c-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="03c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="03c9c-103">Erstellt eine neue CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="03c9c-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="03c9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03c9c-104">SYNTAX</span></span>

### <span data-ttu-id="03c9c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03c9c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c9c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c9c-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c9c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03c9c-107">DESCRIPTION</span></span>
<span data-ttu-id="03c9c-108">Die New-AzCdnOriginGroup erstellt eine neue Origin-Gruppe innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="03c9c-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="03c9c-109">Wenn dies die erste Ursprungsgruppe für den Endpunkt ist, muss auch die Eigenschaft "DefaultOriginGroup" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="03c9c-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="03c9c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03c9c-110">EXAMPLES</span></span>

### <span data-ttu-id="03c9c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03c9c-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="03c9c-112">Dieses Cmdlet erstellt eine neue Origin-Gruppe innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="03c9c-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="03c9c-113">Dabei werden die angegebenen Origin-IDs als Ursprung verwendet.</span><span class="sxs-lookup"><span data-stu-id="03c9c-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="03c9c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c9c-114">PARAMETERS</span></span>

### <span data-ttu-id="03c9c-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="03c9c-115">-CdnOriginGroup</span></span>
<span data-ttu-id="03c9c-116">Das CDN-Origin-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="03c9c-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="03c9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c9c-117">-DefaultProfile</span></span>
<span data-ttu-id="03c9c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03c9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c9c-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="03c9c-119">-EndpointName</span></span>
<span data-ttu-id="03c9c-120">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="03c9c-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="03c9c-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="03c9c-121">-OriginGroupName</span></span>
<span data-ttu-id="03c9c-122">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="03c9c-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="03c9c-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="03c9c-123">-OriginId</span></span>
<span data-ttu-id="03c9c-124">Azure CDN-Origin-Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="03c9c-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="03c9c-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="03c9c-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="03c9c-126">Die Anzahl von Sekunden zwischen Integritätstest.</span><span class="sxs-lookup"><span data-stu-id="03c9c-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="03c9c-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="03c9c-127">-ProbePath</span></span>
<span data-ttu-id="03c9c-128">Der Pfad relativ zum Ursprung, der zur Ermittlung der Integrität des Ursprungs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03c9c-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="03c9c-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="03c9c-129">-ProbeProtocol</span></span>
<span data-ttu-id="03c9c-130">Protokoll, das für integritätsintepunkt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="03c9c-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="03c9c-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="03c9c-131">-ProbeRequestType</span></span>
<span data-ttu-id="03c9c-132">Der Typ der von der Integritätsintepunktanforderung vorgenommenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="03c9c-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="03c9c-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="03c9c-133">-ProfileName</span></span>
<span data-ttu-id="03c9c-134">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="03c9c-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="03c9c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c9c-135">-ResourceGroupName</span></span>
<span data-ttu-id="03c9c-136">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="03c9c-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="03c9c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c9c-137">-Confirm</span></span>
<span data-ttu-id="03c9c-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03c9c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c9c-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03c9c-139">-WhatIf</span></span>
<span data-ttu-id="03c9c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03c9c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03c9c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03c9c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c9c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c9c-142">CommonParameters</span></span>
<span data-ttu-id="03c9c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c9c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c9c-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c9c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c9c-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03c9c-145">INPUTS</span></span>

### <span data-ttu-id="03c9c-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="03c9c-146">System.Object</span></span>

## <span data-ttu-id="03c9c-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03c9c-147">OUTPUTS</span></span>

### <span data-ttu-id="03c9c-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="03c9c-148">System.Object</span></span>

## <span data-ttu-id="03c9c-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03c9c-149">NOTES</span></span>

## <span data-ttu-id="03c9c-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03c9c-150">RELATED LINKS</span></span>
