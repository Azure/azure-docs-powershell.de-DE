---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473179"
---
# <span data-ttu-id="3c60f-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="3c60f-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="3c60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c60f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c60f-103">Aktualisiert die CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3c60f-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="3c60f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c60f-104">SYNTAX</span></span>

### <span data-ttu-id="3c60f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c60f-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c60f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c60f-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c60f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c60f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c60f-108">Set-AzCdnOriginGroup die angegebene Origin-Gruppe innerhalb des angegebenen Endpunkts aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3c60f-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="3c60f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c60f-109">EXAMPLES</span></span>

### <span data-ttu-id="3c60f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c60f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="3c60f-111">Dieses Cmdlet aktualisiert die Eigenschaft "ProbeIntervalInSeconds" in der Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3c60f-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="3c60f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c60f-112">PARAMETERS</span></span>

### <span data-ttu-id="3c60f-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="3c60f-113">-CdnOriginGroup</span></span>
<span data-ttu-id="3c60f-114">Das CdN-Origin-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c60f-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="3c60f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c60f-115">-DefaultProfile</span></span>
<span data-ttu-id="3c60f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c60f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c60f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3c60f-117">-EndpointName</span></span>
<span data-ttu-id="3c60f-118">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3c60f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3c60f-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="3c60f-119">-OriginGroupName</span></span>
<span data-ttu-id="3c60f-120">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3c60f-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="3c60f-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="3c60f-121">-OriginId</span></span>
<span data-ttu-id="3c60f-122">Azure CDN-Origin-Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="3c60f-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="3c60f-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3c60f-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="3c60f-124">Die Anzahl von Sekunden zwischen integritätsintepunkts.</span><span class="sxs-lookup"><span data-stu-id="3c60f-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="3c60f-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="3c60f-125">-ProbePath</span></span>
<span data-ttu-id="3c60f-126">Der Pfad relativ zum Ursprung, der zur Ermittlung der Integrität des Ursprungs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c60f-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="3c60f-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="3c60f-127">-ProbeProtocol</span></span>
<span data-ttu-id="3c60f-128">Protokoll, das für integritätsintepunkt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c60f-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="3c60f-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="3c60f-129">-ProbeRequestType</span></span>
<span data-ttu-id="3c60f-130">Der Typ der von der Integritätsintepunktanforderung vorgenommenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3c60f-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="3c60f-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3c60f-131">-ProfileName</span></span>
<span data-ttu-id="3c60f-132">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="3c60f-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3c60f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c60f-133">-ResourceGroupName</span></span>
<span data-ttu-id="3c60f-134">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="3c60f-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3c60f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c60f-135">-Confirm</span></span>
<span data-ttu-id="3c60f-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c60f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c60f-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c60f-137">-WhatIf</span></span>
<span data-ttu-id="3c60f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c60f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c60f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c60f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c60f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c60f-140">CommonParameters</span></span>
<span data-ttu-id="3c60f-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c60f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c60f-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c60f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c60f-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c60f-143">INPUTS</span></span>

### <span data-ttu-id="3c60f-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="3c60f-144">System.Object</span></span>

## <span data-ttu-id="3c60f-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c60f-145">OUTPUTS</span></span>

### <span data-ttu-id="3c60f-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="3c60f-146">System.Object</span></span>

## <span data-ttu-id="3c60f-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c60f-147">NOTES</span></span>

## <span data-ttu-id="3c60f-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c60f-148">RELATED LINKS</span></span>
