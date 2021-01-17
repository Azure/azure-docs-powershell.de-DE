---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470348"
---
# <span data-ttu-id="d4cf5-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d4cf5-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="d4cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cf5-103">Holen Sie sich eine App und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-103">Get an App and its properties.</span></span>

## <span data-ttu-id="d4cf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4cf5-104">SYNTAX</span></span>

### <span data-ttu-id="d4cf5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4cf5-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4cf5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d4cf5-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4cf5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4cf5-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4cf5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="d4cf5-109">Holen Sie sich eine App und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-109">Get an App and its properties.</span></span>

## <span data-ttu-id="d4cf5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="d4cf5-111">Beispiel 1: Quell-Cloud-App nach Name erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="d4cf5-112">Holen Sie sich die Spring Cloud App nach Name.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="d4cf5-113">Beispiel 2: Auflisten der app unter einem bestimmten Dienst für die Quellwolke.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="d4cf5-114">Listen Sie alle Apps unter einem bestimmten Quell-Cloud-Dienst auf.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="d4cf5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4cf5-115">PARAMETERS</span></span>

### <span data-ttu-id="d4cf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cf5-116">-DefaultProfile</span></span>
<span data-ttu-id="d4cf5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4cf5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4cf5-118">-InputObject</span></span>
<span data-ttu-id="d4cf5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4cf5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d4cf5-120">-Name</span></span>
<span data-ttu-id="d4cf5-121">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cf5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cf5-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4cf5-123">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d4cf5-124">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d4cf5-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d4cf5-125">-ServiceName</span></span>
<span data-ttu-id="d4cf5-126">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d4cf5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4cf5-127">-SubscriptionId</span></span>
<span data-ttu-id="d4cf5-128">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4cf5-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4cf5-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="d4cf5-130">-SyncStatus</span></span>
<span data-ttu-id="d4cf5-131">Gibt an, ob der Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="d4cf5-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cf5-132">CommonParameters</span></span>
<span data-ttu-id="d4cf5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cf5-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4cf5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cf5-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-135">INPUTS</span></span>

### <span data-ttu-id="d4cf5-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d4cf5-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d4cf5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-137">OUTPUTS</span></span>

### <span data-ttu-id="d4cf5-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="d4cf5-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="d4cf5-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d4cf5-139">NOTES</span></span>

<span data-ttu-id="d4cf5-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d4cf5-140">ALIASES</span></span>

<span data-ttu-id="d4cf5-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4cf5-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4cf5-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4cf5-144">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d4cf5-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4cf5-145">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d4cf5-146">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d4cf5-147">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d4cf5-148">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d4cf5-149">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d4cf5-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d4cf5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4cf5-151">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="d4cf5-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d4cf5-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d4cf5-153">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d4cf5-154">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d4cf5-155">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d4cf5-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d4cf5-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-157">RELATED LINKS</span></span>

