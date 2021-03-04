---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932976"
---
# <span data-ttu-id="0aa7d-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0aa7d-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="0aa7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa7d-103">Erstellt einen Dienst unter der angegebenen Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="0aa7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0aa7d-104">SYNTAX</span></span>

### <span data-ttu-id="0aa7d-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="0aa7d-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa7d-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="0aa7d-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa7d-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa7d-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa7d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aa7d-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa7d-109">Das **Cmdlet New-AzDeploymentManagerService** erstellt einen Dienst unter einer Diensttopologie und gibt ein -Objekt zurück, das den Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="0aa7d-110">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="0aa7d-111">Das Cmdlet gibt ein Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="0aa7d-112">Sie können dieses Objekt lokal ändern und dann Änderungen auf den Dienst anwenden, indem Sie das cmdlet Set-AzDeploymentManagerService verwenden.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="0aa7d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0aa7d-113">EXAMPLES</span></span>

### <span data-ttu-id="0aa7d-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0aa7d-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="0aa7d-115">Erstellt einen neuen Dienst mit dem Namen ContosoService1 unter Diensttopologie ContosoServiceTopology in Der Ressourcengruppe ContosoResourceGroup am Speicherort Zentral USA.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="0aa7d-116">Die TargetLocation-Eigenschaft gibt an, dass der Dienst ContosoService1 in der Region Ost-USA im angegebenen Abonnement bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="0aa7d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0aa7d-117">PARAMETERS</span></span>

### <span data-ttu-id="0aa7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa7d-118">-DefaultProfile</span></span>
<span data-ttu-id="0aa7d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa7d-120">-Location</span><span class="sxs-lookup"><span data-stu-id="0aa7d-120">-Location</span></span>
<span data-ttu-id="0aa7d-121">Der Speicherort der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0aa7d-122">-Name</span></span>
<span data-ttu-id="0aa7d-123">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa7d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0aa7d-125">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="0aa7d-126">-ServiceTopologyId</span></span>
<span data-ttu-id="0aa7d-127">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="0aa7d-128">-ServiceTopologyName</span></span>
<span data-ttu-id="0aa7d-129">Der Name der Diensttopologie, zu der dieser Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="0aa7d-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="0aa7d-131">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="0aa7d-132">-Tag</span></span>
<span data-ttu-id="0aa7d-133">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="0aa7d-134">-TargetLocation</span></span>
<span data-ttu-id="0aa7d-135">Bestimmt den Speicherort, an dem Ressourcen unter dem Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0aa7d-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="0aa7d-137">Bestimmt das Abonnement, für das Ressourcen unter dem Dienst bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa7d-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0aa7d-138">-Confirm</span></span>
<span data-ttu-id="0aa7d-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa7d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa7d-140">-WhatIf</span></span>
<span data-ttu-id="0aa7d-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa7d-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa7d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa7d-143">CommonParameters</span></span>
<span data-ttu-id="0aa7d-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa7d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa7d-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0aa7d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa7d-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0aa7d-146">INPUTS</span></span>

### <span data-ttu-id="0aa7d-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0aa7d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0aa7d-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0aa7d-148">OUTPUTS</span></span>

### <span data-ttu-id="0aa7d-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="0aa7d-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="0aa7d-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0aa7d-150">NOTES</span></span>

## <span data-ttu-id="0aa7d-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0aa7d-151">RELATED LINKS</span></span>
