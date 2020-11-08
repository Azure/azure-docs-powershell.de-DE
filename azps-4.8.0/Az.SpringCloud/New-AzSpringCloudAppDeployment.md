---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174136"
---
# <span data-ttu-id="6d408-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="6d408-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="6d408-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d408-102">SYNOPSIS</span></span>
<span data-ttu-id="6d408-103">Erstellen Sie eine neue Bereitstellung, oder aktualisieren Sie eine beendende Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6d408-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="6d408-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d408-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6d408-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d408-105">DESCRIPTION</span></span>
<span data-ttu-id="6d408-106">Erstellen Sie eine neue Bereitstellung, oder aktualisieren Sie eine beendende Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6d408-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="6d408-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d408-107">EXAMPLES</span></span>

### <span data-ttu-id="6d408-108">Beispiel 1: Beispiel 1: Erstellen einer Feder Cloud-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6d408-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="6d408-109">Erstellen Sie eine Bereitstellung in der Feder Wolke.</span><span class="sxs-lookup"><span data-stu-id="6d408-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="6d408-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d408-110">PARAMETERS</span></span>

### <span data-ttu-id="6d408-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="6d408-111">-AppName</span></span>
<span data-ttu-id="6d408-112">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6d408-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="6d408-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d408-113">-AsJob</span></span>
<span data-ttu-id="6d408-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d408-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6d408-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="6d408-115">-Cpu</span></span>
<span data-ttu-id="6d408-116">Erforderliche CPU</span><span class="sxs-lookup"><span data-stu-id="6d408-116">Required CPU</span></span>

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

### <span data-ttu-id="6d408-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d408-117">-DefaultProfile</span></span>
<span data-ttu-id="6d408-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d408-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d408-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="6d408-119">-EnvironmentVariable</span></span>
<span data-ttu-id="6d408-120">Sammlung von Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="6d408-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="6d408-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6d408-121">-InstanceCount</span></span>
<span data-ttu-id="6d408-122">Anzahl der Instanzen</span><span class="sxs-lookup"><span data-stu-id="6d408-122">Instance count</span></span>

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

### <span data-ttu-id="6d408-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="6d408-123">-JvmOption</span></span>
<span data-ttu-id="6d408-124">JVM-Parameter</span><span class="sxs-lookup"><span data-stu-id="6d408-124">JVM parameter</span></span>

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

### <span data-ttu-id="6d408-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="6d408-125">-MemoryInGb</span></span>
<span data-ttu-id="6d408-126">Erforderliche Arbeitsspeichergröße in GB</span><span class="sxs-lookup"><span data-stu-id="6d408-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="6d408-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6d408-127">-Name</span></span>
<span data-ttu-id="6d408-128">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="6d408-128">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="6d408-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6d408-129">-NoWait</span></span>
<span data-ttu-id="6d408-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6d408-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d408-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d408-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d408-132">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="6d408-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d408-133">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="6d408-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d408-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="6d408-134">-RuntimeVersion</span></span>
<span data-ttu-id="6d408-135">Runtime-Version</span><span class="sxs-lookup"><span data-stu-id="6d408-135">Runtime version</span></span>

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

### <span data-ttu-id="6d408-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6d408-136">-ServiceName</span></span>
<span data-ttu-id="6d408-137">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="6d408-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6d408-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="6d408-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="6d408-139">Auswahl für das Artefakt, das für die Bereitstellung für Projekte mit mehreren Modulen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d408-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="6d408-140">Dies sollte Bethe relativen Pfad zum Ziel Modul/Projekt.</span><span class="sxs-lookup"><span data-stu-id="6d408-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="6d408-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="6d408-141">-SourceRelativePath</span></span>
<span data-ttu-id="6d408-142">Relativer Pfad des Speichers, der die Quelle speichert</span><span class="sxs-lookup"><span data-stu-id="6d408-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="6d408-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="6d408-143">-SourceType</span></span>
<span data-ttu-id="6d408-144">Typ der hochgeladenen Quelle</span><span class="sxs-lookup"><span data-stu-id="6d408-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="6d408-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="6d408-145">-SourceVersion</span></span>
<span data-ttu-id="6d408-146">Version der Quelle</span><span class="sxs-lookup"><span data-stu-id="6d408-146">Version of the source</span></span>

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

### <span data-ttu-id="6d408-147">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6d408-147">-SubscriptionId</span></span>
<span data-ttu-id="6d408-148">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6d408-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d408-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="6d408-149">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d408-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d408-150">-Confirm</span></span>
<span data-ttu-id="6d408-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d408-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d408-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d408-152">-WhatIf</span></span>
<span data-ttu-id="6d408-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d408-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d408-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d408-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d408-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d408-155">CommonParameters</span></span>
<span data-ttu-id="6d408-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d408-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d408-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d408-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d408-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d408-158">INPUTS</span></span>

## <span data-ttu-id="6d408-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d408-159">OUTPUTS</span></span>

### <span data-ttu-id="6d408-160">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="6d408-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="6d408-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d408-161">NOTES</span></span>

<span data-ttu-id="6d408-162">Aliase</span><span class="sxs-lookup"><span data-stu-id="6d408-162">ALIASES</span></span>

## <span data-ttu-id="6d408-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d408-163">RELATED LINKS</span></span>

