---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174148"
---
# <span data-ttu-id="a00cb-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="a00cb-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="a00cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a00cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a00cb-103">Abrufen einer Bereitstellung und der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a00cb-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="a00cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a00cb-104">SYNTAX</span></span>

### <span data-ttu-id="a00cb-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a00cb-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a00cb-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a00cb-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a00cb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a00cb-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a00cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a00cb-108">DESCRIPTION</span></span>
<span data-ttu-id="a00cb-109">Abrufen einer Bereitstellung und der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a00cb-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="a00cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a00cb-110">EXAMPLES</span></span>

### <span data-ttu-id="a00cb-111">Beispiel 1: Abrufen der Deploymeng-App für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="a00cb-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="a00cb-112">Holen Sie sich die APP Deploymeng für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="a00cb-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="a00cb-113">Beispiel 2: Auflisten der gesamten Bereitstellung unter einer bestimmten app für die Frühlings Wolke</span><span class="sxs-lookup"><span data-stu-id="a00cb-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="a00cb-114">Auflisten der gesamten Bereitstellung unter einer bestimmten app für die Frühlings Wolke</span><span class="sxs-lookup"><span data-stu-id="a00cb-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="a00cb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00cb-115">PARAMETERS</span></span>

### <span data-ttu-id="a00cb-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="a00cb-116">-AppName</span></span>
<span data-ttu-id="a00cb-117">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="a00cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00cb-118">-DefaultProfile</span></span>
<span data-ttu-id="a00cb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a00cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a00cb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a00cb-120">-InputObject</span></span>
<span data-ttu-id="a00cb-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a00cb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a00cb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a00cb-122">-Name</span></span>
<span data-ttu-id="a00cb-123">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="a00cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="a00cb-125">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a00cb-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a00cb-126">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a00cb-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a00cb-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a00cb-127">-ServiceName</span></span>
<span data-ttu-id="a00cb-128">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a00cb-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a00cb-129">-SubscriptionId</span></span>
<span data-ttu-id="a00cb-130">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a00cb-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a00cb-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a00cb-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00cb-132">-Version</span><span class="sxs-lookup"><span data-stu-id="a00cb-132">-Version</span></span>
<span data-ttu-id="a00cb-133">Version der aufzulistenden Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="a00cb-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00cb-134">CommonParameters</span></span>
<span data-ttu-id="a00cb-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00cb-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a00cb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00cb-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a00cb-137">INPUTS</span></span>

### <span data-ttu-id="a00cb-138">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a00cb-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a00cb-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a00cb-139">OUTPUTS</span></span>

### <span data-ttu-id="a00cb-140">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="a00cb-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="a00cb-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a00cb-141">NOTES</span></span>

<span data-ttu-id="a00cb-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="a00cb-142">ALIASES</span></span>

<span data-ttu-id="a00cb-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a00cb-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a00cb-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a00cb-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a00cb-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a00cb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a00cb-146">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a00cb-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a00cb-147">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a00cb-148">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a00cb-149">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a00cb-150">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a00cb-151">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a00cb-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a00cb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a00cb-153">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="a00cb-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a00cb-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a00cb-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a00cb-155">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a00cb-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a00cb-156">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="a00cb-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a00cb-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a00cb-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a00cb-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a00cb-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a00cb-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a00cb-159">RELATED LINKS</span></span>

