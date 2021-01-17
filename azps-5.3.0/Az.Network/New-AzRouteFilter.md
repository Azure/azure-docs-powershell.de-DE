---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459883"
---
# <span data-ttu-id="2d02d-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d02d-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="2d02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d02d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d02d-103">Erstellt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="2d02d-103">Creates a route filter.</span></span>

## <span data-ttu-id="2d02d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d02d-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d02d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d02d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d02d-106">Das New-AzRouteFilter erstellt einen Azure-Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="2d02d-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="2d02d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d02d-107">EXAMPLES</span></span>

### <span data-ttu-id="2d02d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d02d-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="2d02d-109">Der Befehl erstellt einen neuen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="2d02d-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="2d02d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d02d-110">PARAMETERS</span></span>

### <span data-ttu-id="2d02d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d02d-111">-AsJob</span></span>
<span data-ttu-id="2d02d-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2d02d-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d02d-113">-DefaultProfile</span></span>
<span data-ttu-id="2d02d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d02d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d02d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d02d-115">-Force</span></span>
<span data-ttu-id="2d02d-116">Gibt an, dass mit diesem Cmdlet eine Routentabelle erstellt wird, auch wenn bereits ein Routenfilter mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2d02d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2d02d-117">-Location</span></span>
<span data-ttu-id="2d02d-118">Gibt die Azure-Region an, in der dieses Cmdlet einen Routenfilter erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d02d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2d02d-119">-Name</span></span>
<span data-ttu-id="2d02d-120">Gibt einen Namen für den Routenfilter an.</span><span class="sxs-lookup"><span data-stu-id="2d02d-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d02d-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d02d-122">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet einen Routenfilter erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d02d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="2d02d-123">-Rule</span></span>
<span data-ttu-id="2d02d-124">Gibt ein Array von Routenfilterregelobjekten an, die dem Routenfilter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2d02d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d02d-125">-Tag</span></span>
<span data-ttu-id="2d02d-126">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2d02d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d02d-127">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2d02d-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d02d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d02d-128">-Confirm</span></span>
<span data-ttu-id="2d02d-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d02d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d02d-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d02d-130">-WhatIf</span></span>
<span data-ttu-id="2d02d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d02d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d02d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d02d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d02d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d02d-133">CommonParameters</span></span>
<span data-ttu-id="2d02d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d02d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d02d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d02d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d02d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d02d-136">INPUTS</span></span>

### <span data-ttu-id="2d02d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2d02d-137">System.String</span></span>

### <span data-ttu-id="2d02d-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="2d02d-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="2d02d-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d02d-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d02d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d02d-140">OUTPUTS</span></span>

### <span data-ttu-id="2d02d-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d02d-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2d02d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d02d-142">NOTES</span></span>
<span data-ttu-id="2d02d-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="2d02d-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2d02d-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d02d-144">RELATED LINKS</span></span>

[<span data-ttu-id="2d02d-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d02d-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2d02d-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d02d-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="2d02d-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d02d-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="2d02d-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d02d-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2d02d-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d02d-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2d02d-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d02d-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2d02d-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d02d-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2d02d-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d02d-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
