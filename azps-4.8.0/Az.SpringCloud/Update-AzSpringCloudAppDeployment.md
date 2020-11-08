---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173492"
---
# <span data-ttu-id="c4502-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c4502-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c4502-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4502-102">SYNOPSIS</span></span>
<span data-ttu-id="c4502-103">Vorgang zum Aktualisieren einer beendenden Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c4502-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c4502-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4502-104">SYNTAX</span></span>

### <span data-ttu-id="c4502-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4502-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c4502-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4502-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4502-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4502-107">DESCRIPTION</span></span>
<span data-ttu-id="c4502-108">Vorgang zum Aktualisieren einer beendenden Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c4502-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c4502-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4502-109">EXAMPLES</span></span>

### <span data-ttu-id="c4502-110">Beispiel 1: Aktualisieren der Bereitstellung der Quell Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="c4502-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c4502-111">Aktualisieren Sie die Bereitstellung der Quell Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="c4502-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="c4502-112">Beispiel 2: Aktualisieren der Bereitstellung der Quell Wolke von Pipe</span><span class="sxs-lookup"><span data-stu-id="c4502-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c4502-113">Aktualisieren Sie die Bereitstellung der Quell Wolke von Pipe.</span><span class="sxs-lookup"><span data-stu-id="c4502-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="c4502-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4502-114">PARAMETERS</span></span>

### <span data-ttu-id="c4502-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="c4502-115">-AppName</span></span>
<span data-ttu-id="c4502-116">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4502-117">-AsJob</span></span>
<span data-ttu-id="c4502-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c4502-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c4502-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="c4502-119">-Cpu</span></span>
<span data-ttu-id="c4502-120">Erforderliche CPU</span><span class="sxs-lookup"><span data-stu-id="c4502-120">Required CPU</span></span>

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

### <span data-ttu-id="c4502-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4502-121">-DefaultProfile</span></span>
<span data-ttu-id="c4502-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4502-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4502-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c4502-123">-EnvironmentVariable</span></span>
<span data-ttu-id="c4502-124">Sammlung von Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="c4502-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="c4502-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4502-125">-InputObject</span></span>
<span data-ttu-id="c4502-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c4502-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="c4502-127">-InstanceCount</span></span>
<span data-ttu-id="c4502-128">Anzahl der Instanzen</span><span class="sxs-lookup"><span data-stu-id="c4502-128">Instance count</span></span>

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

### <span data-ttu-id="c4502-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c4502-129">-JvmOption</span></span>
<span data-ttu-id="c4502-130">JVM-Parameter</span><span class="sxs-lookup"><span data-stu-id="c4502-130">JVM parameter</span></span>

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

### <span data-ttu-id="c4502-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c4502-131">-MemoryInGb</span></span>
<span data-ttu-id="c4502-132">Erforderliche Arbeitsspeichergröße in GB</span><span class="sxs-lookup"><span data-stu-id="c4502-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="c4502-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c4502-133">-Name</span></span>
<span data-ttu-id="c4502-134">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-134">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c4502-135">-NoWait</span></span>
<span data-ttu-id="c4502-136">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c4502-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4502-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4502-137">-ResourceGroupName</span></span>
<span data-ttu-id="c4502-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c4502-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c4502-139">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c4502-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c4502-140">-RuntimeVersion</span></span>
<span data-ttu-id="c4502-141">Runtime-Version</span><span class="sxs-lookup"><span data-stu-id="c4502-141">Runtime version</span></span>

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

### <span data-ttu-id="c4502-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4502-142">-ServiceName</span></span>
<span data-ttu-id="c4502-143">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-143">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c4502-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="c4502-145">Auswahl für das Artefakt, das für die Bereitstellung für Projekte mit mehreren Modulen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4502-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c4502-146">Dies sollte Bethe relativen Pfad zum Ziel Modul/Projekt.</span><span class="sxs-lookup"><span data-stu-id="c4502-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="c4502-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c4502-147">-SourceRelativePath</span></span>
<span data-ttu-id="c4502-148">Relativer Pfad des Speichers, der die Quelle speichert</span><span class="sxs-lookup"><span data-stu-id="c4502-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="c4502-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c4502-149">-SourceType</span></span>
<span data-ttu-id="c4502-150">Typ der hochgeladenen Quelle</span><span class="sxs-lookup"><span data-stu-id="c4502-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="c4502-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c4502-151">-SourceVersion</span></span>
<span data-ttu-id="c4502-152">Version der Quelle</span><span class="sxs-lookup"><span data-stu-id="c4502-152">Version of the source</span></span>

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

### <span data-ttu-id="c4502-153">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c4502-153">-SubscriptionId</span></span>
<span data-ttu-id="c4502-154">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c4502-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4502-155">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c4502-155">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4502-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4502-156">-Confirm</span></span>
<span data-ttu-id="c4502-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4502-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4502-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4502-158">-WhatIf</span></span>
<span data-ttu-id="c4502-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4502-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4502-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4502-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4502-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4502-161">CommonParameters</span></span>
<span data-ttu-id="c4502-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4502-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4502-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4502-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4502-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4502-164">INPUTS</span></span>

### <span data-ttu-id="c4502-165">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="c4502-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c4502-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4502-166">OUTPUTS</span></span>

### <span data-ttu-id="c4502-167">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c4502-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="c4502-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4502-168">NOTES</span></span>

<span data-ttu-id="c4502-169">Aliase</span><span class="sxs-lookup"><span data-stu-id="c4502-169">ALIASES</span></span>

<span data-ttu-id="c4502-170">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4502-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4502-171">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4502-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4502-172">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c4502-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4502-173">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c4502-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4502-174">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c4502-175">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c4502-176">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c4502-177">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c4502-178">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c4502-179">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c4502-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4502-180">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="c4502-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c4502-181">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c4502-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c4502-182">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c4502-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c4502-183">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="c4502-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c4502-184">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c4502-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c4502-185">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c4502-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c4502-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4502-186">RELATED LINKS</span></span>

