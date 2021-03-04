---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918424"
---
# <span data-ttu-id="8478f-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="8478f-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="8478f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8478f-102">SYNOPSIS</span></span>
<span data-ttu-id="8478f-103">Aktualisieren sie einen Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="8478f-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="8478f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8478f-104">SYNTAX</span></span>

### <span data-ttu-id="8478f-105">RouteServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8478f-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8478f-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8478f-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8478f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8478f-107">DESCRIPTION</span></span>
<span data-ttu-id="8478f-108">Das **Update-AzRouteServer-Cmdlet** wechselt den Branch-to-Branch-Datenverkehr zu einem Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="8478f-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="8478f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8478f-109">EXAMPLES</span></span>

### <span data-ttu-id="8478f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8478f-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="8478f-111">So aktivieren Sie den Verzweigungsverkehr für den Routenserver.</span><span class="sxs-lookup"><span data-stu-id="8478f-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="8478f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8478f-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="8478f-113">So deaktivieren Sie den Verzweigungs-zu-Verzweigungsverkehr für den Routenserver.</span><span class="sxs-lookup"><span data-stu-id="8478f-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="8478f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8478f-114">PARAMETERS</span></span>

### <span data-ttu-id="8478f-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="8478f-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="8478f-116">Kennzeichnen Sie, um den Verzweigungsverkehr für den Routenserver zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8478f-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="8478f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8478f-117">-DefaultProfile</span></span>
<span data-ttu-id="8478f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8478f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8478f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8478f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8478f-120">Der Ressourcengruppenname des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="8478f-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="8478f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8478f-121">-ResourceId</span></span>
<span data-ttu-id="8478f-122">ResourceId des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="8478f-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="8478f-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="8478f-123">-RouteServerName</span></span>
<span data-ttu-id="8478f-124">Der Name des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="8478f-124">The name of the route server.</span></span>

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

### <span data-ttu-id="8478f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8478f-125">-Confirm</span></span>
<span data-ttu-id="8478f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8478f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8478f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8478f-127">-WhatIf</span></span>
<span data-ttu-id="8478f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8478f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8478f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8478f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8478f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8478f-130">CommonParameters</span></span>
<span data-ttu-id="8478f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8478f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8478f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8478f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8478f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8478f-133">INPUTS</span></span>

### <span data-ttu-id="8478f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8478f-134">System.String</span></span>

## <span data-ttu-id="8478f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8478f-135">OUTPUTS</span></span>

### <span data-ttu-id="8478f-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="8478f-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="8478f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8478f-137">NOTES</span></span>

## <span data-ttu-id="8478f-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8478f-138">RELATED LINKS</span></span>
