---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290236"
---
# <span data-ttu-id="64889-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="64889-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="64889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64889-102">SYNOPSIS</span></span>
<span data-ttu-id="64889-103">Erstellt einen Dienst unter der angegebenen Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="64889-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="64889-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64889-104">SYNTAX</span></span>

### <span data-ttu-id="64889-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="64889-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64889-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="64889-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64889-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="64889-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64889-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64889-108">DESCRIPTION</span></span>
<span data-ttu-id="64889-109">Das **Cmdlet "New-AzDeploymentManagerService"** erstellt einen Dienst unter einer Diensttopologie und gibt ein Objekt zurück, das den Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="64889-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="64889-110">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="64889-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="64889-111">Das Cmdlet gibt ein Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="64889-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="64889-112">Sie können dieses Objekt lokal ändern und dann Änderungen an dem Dienst mithilfe des cmdlets Set-AzDeploymentManagerService anwenden.</span><span class="sxs-lookup"><span data-stu-id="64889-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="64889-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64889-113">EXAMPLES</span></span>

### <span data-ttu-id="64889-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64889-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="64889-115">Erstellt einen neuen Dienst mit dem Namen "ContosoService1" unter der Diensttopologie "ContosoServiceTopology" in der Ressourcengruppe "ContosoResourceGroup" am Speicherort "USA, Mitte".</span><span class="sxs-lookup"><span data-stu-id="64889-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="64889-116">Die "TargetLocation"-Eigenschaft gibt an, dass der Dienst "ContosoService1" in der Region "USA, Osten" im angegebenen Abonnement bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64889-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="64889-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64889-117">PARAMETERS</span></span>

### <span data-ttu-id="64889-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64889-118">-DefaultProfile</span></span>
<span data-ttu-id="64889-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64889-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64889-120">-Location</span><span class="sxs-lookup"><span data-stu-id="64889-120">-Location</span></span>
<span data-ttu-id="64889-121">Der Speicherort der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="64889-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="64889-122">-Name</span><span class="sxs-lookup"><span data-stu-id="64889-122">-Name</span></span>
<span data-ttu-id="64889-123">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="64889-123">The name of the service.</span></span>

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

### <span data-ttu-id="64889-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64889-124">-ResourceGroupName</span></span>
<span data-ttu-id="64889-125">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64889-125">The resource group.</span></span>

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

### <span data-ttu-id="64889-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="64889-126">-ServiceTopologyId</span></span>
<span data-ttu-id="64889-127">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64889-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="64889-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="64889-128">-ServiceTopologyName</span></span>
<span data-ttu-id="64889-129">Der Name der Diensttopologie, zu der dieser Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="64889-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="64889-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="64889-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="64889-131">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64889-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="64889-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="64889-132">-Tag</span></span>
<span data-ttu-id="64889-133">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="64889-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="64889-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="64889-134">-TargetLocation</span></span>
<span data-ttu-id="64889-135">Bestimmt den Speicherort, an dem Ressourcen unter dem Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64889-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="64889-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64889-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="64889-137">Bestimmt das Abonnement, für das Ressourcen unter dem Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64889-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="64889-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64889-138">-Confirm</span></span>
<span data-ttu-id="64889-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64889-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64889-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64889-140">-WhatIf</span></span>
<span data-ttu-id="64889-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64889-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64889-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64889-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64889-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64889-143">CommonParameters</span></span>
<span data-ttu-id="64889-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64889-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64889-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64889-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64889-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64889-146">INPUTS</span></span>

### <span data-ttu-id="64889-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="64889-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64889-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64889-148">OUTPUTS</span></span>

### <span data-ttu-id="64889-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="64889-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="64889-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64889-150">NOTES</span></span>

## <span data-ttu-id="64889-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64889-151">RELATED LINKS</span></span>
