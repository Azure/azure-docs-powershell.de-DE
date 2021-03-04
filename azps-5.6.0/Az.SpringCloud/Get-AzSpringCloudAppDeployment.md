---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: b4b68f654c78da0dc2341966e3f9efaac397e504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920267"
---
# <span data-ttu-id="76b18-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="76b18-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="76b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b18-102">SYNOPSIS</span></span>
<span data-ttu-id="76b18-103">Holen Sie sich eine Bereitstellung und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76b18-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="76b18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76b18-104">SYNTAX</span></span>

### <span data-ttu-id="76b18-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="76b18-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76b18-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="76b18-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76b18-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76b18-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76b18-108">Liste</span><span class="sxs-lookup"><span data-stu-id="76b18-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76b18-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76b18-109">DESCRIPTION</span></span>
<span data-ttu-id="76b18-110">Holen Sie sich eine Bereitstellung und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76b18-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="76b18-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76b18-111">EXAMPLES</span></span>

### <span data-ttu-id="76b18-112">Beispiel 1: Holen Sie sich "Spring Cloud App Deploymeng" nach Name.</span><span class="sxs-lookup"><span data-stu-id="76b18-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="76b18-113">Holen Sie sich "Spring Cloud App Deploymeng" nach Name.</span><span class="sxs-lookup"><span data-stu-id="76b18-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="76b18-114">Beispiel 2: Listen Sie die ganze Bereitstellung unter einer bestimmten Quell-Cloud-App auf.</span><span class="sxs-lookup"><span data-stu-id="76b18-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="76b18-115">Listen Sie alle Bereitstellungen unter einer bestimmten Quell-Cloud-App auf.</span><span class="sxs-lookup"><span data-stu-id="76b18-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="76b18-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="76b18-116">PARAMETERS</span></span>

### <span data-ttu-id="76b18-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="76b18-117">-AppName</span></span>
<span data-ttu-id="76b18-118">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="76b18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b18-119">-DefaultProfile</span></span>
<span data-ttu-id="76b18-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b18-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76b18-121">-InputObject</span></span>
<span data-ttu-id="76b18-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="76b18-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76b18-123">-Name</span><span class="sxs-lookup"><span data-stu-id="76b18-123">-Name</span></span>
<span data-ttu-id="76b18-124">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="76b18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b18-125">-ResourceGroupName</span></span>
<span data-ttu-id="76b18-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="76b18-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="76b18-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="76b18-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="76b18-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="76b18-128">-ServiceName</span></span>
<span data-ttu-id="76b18-129">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="76b18-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76b18-130">-SubscriptionId</span></span>
<span data-ttu-id="76b18-131">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="76b18-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="76b18-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="76b18-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76b18-133">-Version</span><span class="sxs-lookup"><span data-stu-id="76b18-133">-Version</span></span>
<span data-ttu-id="76b18-134">Version der zu aufgelisteten Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="76b18-134">Version of the deployments to be listed</span></span>

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

### <span data-ttu-id="76b18-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b18-135">CommonParameters</span></span>
<span data-ttu-id="76b18-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b18-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b18-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76b18-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b18-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76b18-138">INPUTS</span></span>

### <span data-ttu-id="76b18-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="76b18-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="76b18-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76b18-140">OUTPUTS</span></span>

### <span data-ttu-id="76b18-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="76b18-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="76b18-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="76b18-142">NOTES</span></span>

<span data-ttu-id="76b18-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="76b18-143">ALIASES</span></span>

<span data-ttu-id="76b18-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="76b18-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76b18-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="76b18-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76b18-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76b18-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76b18-147">INPUTOBJECT <ISpringCloudIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="76b18-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76b18-148">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="76b18-149">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="76b18-150">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="76b18-151">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="76b18-152">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="76b18-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="76b18-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76b18-154">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="76b18-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="76b18-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="76b18-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="76b18-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="76b18-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="76b18-157">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="76b18-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="76b18-158">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="76b18-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="76b18-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="76b18-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76b18-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="76b18-160">RELATED LINKS</span></span>

