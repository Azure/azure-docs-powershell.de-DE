---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175448"
---
# <span data-ttu-id="7c570-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="7c570-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="7c570-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c570-102">SYNOPSIS</span></span>
<span data-ttu-id="7c570-103">Rufen Sie eine APP und ihre Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="7c570-103">Get an App and its properties.</span></span>

## <span data-ttu-id="7c570-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c570-104">SYNTAX</span></span>

### <span data-ttu-id="7c570-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c570-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c570-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7c570-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c570-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c570-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c570-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c570-108">DESCRIPTION</span></span>
<span data-ttu-id="7c570-109">Rufen Sie eine APP und ihre Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="7c570-109">Get an App and its properties.</span></span>

## <span data-ttu-id="7c570-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c570-110">EXAMPLES</span></span>

### <span data-ttu-id="7c570-111">Beispiel 1: Abrufen der APP für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="7c570-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="7c570-112">Holen Sie sich die APP für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="7c570-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="7c570-113">Beispiel 2: Auflisten aller apps unter einem bestimmten Spring Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7c570-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="7c570-114">Listen Sie alle apps unter einem bestimmten Spring Cloud-Dienst auf.</span><span class="sxs-lookup"><span data-stu-id="7c570-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="7c570-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c570-115">PARAMETERS</span></span>

### <span data-ttu-id="7c570-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c570-116">-DefaultProfile</span></span>
<span data-ttu-id="7c570-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c570-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c570-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c570-118">-InputObject</span></span>
<span data-ttu-id="7c570-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7c570-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7c570-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c570-120">-Name</span></span>
<span data-ttu-id="7c570-121">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="7c570-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c570-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c570-123">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7c570-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7c570-124">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7c570-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7c570-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c570-125">-ServiceName</span></span>
<span data-ttu-id="7c570-126">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7c570-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7c570-127">-SubscriptionId</span></span>
<span data-ttu-id="7c570-128">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7c570-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c570-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7c570-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7c570-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="7c570-130">-SyncStatus</span></span>
<span data-ttu-id="7c570-131">Gibt an, ob der Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="7c570-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="7c570-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c570-132">CommonParameters</span></span>
<span data-ttu-id="7c570-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c570-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c570-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c570-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c570-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c570-135">INPUTS</span></span>

### <span data-ttu-id="7c570-136">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7c570-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7c570-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c570-137">OUTPUTS</span></span>

### <span data-ttu-id="7c570-138">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="7c570-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="7c570-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c570-139">NOTES</span></span>

<span data-ttu-id="7c570-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="7c570-140">ALIASES</span></span>

<span data-ttu-id="7c570-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c570-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c570-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c570-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c570-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7c570-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c570-144">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7c570-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c570-145">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7c570-146">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7c570-147">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7c570-148">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7c570-149">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7c570-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7c570-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c570-151">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="7c570-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7c570-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7c570-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7c570-153">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7c570-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7c570-154">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7c570-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7c570-155">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7c570-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7c570-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7c570-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7c570-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c570-157">RELATED LINKS</span></span>

