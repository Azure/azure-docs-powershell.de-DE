---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175449"
---
# <span data-ttu-id="2fd2e-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="2fd2e-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="2fd2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd2e-103">Abrufen einer Bereitstellung und der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fd2e-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="2fd2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fd2e-104">SYNTAX</span></span>

### <span data-ttu-id="2fd2e-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fd2e-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2fd2e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2fd2e-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2fd2e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2fd2e-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd2e-108">Liste</span><span class="sxs-lookup"><span data-stu-id="2fd2e-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2fd2e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fd2e-109">DESCRIPTION</span></span>
<span data-ttu-id="2fd2e-110">Abrufen einer Bereitstellung und der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fd2e-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="2fd2e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fd2e-111">EXAMPLES</span></span>

### <span data-ttu-id="2fd2e-112">Beispiel 1: Abrufen der Deploymeng-App für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
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

<span data-ttu-id="2fd2e-113">Holen Sie sich die APP Deploymeng für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="2fd2e-114">Beispiel 2: Auflisten der gesamten Bereitstellung unter einer bestimmten app für die Frühlings Wolke</span><span class="sxs-lookup"><span data-stu-id="2fd2e-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="2fd2e-115">Auflisten der gesamten Bereitstellung unter einer bestimmten app für die Frühlings Wolke</span><span class="sxs-lookup"><span data-stu-id="2fd2e-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="2fd2e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd2e-116">PARAMETERS</span></span>

### <span data-ttu-id="2fd2e-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="2fd2e-117">-AppName</span></span>
<span data-ttu-id="2fd2e-118">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd2e-119">-DefaultProfile</span></span>
<span data-ttu-id="2fd2e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd2e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fd2e-121">-InputObject</span></span>
<span data-ttu-id="2fd2e-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2fd2e-123">-Name</span></span>
<span data-ttu-id="2fd2e-124">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd2e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2fd2e-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2fd2e-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2fd2e-128">-ServiceName</span></span>
<span data-ttu-id="2fd2e-129">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2fd2e-130">-SubscriptionId</span></span>
<span data-ttu-id="2fd2e-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2fd2e-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-133">-Version</span><span class="sxs-lookup"><span data-stu-id="2fd2e-133">-Version</span></span>
<span data-ttu-id="2fd2e-134">Version der aufzulistenden Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="2fd2e-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd2e-135">CommonParameters</span></span>
<span data-ttu-id="2fd2e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd2e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fd2e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd2e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fd2e-138">INPUTS</span></span>

### <span data-ttu-id="2fd2e-139">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2fd2e-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2fd2e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fd2e-140">OUTPUTS</span></span>

### <span data-ttu-id="2fd2e-141">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="2fd2e-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="2fd2e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fd2e-142">NOTES</span></span>

<span data-ttu-id="2fd2e-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="2fd2e-143">ALIASES</span></span>

<span data-ttu-id="2fd2e-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fd2e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fd2e-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fd2e-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fd2e-147">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd2e-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2fd2e-148">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2fd2e-149">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2fd2e-150">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2fd2e-151">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2fd2e-152">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2fd2e-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2fd2e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2fd2e-154">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="2fd2e-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2fd2e-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2fd2e-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2fd2e-157">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2fd2e-158">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2fd2e-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2fd2e-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2fd2e-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fd2e-160">RELATED LINKS</span></span>

