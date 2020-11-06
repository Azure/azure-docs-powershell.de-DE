---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474738"
---
# <span data-ttu-id="01c58-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="01c58-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="01c58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01c58-102">SYNOPSIS</span></span>
<span data-ttu-id="01c58-103">Erstellt eine neue Diensteinheit unter einem Dienst in einer Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="01c58-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="01c58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01c58-104">SYNTAX</span></span>

### <span data-ttu-id="01c58-105">ByTopologyAndServiceNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="01c58-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01c58-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="01c58-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c58-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="01c58-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c58-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="01c58-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c58-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="01c58-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c58-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01c58-110">DESCRIPTION</span></span>
<span data-ttu-id="01c58-111">Das Cmdlet **New-AzureRmDeploymentManagerServiceUnit** erstellt einen Dienst unter einem Dienst in einer Dienst Topologie und gibt ein Objekt zurück, das diese Diensteinheit darstellt.</span><span class="sxs-lookup"><span data-stu-id="01c58-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="01c58-112">Geben Sie die Diensteinheit unter dem Namen, dem Dienstnamen, der Dienst Topologie, in der Sie sich befindet, und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="01c58-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="01c58-113">Das Cmdlet gibt ein Serviceunit-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="01c58-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="01c58-114">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerService-Cmdlets Änderungen am Dienst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="01c58-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="01c58-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01c58-115">EXAMPLES</span></span>

### <span data-ttu-id="01c58-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01c58-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="01c58-117">Mit diesem Cmdlet wird eine neue Diensteinheit mit dem Namen ContosoService2Storage in der ContosoResourceGroup unter dem Dienst ContosoService2 in Topologie ContosoServiceTopology an der zentralen Position von US erstellt.</span><span class="sxs-lookup"><span data-stu-id="01c58-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="01c58-118">Die Vorlagen-und Parameterdateien werden als relative Pfade in den Artefakt-Quellspeicherort definiert, auf die in der Dienst Topologie ContosoServiceTopology verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="01c58-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="01c58-119">Die in dieser Vorlage definierten Ressourcen werden in der Ziel Ressourcengruppe service2ResourceGroup bereitgestellt, wobei der Bereitstellungsmodus auf Incremental festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01c58-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="01c58-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01c58-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="01c58-121">Mit diesem Cmdlet wird eine neue Diensteinheit mit dem Namen ContosoService2Storage in der ContosoResourceGroup unter dem Dienst ContosoService2 in Topologie ContosoServiceTopology an der zentralen Position von US erstellt.</span><span class="sxs-lookup"><span data-stu-id="01c58-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="01c58-122">Die Vorlagen-und Parameters-Verweise werden in Form von SAS-URI als Artefakt-Quell-ContosoServiceTopology1 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="01c58-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="01c58-123">Die in dieser Vorlage definierten Ressourcen werden in der Ziel Ressourcengruppe service2ResourceGroup bereitgestellt, wobei der Bereitstellungsmodus auf "abgeschlossen" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01c58-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="01c58-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="01c58-124">PARAMETERS</span></span>

### <span data-ttu-id="01c58-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01c58-125">-AsJob</span></span>
<span data-ttu-id="01c58-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01c58-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01c58-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c58-127">-DefaultProfile</span></span>
<span data-ttu-id="01c58-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01c58-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c58-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="01c58-129">-DeploymentMode</span></span>
<span data-ttu-id="01c58-130">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="01c58-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="01c58-131">-Location</span></span>
<span data-ttu-id="01c58-132">Der Speicherort der Dienst Einheits Ressource.</span><span class="sxs-lookup"><span data-stu-id="01c58-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="01c58-133">-Name</span><span class="sxs-lookup"><span data-stu-id="01c58-133">-Name</span></span>
<span data-ttu-id="01c58-134">Der Name der Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="01c58-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="01c58-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="01c58-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="01c58-136">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="01c58-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="01c58-137">-ParametersUri</span></span>
<span data-ttu-id="01c58-138">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="01c58-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c58-139">-ResourceGroupName</span></span>
<span data-ttu-id="01c58-140">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01c58-140">The resource group.</span></span>

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

### <span data-ttu-id="01c58-141">-Service</span><span class="sxs-lookup"><span data-stu-id="01c58-141">-Service</span></span>
<span data-ttu-id="01c58-142">Das Dienstobjekt, in dem die Serviceeinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="01c58-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="01c58-143">-ServiceName</span></span>
<span data-ttu-id="01c58-144">Der Name des Diensts, zu dem diese Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="01c58-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="01c58-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="01c58-145">-ServiceResourceId</span></span>
<span data-ttu-id="01c58-146">Der Dienst Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="01c58-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="01c58-147">-ServiceTopology</span></span>
<span data-ttu-id="01c58-148">Das Service Topology-Objekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="01c58-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="01c58-149">-ServiceTopologyName</span></span>
<span data-ttu-id="01c58-150">Der Name der Serivce-Topologie, zu der diese Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="01c58-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="01c58-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="01c58-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="01c58-152">Der Dienst Topologie-Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="01c58-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="01c58-153">-Tag</span></span>
<span data-ttu-id="01c58-154">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="01c58-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="01c58-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01c58-155">-TargetResourceGroup</span></span>
<span data-ttu-id="01c58-156">Bestimmt den Standort, in dem Ressourcen unter der Serviceeinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01c58-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="01c58-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="01c58-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="01c58-158">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="01c58-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="01c58-159">-TemplateUri</span></span>
<span data-ttu-id="01c58-160">Der Bereitstellungsmodus, der beim Bereitstellen der Ressourcen in der Diensteinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01c58-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="01c58-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01c58-161">-Confirm</span></span>
<span data-ttu-id="01c58-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01c58-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c58-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c58-163">-WhatIf</span></span>
<span data-ttu-id="01c58-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01c58-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01c58-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01c58-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c58-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c58-166">CommonParameters</span></span>
<span data-ttu-id="01c58-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c58-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c58-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c58-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c58-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01c58-169">INPUTS</span></span>

### <span data-ttu-id="01c58-170">Keine</span><span class="sxs-lookup"><span data-stu-id="01c58-170">None</span></span>

## <span data-ttu-id="01c58-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01c58-171">OUTPUTS</span></span>

### <span data-ttu-id="01c58-172">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="01c58-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="01c58-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="01c58-173">NOTES</span></span>

## <span data-ttu-id="01c58-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01c58-174">RELATED LINKS</span></span>

[<span data-ttu-id="01c58-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="01c58-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="01c58-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="01c58-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="01c58-177">Satz-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="01c58-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)