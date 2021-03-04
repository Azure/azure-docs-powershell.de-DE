---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: a954b6c259b9e793ca4e35e99ecb4c710ab7a4e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919024"
---
# <span data-ttu-id="4f574-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4f574-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="4f574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f574-102">SYNOPSIS</span></span>
<span data-ttu-id="4f574-103">Entfernt eine CDN-Ursprungsgruppe</span><span class="sxs-lookup"><span data-stu-id="4f574-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="4f574-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f574-104">SYNTAX</span></span>

### <span data-ttu-id="4f574-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f574-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f574-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f574-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f574-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f574-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f574-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f574-108">DESCRIPTION</span></span>
<span data-ttu-id="4f574-109">Remove-AzCdnOriginGroup wird eine CDN-Ursprungsgruppe vom angegebenen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="4f574-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="4f574-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f574-110">EXAMPLES</span></span>

### <span data-ttu-id="4f574-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f574-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="4f574-112">Mit diesem Cmdlet wird die angegebene Ursprungsgruppe vom angegebenen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="4f574-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="4f574-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f574-113">PARAMETERS</span></span>

### <span data-ttu-id="4f574-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4f574-114">-CdnOriginGroup</span></span>
<span data-ttu-id="4f574-115">Das CDN-Ursprungsgruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="4f574-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="4f574-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f574-116">-DefaultProfile</span></span>
<span data-ttu-id="4f574-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f574-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f574-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f574-118">-EndpointName</span></span>
<span data-ttu-id="4f574-119">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="4f574-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4f574-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="4f574-120">-OriginGroupName</span></span>
<span data-ttu-id="4f574-121">Azure CDN-Ursprungsgruppenname.</span><span class="sxs-lookup"><span data-stu-id="4f574-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="4f574-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f574-122">-PassThru</span></span>
<span data-ttu-id="4f574-123">Rückgabeobjekt, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="4f574-123">Return object if specified.</span></span>

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

### <span data-ttu-id="4f574-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4f574-124">-ProfileName</span></span>
<span data-ttu-id="4f574-125">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="4f574-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4f574-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f574-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f574-127">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="4f574-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4f574-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f574-128">-ResourceId</span></span>
<span data-ttu-id="4f574-129">Die Ressourcen-ID der Azure CDN-Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4f574-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="4f574-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f574-130">-Confirm</span></span>
<span data-ttu-id="4f574-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f574-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f574-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f574-132">-WhatIf</span></span>
<span data-ttu-id="4f574-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f574-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f574-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f574-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f574-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f574-135">CommonParameters</span></span>
<span data-ttu-id="4f574-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f574-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f574-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f574-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f574-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f574-138">INPUTS</span></span>

### <span data-ttu-id="4f574-139">Keine</span><span class="sxs-lookup"><span data-stu-id="4f574-139">None</span></span>

## <span data-ttu-id="4f574-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f574-140">OUTPUTS</span></span>

### <span data-ttu-id="4f574-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f574-141">System.Boolean</span></span>

## <span data-ttu-id="4f574-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4f574-142">NOTES</span></span>

## <span data-ttu-id="4f574-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4f574-143">RELATED LINKS</span></span>
