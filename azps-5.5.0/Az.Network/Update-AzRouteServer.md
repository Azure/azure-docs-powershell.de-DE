---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 9f00ccfb01cd6e6b0d80b120364f8ac0c81daae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151361"
---
# <span data-ttu-id="37ba6-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="37ba6-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="37ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="37ba6-103">Aktualisieren Sie einen Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="37ba6-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="37ba6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37ba6-104">SYNTAX</span></span>

### <span data-ttu-id="37ba6-105">RouteServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37ba6-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ba6-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37ba6-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ba6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="37ba6-108">Mit **dem Cmdlet "Update-AzRouteServer"** wird der Verzweigungs-zu-Verzweigungsverkehr auf einen Azure RouteServer umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37ba6-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="37ba6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37ba6-109">EXAMPLES</span></span>

### <span data-ttu-id="37ba6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37ba6-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="37ba6-111">So aktivieren Sie Verzweigungs-zu-Verzweigungsverkehr für den Routeserver.</span><span class="sxs-lookup"><span data-stu-id="37ba6-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="37ba6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37ba6-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="37ba6-113">So deaktivieren Sie den Verzweigungs-zu-Verzweigungsverkehr für den Routeserver.</span><span class="sxs-lookup"><span data-stu-id="37ba6-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="37ba6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37ba6-114">PARAMETERS</span></span>

### <span data-ttu-id="37ba6-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="37ba6-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="37ba6-116">Kennzeichnen, um Verzweigungs-zu-Verzweigungsdatenverkehr für den Routeserver zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="37ba6-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="37ba6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ba6-117">-DefaultProfile</span></span>
<span data-ttu-id="37ba6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37ba6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ba6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ba6-119">-ResourceGroupName</span></span>
<span data-ttu-id="37ba6-120">Der Ressourcengruppenname des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="37ba6-120">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ba6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37ba6-121">-ResourceId</span></span>
<span data-ttu-id="37ba6-122">ResourceId des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="37ba6-122">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ba6-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="37ba6-123">-RouteServerName</span></span>
<span data-ttu-id="37ba6-124">Der Name des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="37ba6-124">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ba6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37ba6-125">-Confirm</span></span>
<span data-ttu-id="37ba6-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37ba6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ba6-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37ba6-127">-WhatIf</span></span>
<span data-ttu-id="37ba6-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37ba6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ba6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37ba6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ba6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ba6-130">CommonParameters</span></span>
<span data-ttu-id="37ba6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ba6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ba6-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37ba6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ba6-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37ba6-133">INPUTS</span></span>

### <span data-ttu-id="37ba6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="37ba6-134">System.String</span></span>

## <span data-ttu-id="37ba6-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37ba6-135">OUTPUTS</span></span>

### <span data-ttu-id="37ba6-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="37ba6-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="37ba6-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37ba6-137">NOTES</span></span>

## <span data-ttu-id="37ba6-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37ba6-138">RELATED LINKS</span></span>
