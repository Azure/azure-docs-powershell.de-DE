---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473182"
---
# <span data-ttu-id="2760d-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2760d-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="2760d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2760d-102">SYNOPSIS</span></span>
<span data-ttu-id="2760d-103">Entfernt eine CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2760d-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="2760d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2760d-104">SYNTAX</span></span>

### <span data-ttu-id="2760d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2760d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2760d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2760d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2760d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2760d-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2760d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2760d-108">DESCRIPTION</span></span>
<span data-ttu-id="2760d-109">Remove-AzCdnOriginGroup entfernt eine CDN-Origin-Gruppe vom angegebenen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2760d-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="2760d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2760d-110">EXAMPLES</span></span>

### <span data-ttu-id="2760d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2760d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="2760d-112">Mit diesem Cmdlet wird die angegebene Origin-Gruppe vom angegebenen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="2760d-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="2760d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2760d-113">PARAMETERS</span></span>

### <span data-ttu-id="2760d-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2760d-114">-CdnOriginGroup</span></span>
<span data-ttu-id="2760d-115">Das CDN-Origin-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="2760d-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="2760d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2760d-116">-DefaultProfile</span></span>
<span data-ttu-id="2760d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2760d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2760d-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2760d-118">-EndpointName</span></span>
<span data-ttu-id="2760d-119">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="2760d-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2760d-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="2760d-120">-OriginGroupName</span></span>
<span data-ttu-id="2760d-121">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2760d-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="2760d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2760d-122">-PassThru</span></span>
<span data-ttu-id="2760d-123">Rückgabeobjekt, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="2760d-123">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2760d-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2760d-124">-ProfileName</span></span>
<span data-ttu-id="2760d-125">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="2760d-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2760d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2760d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2760d-127">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="2760d-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2760d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2760d-128">-ResourceId</span></span>
<span data-ttu-id="2760d-129">Die Ressourcen-ID der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2760d-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2760d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2760d-130">-Confirm</span></span>
<span data-ttu-id="2760d-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2760d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2760d-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2760d-132">-WhatIf</span></span>
<span data-ttu-id="2760d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2760d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2760d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2760d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2760d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2760d-135">CommonParameters</span></span>
<span data-ttu-id="2760d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2760d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2760d-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2760d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2760d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2760d-138">INPUTS</span></span>

### <span data-ttu-id="2760d-139">Keine</span><span class="sxs-lookup"><span data-stu-id="2760d-139">None</span></span>

## <span data-ttu-id="2760d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2760d-140">OUTPUTS</span></span>

### <span data-ttu-id="2760d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2760d-141">System.Boolean</span></span>

## <span data-ttu-id="2760d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2760d-142">NOTES</span></span>

## <span data-ttu-id="2760d-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2760d-143">RELATED LINKS</span></span>
