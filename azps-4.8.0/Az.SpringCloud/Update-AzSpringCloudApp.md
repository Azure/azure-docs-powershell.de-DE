---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: e4d7d502d96245291fce001f4706ae44f21f5fed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173493"
---
# <span data-ttu-id="b40ff-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="b40ff-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="b40ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b40ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b40ff-103">Vorgang zum Aktualisieren einer beendenden App</span><span class="sxs-lookup"><span data-stu-id="b40ff-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="b40ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b40ff-104">SYNTAX</span></span>

### <span data-ttu-id="b40ff-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b40ff-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b40ff-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b40ff-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b40ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b40ff-107">DESCRIPTION</span></span>
<span data-ttu-id="b40ff-108">Vorgang zum Aktualisieren einer beendenden App</span><span class="sxs-lookup"><span data-stu-id="b40ff-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="b40ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b40ff-109">EXAMPLES</span></span>

### <span data-ttu-id="b40ff-110">Beispiel 1: Aktualisieren der APP für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="b40ff-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="b40ff-111">Aktualisieren Sie die APP für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="b40ff-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="b40ff-112">Beispiel 2: Aktualisieren der APP für die Frühlings Wolke aus Pipe</span><span class="sxs-lookup"><span data-stu-id="b40ff-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="b40ff-113">Aktualisieren Sie die APP für die Frühlings Wolke aus Pipe.</span><span class="sxs-lookup"><span data-stu-id="b40ff-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="b40ff-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b40ff-114">PARAMETERS</span></span>

### <span data-ttu-id="b40ff-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b40ff-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="b40ff-116">Name der aktiven Bereitstellung der APP</span><span class="sxs-lookup"><span data-stu-id="b40ff-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="b40ff-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b40ff-117">-AsJob</span></span>
<span data-ttu-id="b40ff-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b40ff-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b40ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40ff-119">-DefaultProfile</span></span>
<span data-ttu-id="b40ff-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b40ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b40ff-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="b40ff-121">-Fqdn</span></span>
<span data-ttu-id="b40ff-122">Vollständig qualifizierter DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="b40ff-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="b40ff-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b40ff-123">-HttpsOnly</span></span>
<span data-ttu-id="b40ff-124">Geben Sie an, ob nur HTTPS zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b40ff-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="b40ff-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b40ff-125">-InputObject</span></span>
<span data-ttu-id="b40ff-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b40ff-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b40ff-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="b40ff-127">-Location</span></span>
<span data-ttu-id="b40ff-128">Die Geo-Position der Anwendung, immer identisch mit der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="b40ff-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="b40ff-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b40ff-129">-Name</span></span>
<span data-ttu-id="b40ff-130">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="b40ff-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b40ff-131">-NoWait</span></span>
<span data-ttu-id="b40ff-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b40ff-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b40ff-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="b40ff-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="b40ff-134">Bereitstellungspfad des beständigen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="b40ff-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="b40ff-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b40ff-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="b40ff-136">Größe des beständigen Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="b40ff-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="b40ff-137">-Öffentlich</span><span class="sxs-lookup"><span data-stu-id="b40ff-137">-Public</span></span>
<span data-ttu-id="b40ff-138">Gibt an, ob die APP öffentlichen Endpunkt verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b40ff-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="b40ff-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40ff-139">-ResourceGroupName</span></span>
<span data-ttu-id="b40ff-140">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b40ff-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b40ff-141">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b40ff-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b40ff-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b40ff-142">-ServiceName</span></span>
<span data-ttu-id="b40ff-143">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b40ff-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b40ff-144">-SubscriptionId</span></span>
<span data-ttu-id="b40ff-145">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b40ff-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b40ff-146">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b40ff-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b40ff-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="b40ff-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="b40ff-148">Bereitstellungspfad des temporären Datenträgers</span><span class="sxs-lookup"><span data-stu-id="b40ff-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="b40ff-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b40ff-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="b40ff-150">Größe des temporären Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="b40ff-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="b40ff-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b40ff-151">-Confirm</span></span>
<span data-ttu-id="b40ff-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b40ff-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b40ff-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40ff-153">-WhatIf</span></span>
<span data-ttu-id="b40ff-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b40ff-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b40ff-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b40ff-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b40ff-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40ff-156">CommonParameters</span></span>
<span data-ttu-id="b40ff-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40ff-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40ff-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b40ff-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40ff-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b40ff-159">INPUTS</span></span>

### <span data-ttu-id="b40ff-160">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b40ff-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b40ff-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b40ff-161">OUTPUTS</span></span>

### <span data-ttu-id="b40ff-162">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="b40ff-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="b40ff-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="b40ff-163">NOTES</span></span>

<span data-ttu-id="b40ff-164">Aliase</span><span class="sxs-lookup"><span data-stu-id="b40ff-164">ALIASES</span></span>

<span data-ttu-id="b40ff-165">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b40ff-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b40ff-166">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b40ff-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b40ff-167">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b40ff-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b40ff-168">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b40ff-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b40ff-169">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b40ff-170">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b40ff-171">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b40ff-172">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b40ff-173">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b40ff-174">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b40ff-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b40ff-175">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="b40ff-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b40ff-176">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b40ff-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b40ff-177">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b40ff-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b40ff-178">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="b40ff-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b40ff-179">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b40ff-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b40ff-180">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b40ff-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b40ff-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b40ff-181">RELATED LINKS</span></span>

