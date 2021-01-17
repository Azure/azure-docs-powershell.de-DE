---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471774"
---
# <span data-ttu-id="9baa5-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="9baa5-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="9baa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9baa5-102">SYNOPSIS</span></span>
<span data-ttu-id="9baa5-103">Entfernen sie einen Dienst aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="9baa5-103">Remove a service from the cluster.</span></span> <span data-ttu-id="9baa5-104">Unterstützt nur ARM bereitgestellten Dienste.</span><span class="sxs-lookup"><span data-stu-id="9baa5-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="9baa5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9baa5-105">SYNTAX</span></span>

### <span data-ttu-id="9baa5-106">ByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="9baa5-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9baa5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9baa5-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9baa5-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9baa5-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9baa5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9baa5-109">DESCRIPTION</span></span>
<span data-ttu-id="9baa5-110">Mit diesem Cmdlet wird ein Dienst aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="9baa5-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="9baa5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9baa5-111">EXAMPLES</span></span>

### <span data-ttu-id="9baa5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9baa5-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="9baa5-113">In diesem Beispiel wird der Dienst "testApp~testService1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="9baa5-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="9baa5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9baa5-114">PARAMETERS</span></span>

### <span data-ttu-id="9baa5-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9baa5-115">-ApplicationName</span></span>
<span data-ttu-id="9baa5-116">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9baa5-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9baa5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9baa5-117">-ClusterName</span></span>
<span data-ttu-id="9baa5-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="9baa5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9baa5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9baa5-119">-DefaultProfile</span></span>
<span data-ttu-id="9baa5-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9baa5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9baa5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9baa5-121">-Force</span></span>
<span data-ttu-id="9baa5-122">"Ohne Aufforderung entfernen" aus.</span><span class="sxs-lookup"><span data-stu-id="9baa5-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="9baa5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9baa5-123">-InputObject</span></span>
<span data-ttu-id="9baa5-124">Die Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="9baa5-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9baa5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9baa5-125">-Name</span></span>
<span data-ttu-id="9baa5-126">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9baa5-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9baa5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9baa5-127">-PassThru</span></span>
<span data-ttu-id="9baa5-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9baa5-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9baa5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9baa5-129">-ResourceGroupName</span></span>
<span data-ttu-id="9baa5-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9baa5-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9baa5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9baa5-131">-ResourceId</span></span>
<span data-ttu-id="9baa5-132">Arm ResourceId des Diensts.</span><span class="sxs-lookup"><span data-stu-id="9baa5-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="9baa5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9baa5-133">-Confirm</span></span>
<span data-ttu-id="9baa5-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9baa5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9baa5-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9baa5-135">-WhatIf</span></span>
<span data-ttu-id="9baa5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9baa5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9baa5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9baa5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9baa5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9baa5-138">CommonParameters</span></span>
<span data-ttu-id="9baa5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9baa5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9baa5-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9baa5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9baa5-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9baa5-141">INPUTS</span></span>

### <span data-ttu-id="9baa5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9baa5-142">System.String</span></span>

### <span data-ttu-id="9baa5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="9baa5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="9baa5-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9baa5-144">OUTPUTS</span></span>

### <span data-ttu-id="9baa5-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9baa5-145">System.Boolean</span></span>

## <span data-ttu-id="9baa5-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9baa5-146">NOTES</span></span>

## <span data-ttu-id="9baa5-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9baa5-147">RELATED LINKS</span></span>
