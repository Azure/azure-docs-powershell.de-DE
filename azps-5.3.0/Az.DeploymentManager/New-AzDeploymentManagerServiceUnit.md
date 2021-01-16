---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387385"
---
# <span data-ttu-id="861e0-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="861e0-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="861e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="861e0-102">SYNOPSIS</span></span>
<span data-ttu-id="861e0-103">Erstellt eine Diensteinheit unter der angegebenen Dienst- und Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="861e0-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="861e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="861e0-104">SYNTAX</span></span>

### <span data-ttu-id="861e0-105">ByTopologyAndServiceNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="861e0-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="861e0-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="861e0-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="861e0-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="861e0-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="861e0-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="861e0-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="861e0-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="861e0-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861e0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="861e0-110">DESCRIPTION</span></span>
<span data-ttu-id="861e0-111">Das **Cmdlet "New-AzDeploymentManagerServiceUnit"** erstellt einen Dienst unter einem Dienst in einer Diensttopologie und gibt ein Objekt zurück, das diese Diensteinheit darstellt.</span><span class="sxs-lookup"><span data-stu-id="861e0-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="861e0-112">Geben Sie den Namen, den Dienstnamen, die Diensttopologie, in der sie sich befindet, und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="861e0-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="861e0-113">Das Cmdlet gibt ein "ServiceUnit"-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="861e0-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="861e0-114">Sie können dieses Objekt lokal ändern und dann Änderungen an dem Dienst mithilfe des cmdlets Set-AzDeploymentManagerService anwenden.</span><span class="sxs-lookup"><span data-stu-id="861e0-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="861e0-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="861e0-115">EXAMPLES</span></span>

### <span data-ttu-id="861e0-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="861e0-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="861e0-117">Dieses Cmdlet erstellt eine neue Diensteinheit mit dem Namen "ContosoService2Storage" in der ContosoResourceGroup unter dem Dienst "ContosoService2" in der Topologie "ContosoServiceTopology" am Ort "Central US".</span><span class="sxs-lookup"><span data-stu-id="861e0-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="861e0-118">Die Vorlagen- und Parameterdateien sind als relative Pfade zu dem Artefaktquellenspeicherort definiert, auf den in der Diensttopologie "ContosoServiceTopology" verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="861e0-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="861e0-119">Die in dieser Vorlage definierten Ressourcen müssen in der Zielressourcengruppe "service2ResourceGroup" bereitgestellt werden, und der Bereitstellungsmodus ist auf "Inkrementell" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="861e0-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="861e0-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="861e0-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="861e0-121">Dieses Cmdlet erstellt eine neue Diensteinheit mit dem Namen "ContosoService2Storage" in der ContosoResourceGroup unter dem Dienst "ContosoService2" in der Topologie "ContosoServiceTopology" am Ort "Central US".</span><span class="sxs-lookup"><span data-stu-id="861e0-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="861e0-122">Die Vorlagen- und Parameterverweise werden als SAS-URI bereitgestellt, da "ResourceId" als Artefaktquelle in der Diensttopologie "ContosoServiceTopology1" nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="861e0-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="861e0-123">Die in dieser Vorlage definierten Ressourcen müssen in der Zielressourcengruppe "service2ResourceGroup" bereitgestellt werden, und der Bereitstellungsmodus ist auf "Abgeschlossen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="861e0-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="861e0-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="861e0-124">PARAMETERS</span></span>

### <span data-ttu-id="861e0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="861e0-125">-AsJob</span></span>
<span data-ttu-id="861e0-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="861e0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="861e0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861e0-127">-DefaultProfile</span></span>
<span data-ttu-id="861e0-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="861e0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="861e0-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="861e0-129">-DeploymentMode</span></span>
<span data-ttu-id="861e0-130">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="861e0-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-131">-Location</span><span class="sxs-lookup"><span data-stu-id="861e0-131">-Location</span></span>
<span data-ttu-id="861e0-132">Der Speicherort der Diensteinheitsressource.</span><span class="sxs-lookup"><span data-stu-id="861e0-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="861e0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="861e0-133">-Name</span></span>
<span data-ttu-id="861e0-134">Der Name der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="861e0-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="861e0-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="861e0-136">Der Pfad zur Parameterdatei relativ zur Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="861e0-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="861e0-137">Erfordert, dass in serviceTopology auf ArtifactSource verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="861e0-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="861e0-138">-ParametersUri</span></span>
<span data-ttu-id="861e0-139">Der SAS-URI der Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="861e0-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="861e0-140">Wenn in der ServiceTopology auf "ArtifactSourceId" verwiesen wurde, geben Sie einen relativen Pfad mit "ParametersArtifactSourceRelativePath" an.</span><span class="sxs-lookup"><span data-stu-id="861e0-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="861e0-141">-ResourceGroupName</span></span>
<span data-ttu-id="861e0-142">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="861e0-142">The resource group.</span></span>

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

### <span data-ttu-id="861e0-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="861e0-143">-ServiceName</span></span>
<span data-ttu-id="861e0-144">Der Name des Diensts, zu dem diese Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="861e0-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="861e0-145">-ServiceObject</span></span>
<span data-ttu-id="861e0-146">Das Dienstobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="861e0-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="861e0-147">-ServiceResourceId</span></span>
<span data-ttu-id="861e0-148">Der Bezeichner der Dienstressource, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="861e0-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="861e0-149">-ServiceTopologyName</span></span>
<span data-ttu-id="861e0-150">Der Name der Diensttopologie, zu der diese Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="861e0-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="861e0-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="861e0-152">Das Diensttopologieobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="861e0-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="861e0-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="861e0-154">Der Ressourcenbezeichner für die Diensttopologie, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="861e0-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="861e0-155">-Tag</span></span>
<span data-ttu-id="861e0-156">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="861e0-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="861e0-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="861e0-157">-TargetResourceGroup</span></span>
<span data-ttu-id="861e0-158">Bestimmt den Speicherort, an dem Ressourcen unter der Diensteinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="861e0-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="861e0-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="861e0-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="861e0-160">Der Pfad zur Vorlagendatei relativ zur Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="861e0-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="861e0-161">Erfordert, dass in serviceTopology auf ArtifactSource verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="861e0-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="861e0-162">-TemplateUri</span></span>
<span data-ttu-id="861e0-163">Der SAS-URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="861e0-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="861e0-164">Wenn in der ServiceTopology auf "ArtifactSourceId" verwiesen wurde, geben Sie einen relativen Pfad mit "TemplateArtifactSourceRelativePath" an.</span><span class="sxs-lookup"><span data-stu-id="861e0-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861e0-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="861e0-165">-Confirm</span></span>
<span data-ttu-id="861e0-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="861e0-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="861e0-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="861e0-167">-WhatIf</span></span>
<span data-ttu-id="861e0-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="861e0-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="861e0-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="861e0-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="861e0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861e0-170">CommonParameters</span></span>
<span data-ttu-id="861e0-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861e0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861e0-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="861e0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861e0-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="861e0-173">INPUTS</span></span>

### <span data-ttu-id="861e0-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="861e0-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="861e0-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="861e0-175">OUTPUTS</span></span>

### <span data-ttu-id="861e0-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="861e0-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="861e0-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="861e0-177">NOTES</span></span>

## <span data-ttu-id="861e0-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="861e0-178">RELATED LINKS</span></span>
