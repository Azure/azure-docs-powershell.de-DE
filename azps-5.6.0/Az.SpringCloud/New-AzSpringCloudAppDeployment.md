---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947712"
---
# <span data-ttu-id="c3e3b-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c3e3b-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c3e3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e3b-103">Erstellen Sie eine neue Bereitstellung, oder aktualisieren Sie eine beendende Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c3e3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3e3b-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c3e3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e3b-106">Erstellen Sie eine neue Bereitstellung, oder aktualisieren Sie eine beendende Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c3e3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3e3b-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e3b-108">Beispiel 1: Beispiel 1: Erstellen einer Quellwolkenbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c3e3b-109">Erstellen Sie eine Quellwolkenbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="c3e3b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3e3b-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e3b-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="c3e3b-111">-AppName</span></span>
<span data-ttu-id="c3e3b-112">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="c3e3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3e3b-113">-AsJob</span></span>
<span data-ttu-id="c3e3b-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c3e3b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c3e3b-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="c3e3b-115">-Cpu</span></span>
<span data-ttu-id="c3e3b-116">Erforderliche CPU</span><span class="sxs-lookup"><span data-stu-id="c3e3b-116">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e3b-117">-DefaultProfile</span></span>
<span data-ttu-id="c3e3b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c3e3b-119">-EnvironmentVariable</span></span>
<span data-ttu-id="c3e3b-120">Sammlung von Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="c3e3b-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="c3e3b-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c3e3b-121">-JvmOption</span></span>
<span data-ttu-id="c3e3b-122">JVM-Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e3b-122">JVM parameter</span></span>

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

### <span data-ttu-id="c3e3b-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c3e3b-123">-MemoryInGb</span></span>
<span data-ttu-id="c3e3b-124">Erforderliche Arbeitsspeichergröße in GB</span><span class="sxs-lookup"><span data-stu-id="c3e3b-124">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e3b-125">-Name</span></span>
<span data-ttu-id="c3e3b-126">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3e3b-127">-NoWait</span></span>
<span data-ttu-id="c3e3b-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c3e3b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3e3b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e3b-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3e3b-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c3e3b-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c3e3b-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c3e3b-132">-RuntimeVersion</span></span>
<span data-ttu-id="c3e3b-133">Laufzeitversion</span><span class="sxs-lookup"><span data-stu-id="c3e3b-133">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c3e3b-134">-ServiceName</span></span>
<span data-ttu-id="c3e3b-135">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c3e3b-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c3e3b-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="c3e3b-137">Auswahl für das Artefakt, das für die Bereitstellung für Projekte mit mehreren Modulen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c3e3b-138">Dies sollte der relative Pfad zum Zielmodul/-projekt sein.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="c3e3b-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c3e3b-139">-SourceRelativePath</span></span>
<span data-ttu-id="c3e3b-140">Relativer Pfad des Speichers, in dem die Quelle gespeichert wird</span><span class="sxs-lookup"><span data-stu-id="c3e3b-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="c3e3b-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c3e3b-141">-SourceType</span></span>
<span data-ttu-id="c3e3b-142">Typ der hochgeladenen Quelle</span><span class="sxs-lookup"><span data-stu-id="c3e3b-142">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c3e3b-143">-SourceVersion</span></span>
<span data-ttu-id="c3e3b-144">Version der Quelle</span><span class="sxs-lookup"><span data-stu-id="c3e3b-144">Version of the source</span></span>

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

### <span data-ttu-id="c3e3b-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3e3b-145">-SubscriptionId</span></span>
<span data-ttu-id="c3e3b-146">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3e3b-147">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3b-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3e3b-148">-Confirm</span></span>
<span data-ttu-id="c3e3b-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e3b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e3b-150">-WhatIf</span></span>
<span data-ttu-id="c3e3b-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e3b-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e3b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e3b-153">CommonParameters</span></span>
<span data-ttu-id="c3e3b-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e3b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e3b-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e3b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e3b-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3e3b-156">INPUTS</span></span>

## <span data-ttu-id="c3e3b-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3e3b-157">OUTPUTS</span></span>

### <span data-ttu-id="c3e3b-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c3e3b-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="c3e3b-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3e3b-159">NOTES</span></span>

<span data-ttu-id="c3e3b-160">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c3e3b-160">ALIASES</span></span>

## <span data-ttu-id="c3e3b-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3e3b-161">RELATED LINKS</span></span>

