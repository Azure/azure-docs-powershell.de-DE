---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375653"
---
# <span data-ttu-id="e306c-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="e306c-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="e306c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e306c-102">SYNOPSIS</span></span>
<span data-ttu-id="e306c-103">Vorgang zum Aktualisieren einer beendenden App.</span><span class="sxs-lookup"><span data-stu-id="e306c-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="e306c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e306c-104">SYNTAX</span></span>

### <span data-ttu-id="e306c-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e306c-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e306c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e306c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e306c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e306c-107">DESCRIPTION</span></span>
<span data-ttu-id="e306c-108">Vorgang zum Aktualisieren einer beendenden App.</span><span class="sxs-lookup"><span data-stu-id="e306c-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="e306c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e306c-109">EXAMPLES</span></span>

### <span data-ttu-id="e306c-110">Beispiel 1: Aktualisieren der Spring Cloud App nach Name.</span><span class="sxs-lookup"><span data-stu-id="e306c-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
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

<span data-ttu-id="e306c-111">Aktualisieren Sie die Spring Cloud App nach Name.</span><span class="sxs-lookup"><span data-stu-id="e306c-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="e306c-112">Beispiel 2: Aktualisieren der Spring Cloud App über Pipe.</span><span class="sxs-lookup"><span data-stu-id="e306c-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
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

<span data-ttu-id="e306c-113">Aktualisieren Sie die Spring Cloud App über Pipe.</span><span class="sxs-lookup"><span data-stu-id="e306c-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="e306c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e306c-114">PARAMETERS</span></span>

### <span data-ttu-id="e306c-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e306c-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="e306c-116">Name der aktiven Bereitstellung der App</span><span class="sxs-lookup"><span data-stu-id="e306c-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="e306c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e306c-117">-AsJob</span></span>
<span data-ttu-id="e306c-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e306c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e306c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e306c-119">-DefaultProfile</span></span>
<span data-ttu-id="e306c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e306c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e306c-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="e306c-121">-Fqdn</span></span>
<span data-ttu-id="e306c-122">Vollqualifizierter DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="e306c-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="e306c-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e306c-123">-HttpsOnly</span></span>
<span data-ttu-id="e306c-124">Geben Sie an, ob nur https zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e306c-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="e306c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e306c-125">-InputObject</span></span>
<span data-ttu-id="e306c-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e306c-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e306c-127">-Location</span><span class="sxs-lookup"><span data-stu-id="e306c-127">-Location</span></span>
<span data-ttu-id="e306c-128">Der GEO-Standort der Anwendung, immer identisch mit der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="e306c-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="e306c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e306c-129">-Name</span></span>
<span data-ttu-id="e306c-130">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e306c-131">-NoWait</span></span>
<span data-ttu-id="e306c-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e306c-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e306c-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="e306c-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="e306c-134">Bereitstellungspfad des beständigen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="e306c-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="e306c-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="e306c-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="e306c-136">Größe des beständigen Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="e306c-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="e306c-137">-Public</span><span class="sxs-lookup"><span data-stu-id="e306c-137">-Public</span></span>
<span data-ttu-id="e306c-138">Gibt an, ob die App einen öffentlichen Endpunkt verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e306c-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="e306c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e306c-139">-ResourceGroupName</span></span>
<span data-ttu-id="e306c-140">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e306c-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e306c-141">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e306c-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e306c-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e306c-142">-ServiceName</span></span>
<span data-ttu-id="e306c-143">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e306c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e306c-144">-SubscriptionId</span></span>
<span data-ttu-id="e306c-145">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e306c-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e306c-146">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e306c-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e306c-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="e306c-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="e306c-148">Bereitstellungspfad des temporären Datenträgers</span><span class="sxs-lookup"><span data-stu-id="e306c-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="e306c-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="e306c-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="e306c-150">Größe des temporären Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="e306c-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="e306c-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e306c-151">-Confirm</span></span>
<span data-ttu-id="e306c-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e306c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e306c-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e306c-153">-WhatIf</span></span>
<span data-ttu-id="e306c-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e306c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e306c-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e306c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e306c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e306c-156">CommonParameters</span></span>
<span data-ttu-id="e306c-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e306c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e306c-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e306c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e306c-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e306c-159">INPUTS</span></span>

### <span data-ttu-id="e306c-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e306c-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e306c-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e306c-161">OUTPUTS</span></span>

### <span data-ttu-id="e306c-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="e306c-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="e306c-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e306c-163">NOTES</span></span>

<span data-ttu-id="e306c-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e306c-164">ALIASES</span></span>

<span data-ttu-id="e306c-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e306c-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e306c-166">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e306c-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e306c-167">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e306c-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e306c-168">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e306c-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e306c-169">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e306c-170">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e306c-171">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e306c-172">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e306c-173">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e306c-174">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e306c-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e306c-175">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="e306c-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e306c-176">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e306c-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e306c-177">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e306c-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e306c-178">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="e306c-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e306c-179">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e306c-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e306c-180">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e306c-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e306c-181">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e306c-181">RELATED LINKS</span></span>

