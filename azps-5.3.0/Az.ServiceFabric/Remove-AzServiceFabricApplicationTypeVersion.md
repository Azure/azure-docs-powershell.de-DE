---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471795"
---
# <span data-ttu-id="e310b-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e310b-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="e310b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e310b-102">SYNOPSIS</span></span>
<span data-ttu-id="e310b-103">Remove Service fabric an application type version from the cluster.</span><span class="sxs-lookup"><span data-stu-id="e310b-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="e310b-104">Unterstützt nur ARM bereitgestellten Anwendungstypversionen.</span><span class="sxs-lookup"><span data-stu-id="e310b-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="e310b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e310b-105">SYNTAX</span></span>

### <span data-ttu-id="e310b-106">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="e310b-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e310b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e310b-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e310b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e310b-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e310b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e310b-109">DESCRIPTION</span></span>
<span data-ttu-id="e310b-110">Mit diesem Cmdlet wird eine Anwendungstypversion aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="e310b-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="e310b-111">Alle Anwendungen unter dieser Ressource müssen entfernt werden, bevor dieser Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e310b-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="e310b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e310b-112">EXAMPLES</span></span>

### <span data-ttu-id="e310b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e310b-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="e310b-114">In diesem Beispiel wird die Version "v1" vom Typ "testAppType" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e310b-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="e310b-115">Unter dieser Ressource gibt es Anwendungen, durch die der Befehl eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="e310b-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="e310b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e310b-116">PARAMETERS</span></span>

### <span data-ttu-id="e310b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e310b-117">-ClusterName</span></span>
<span data-ttu-id="e310b-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e310b-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e310b-119">-DefaultProfile</span></span>
<span data-ttu-id="e310b-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e310b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e310b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e310b-121">-Force</span></span>
<span data-ttu-id="e310b-122">"Ohne Eingabeaufforderung entfernen" aus.</span><span class="sxs-lookup"><span data-stu-id="e310b-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="e310b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e310b-123">-InputObject</span></span>
<span data-ttu-id="e310b-124">Die Ressourcenversionsressource des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="e310b-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e310b-125">-Name</span></span>
<span data-ttu-id="e310b-126">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="e310b-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e310b-127">-PassThru</span></span>
<span data-ttu-id="e310b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e310b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e310b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e310b-129">-ResourceGroupName</span></span>
<span data-ttu-id="e310b-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e310b-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e310b-131">-ResourceId</span></span>
<span data-ttu-id="e310b-132">Arm ResourceId der Anwendungstypversion.</span><span class="sxs-lookup"><span data-stu-id="e310b-132">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-133">-Version</span><span class="sxs-lookup"><span data-stu-id="e310b-133">-Version</span></span>
<span data-ttu-id="e310b-134">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="e310b-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e310b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e310b-135">-Confirm</span></span>
<span data-ttu-id="e310b-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e310b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e310b-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e310b-137">-WhatIf</span></span>
<span data-ttu-id="e310b-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e310b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e310b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e310b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e310b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e310b-140">CommonParameters</span></span>
<span data-ttu-id="e310b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e310b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e310b-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e310b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e310b-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e310b-143">INPUTS</span></span>

### <span data-ttu-id="e310b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e310b-144">System.String</span></span>

### <span data-ttu-id="e310b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e310b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="e310b-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e310b-146">OUTPUTS</span></span>

### <span data-ttu-id="e310b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e310b-147">System.Boolean</span></span>

## <span data-ttu-id="e310b-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e310b-148">NOTES</span></span>

## <span data-ttu-id="e310b-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e310b-149">RELATED LINKS</span></span>
