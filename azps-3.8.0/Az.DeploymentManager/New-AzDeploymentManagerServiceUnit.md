---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004587"
---
# <span data-ttu-id="ecf3f-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ecf3f-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="ecf3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf3f-103">Erstellt eine Diensteinheit unter der angegebenen Dienst-und Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="ecf3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecf3f-104">SYNTAX</span></span>

### <span data-ttu-id="ecf3f-105">ByTopologyAndServiceNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecf3f-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf3f-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ecf3f-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf3f-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ecf3f-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf3f-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="ecf3f-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf3f-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf3f-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf3f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecf3f-110">DESCRIPTION</span></span>
<span data-ttu-id="ecf3f-111">Das Cmdlet **New-AzDeploymentManagerServiceUnit** erstellt einen Dienst unter einem Dienst in einer Dienst Topologie und gibt ein Objekt zurück, das diese Diensteinheit darstellt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="ecf3f-112">Geben Sie die Diensteinheit unter dem Namen, dem Dienstnamen, der Dienst Topologie, in der Sie sich befindet, und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="ecf3f-113">Das Cmdlet gibt ein Serviceunit-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="ecf3f-114">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerService-Cmdlets Änderungen am Dienst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="ecf3f-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecf3f-115">EXAMPLES</span></span>

### <span data-ttu-id="ecf3f-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecf3f-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="ecf3f-117">Mit diesem Cmdlet wird eine neue Diensteinheit mit dem Namen ContosoService2Storage in der ContosoResourceGroup unter dem Dienst ContosoService2 in Topologie ContosoServiceTopology an der zentralen Position von US erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ecf3f-118">Die Vorlagen-und Parameterdateien werden als relative Pfade in den Artefakt-Quellspeicherort definiert, auf die in der Dienst Topologie ContosoServiceTopology verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="ecf3f-119">Die in dieser Vorlage definierten Ressourcen werden in der Ziel Ressourcengruppe service2ResourceGroup bereitgestellt, wobei der Bereitstellungsmodus auf Incremental festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="ecf3f-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ecf3f-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="ecf3f-121">Mit diesem Cmdlet wird eine neue Diensteinheit mit dem Namen ContosoService2Storage in der ContosoResourceGroup unter dem Dienst ContosoService2 in Topologie ContosoServiceTopology an der zentralen Position von US erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ecf3f-122">Die Vorlagen-und Parameters-Verweise werden in Form von SAS-URI als Artefakt-Quell-ContosoServiceTopology1 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="ecf3f-123">Die in dieser Vorlage definierten Ressourcen werden in der Ziel Ressourcengruppe service2ResourceGroup bereitgestellt, wobei der Bereitstellungsmodus auf "abgeschlossen" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="ecf3f-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecf3f-124">PARAMETERS</span></span>

### <span data-ttu-id="ecf3f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecf3f-125">-AsJob</span></span>
<span data-ttu-id="ecf3f-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ecf3f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecf3f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf3f-127">-DefaultProfile</span></span>
<span data-ttu-id="ecf3f-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf3f-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="ecf3f-129">-DeploymentMode</span></span>
<span data-ttu-id="ecf3f-130">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ecf3f-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="ecf3f-131">-Location</span></span>
<span data-ttu-id="ecf3f-132">Der Speicherort der Dienst Einheits Ressource.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="ecf3f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ecf3f-133">-Name</span></span>
<span data-ttu-id="ecf3f-134">Der Name der Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="ecf3f-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ecf3f-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="ecf3f-136">Der Pfad zur Parameterdatei relativ zur Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="ecf3f-137">Erfordert, dass in ServiceTopology auf ArtifactSource verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="ecf3f-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="ecf3f-138">-ParametersUri</span></span>
<span data-ttu-id="ecf3f-139">Der SAS-URI für die Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="ecf3f-140">Wenn im ServiceTopology auf ArtifactSourceId verwiesen wurde, geben Sie relativen Pfad mithilfe von ParametersArtifactSourceRelativePath an.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="ecf3f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf3f-141">-ResourceGroupName</span></span>
<span data-ttu-id="ecf3f-142">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-142">The resource group.</span></span>

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

### <span data-ttu-id="ecf3f-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ecf3f-143">-ServiceName</span></span>
<span data-ttu-id="ecf3f-144">Der Name des Diensts, zu dem diese Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="ecf3f-145">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="ecf3f-145">-ServiceObject</span></span>
<span data-ttu-id="ecf3f-146">Das Dienstobjekt, in dem die Serviceeinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ecf3f-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf3f-147">-ServiceResourceId</span></span>
<span data-ttu-id="ecf3f-148">Der Dienst Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ecf3f-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ecf3f-149">-ServiceTopologyName</span></span>
<span data-ttu-id="ecf3f-150">Der Name der Dienst Topologie, zu der diese Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="ecf3f-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ecf3f-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="ecf3f-152">Das Service Topology-Objekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ecf3f-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf3f-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ecf3f-154">Der Dienst Topologie-Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ecf3f-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecf3f-155">-Tag</span></span>
<span data-ttu-id="ecf3f-156">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ecf3f-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecf3f-157">-TargetResourceGroup</span></span>
<span data-ttu-id="ecf3f-158">Bestimmt den Standort, in dem Ressourcen unter der Serviceeinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="ecf3f-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ecf3f-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="ecf3f-160">Der Pfad zur Vorlagendatei relativ zur Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="ecf3f-161">Erfordert, dass in ServiceTopology auf ArtifactSource verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="ecf3f-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ecf3f-162">-TemplateUri</span></span>
<span data-ttu-id="ecf3f-163">Der SAS-URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="ecf3f-164">Wenn im ServiceTopology auf ArtifactSourceId verwiesen wurde, geben Sie relativen Pfad mithilfe von TemplateArtifactSourceRelativePath an.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="ecf3f-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecf3f-165">-Confirm</span></span>
<span data-ttu-id="ecf3f-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf3f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf3f-167">-WhatIf</span></span>
<span data-ttu-id="ecf3f-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf3f-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf3f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf3f-170">CommonParameters</span></span>
<span data-ttu-id="ecf3f-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf3f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf3f-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecf3f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf3f-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecf3f-173">INPUTS</span></span>

### <span data-ttu-id="ecf3f-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecf3f-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ecf3f-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecf3f-175">OUTPUTS</span></span>

### <span data-ttu-id="ecf3f-176">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="ecf3f-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ecf3f-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecf3f-177">NOTES</span></span>

## <span data-ttu-id="ecf3f-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecf3f-178">RELATED LINKS</span></span>
