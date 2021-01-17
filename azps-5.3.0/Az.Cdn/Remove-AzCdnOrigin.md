---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470996"
---
# <span data-ttu-id="7f026-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7f026-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="7f026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f026-102">SYNOPSIS</span></span>
<span data-ttu-id="7f026-103">Entfernt einen CDN-Ursprung.</span><span class="sxs-lookup"><span data-stu-id="7f026-103">Removes a CDN origin</span></span>

## <span data-ttu-id="7f026-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f026-104">SYNTAX</span></span>

### <span data-ttu-id="7f026-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f026-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f026-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f026-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f026-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f026-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f026-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f026-108">DESCRIPTION</span></span>
<span data-ttu-id="7f026-109">Remove-AzCdnOrigin wird ein CDN-Ursprung vom angegebenen Endpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7f026-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="7f026-110">Wenn der Ursprung der einzige Ursprung innerhalb des angegebenen Endpunkts ist, kann der Löschvorgang fehlschlagen, da mindestens ein Ursprung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f026-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="7f026-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f026-111">EXAMPLES</span></span>

### <span data-ttu-id="7f026-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f026-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="7f026-113">Dieses Cmdlet entfernt den angegebenen Ursprung vom angegebenen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7f026-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="7f026-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f026-114">PARAMETERS</span></span>

### <span data-ttu-id="7f026-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7f026-115">-CdnOrigin</span></span>
<span data-ttu-id="7f026-116">Das CDN-Origin-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f026-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="7f026-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f026-117">-DefaultProfile</span></span>
<span data-ttu-id="7f026-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f026-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f026-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f026-119">-EndpointName</span></span>
<span data-ttu-id="7f026-120">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="7f026-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7f026-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="7f026-121">-OriginName</span></span>
<span data-ttu-id="7f026-122">Azure CDN-Origin-Name.</span><span class="sxs-lookup"><span data-stu-id="7f026-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="7f026-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f026-123">-PassThru</span></span>
<span data-ttu-id="7f026-124">Rückgabeobjekt bei Angabe</span><span class="sxs-lookup"><span data-stu-id="7f026-124">Return object if specified.</span></span>

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

### <span data-ttu-id="7f026-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7f026-125">-ProfileName</span></span>
<span data-ttu-id="7f026-126">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="7f026-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7f026-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f026-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f026-128">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="7f026-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7f026-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f026-129">-ResourceId</span></span>
<span data-ttu-id="7f026-130">Die Ressourcen-ID des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="7f026-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="7f026-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f026-131">-Confirm</span></span>
<span data-ttu-id="7f026-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f026-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f026-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f026-133">-WhatIf</span></span>
<span data-ttu-id="7f026-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f026-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f026-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f026-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f026-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f026-136">CommonParameters</span></span>
<span data-ttu-id="7f026-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f026-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f026-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f026-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f026-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f026-139">INPUTS</span></span>

### <span data-ttu-id="7f026-140">Keine</span><span class="sxs-lookup"><span data-stu-id="7f026-140">None</span></span>

## <span data-ttu-id="7f026-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f026-141">OUTPUTS</span></span>

### <span data-ttu-id="7f026-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f026-142">System.Boolean</span></span>

## <span data-ttu-id="7f026-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f026-143">NOTES</span></span>

## <span data-ttu-id="7f026-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f026-144">RELATED LINKS</span></span>
