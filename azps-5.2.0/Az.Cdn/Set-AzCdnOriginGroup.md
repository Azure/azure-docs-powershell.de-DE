---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303811"
---
# <span data-ttu-id="fd6b3-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="fd6b3-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="fd6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6b3-103">Aktualisiert die CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="fd6b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd6b3-104">SYNTAX</span></span>

### <span data-ttu-id="fd6b3-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd6b3-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd6b3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6b3-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd6b3-107">DESCRIPTION</span></span>
<span data-ttu-id="fd6b3-108">Set-AzCdnOriginGroup die angegebene Origin-Gruppe innerhalb des angegebenen Endpunkts aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="fd6b3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd6b3-109">EXAMPLES</span></span>

### <span data-ttu-id="fd6b3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd6b3-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="fd6b3-111">Dieses Cmdlet aktualisiert die Eigenschaft "ProbeIntervalInSeconds" in der Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="fd6b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd6b3-112">PARAMETERS</span></span>

### <span data-ttu-id="fd6b3-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="fd6b3-113">-CdnOriginGroup</span></span>
<span data-ttu-id="fd6b3-114">Das CDN-Origin-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="fd6b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6b3-115">-DefaultProfile</span></span>
<span data-ttu-id="fd6b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd6b3-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fd6b3-117">-EndpointName</span></span>
<span data-ttu-id="fd6b3-118">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fd6b3-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6b3-119">-OriginGroupName</span></span>
<span data-ttu-id="fd6b3-120">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="fd6b3-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="fd6b3-121">-OriginId</span></span>
<span data-ttu-id="fd6b3-122">Azure CDN-Origin-Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="fd6b3-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fd6b3-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="fd6b3-124">Die Anzahl von Sekunden zwischen integritätsintepunkts.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="fd6b3-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="fd6b3-125">-ProbePath</span></span>
<span data-ttu-id="fd6b3-126">Der Pfad relativ zum Ursprung, der verwendet wird, um die Integrität des Ursprungs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="fd6b3-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="fd6b3-127">-ProbeProtocol</span></span>
<span data-ttu-id="fd6b3-128">Protokoll, das für integritätsintepunkt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="fd6b3-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="fd6b3-129">-ProbeRequestType</span></span>
<span data-ttu-id="fd6b3-130">Der Typ der von der Integritätsintepunktanforderung vorgenommenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="fd6b3-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fd6b3-131">-ProfileName</span></span>
<span data-ttu-id="fd6b3-132">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fd6b3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6b3-133">-ResourceGroupName</span></span>
<span data-ttu-id="fd6b3-134">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="fd6b3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd6b3-135">-Confirm</span></span>
<span data-ttu-id="fd6b3-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6b3-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd6b3-137">-WhatIf</span></span>
<span data-ttu-id="fd6b3-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6b3-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6b3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6b3-140">CommonParameters</span></span>
<span data-ttu-id="fd6b3-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6b3-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd6b3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6b3-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd6b3-143">INPUTS</span></span>

### <span data-ttu-id="fd6b3-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="fd6b3-144">System.Object</span></span>

## <span data-ttu-id="fd6b3-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd6b3-145">OUTPUTS</span></span>

### <span data-ttu-id="fd6b3-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="fd6b3-146">System.Object</span></span>

## <span data-ttu-id="fd6b3-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd6b3-147">NOTES</span></span>

## <span data-ttu-id="fd6b3-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd6b3-148">RELATED LINKS</span></span>
