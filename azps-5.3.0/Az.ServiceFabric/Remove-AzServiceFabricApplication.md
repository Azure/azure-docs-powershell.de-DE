---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471792"
---
# <span data-ttu-id="66c93-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="66c93-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="66c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c93-102">SYNOPSIS</span></span>
<span data-ttu-id="66c93-103">Entfernen Sie eine Anwendung aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="66c93-103">Remove an application from the cluster.</span></span> <span data-ttu-id="66c93-104">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="66c93-104">This will remove all the services under the application.</span></span> <span data-ttu-id="66c93-105">Unterstützt nur ARM bereitgestellten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="66c93-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="66c93-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66c93-106">SYNTAX</span></span>

### <span data-ttu-id="66c93-107">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="66c93-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c93-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66c93-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c93-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="66c93-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c93-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66c93-110">DESCRIPTION</span></span>
<span data-ttu-id="66c93-111">Mit diesem Cmdlet wird eine Anwendung aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="66c93-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="66c93-112">Dadurch werden alle Dienste, sofern eines der Dienste, unter der Anwendungsressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="66c93-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="66c93-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66c93-113">EXAMPLES</span></span>

### <span data-ttu-id="66c93-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66c93-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="66c93-115">In diesem Beispiel wird die Anwendung "testApp" unter der Ressourcengruppe "testRG" und dem Cluster "testCluster" entfernt.</span><span class="sxs-lookup"><span data-stu-id="66c93-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="66c93-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66c93-116">PARAMETERS</span></span>

### <span data-ttu-id="66c93-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="66c93-117">-ClusterName</span></span>
<span data-ttu-id="66c93-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="66c93-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="66c93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c93-119">-DefaultProfile</span></span>
<span data-ttu-id="66c93-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66c93-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c93-121">-Force</span><span class="sxs-lookup"><span data-stu-id="66c93-121">-Force</span></span>
<span data-ttu-id="66c93-122">"Ohne Eingabeaufforderung entfernen" aus.</span><span class="sxs-lookup"><span data-stu-id="66c93-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="66c93-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66c93-123">-InputObject</span></span>
<span data-ttu-id="66c93-124">Die Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="66c93-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66c93-125">-Name</span><span class="sxs-lookup"><span data-stu-id="66c93-125">-Name</span></span>
<span data-ttu-id="66c93-126">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="66c93-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c93-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c93-127">-PassThru</span></span>
<span data-ttu-id="66c93-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="66c93-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="66c93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c93-129">-ResourceGroupName</span></span>
<span data-ttu-id="66c93-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66c93-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="66c93-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c93-131">-ResourceId</span></span>
<span data-ttu-id="66c93-132">Arm ResourceId der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66c93-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="66c93-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66c93-133">-Confirm</span></span>
<span data-ttu-id="66c93-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66c93-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c93-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="66c93-135">-WhatIf</span></span>
<span data-ttu-id="66c93-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66c93-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c93-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66c93-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c93-138">CommonParameters</span></span>
<span data-ttu-id="66c93-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c93-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66c93-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c93-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66c93-141">INPUTS</span></span>

### <span data-ttu-id="66c93-142">System.String</span><span class="sxs-lookup"><span data-stu-id="66c93-142">System.String</span></span>

### <span data-ttu-id="66c93-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="66c93-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="66c93-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66c93-144">OUTPUTS</span></span>

### <span data-ttu-id="66c93-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66c93-145">System.Boolean</span></span>

## <span data-ttu-id="66c93-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66c93-146">NOTES</span></span>

## <span data-ttu-id="66c93-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66c93-147">RELATED LINKS</span></span>
