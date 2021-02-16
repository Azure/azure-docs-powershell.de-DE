---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150628"
---
# <span data-ttu-id="970f4-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="970f4-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="970f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="970f4-102">SYNOPSIS</span></span>
<span data-ttu-id="970f4-103">Erstellen Sie eine neue App, oder aktualisieren Sie eine beendende App.</span><span class="sxs-lookup"><span data-stu-id="970f4-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="970f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="970f4-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="970f4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="970f4-105">DESCRIPTION</span></span>
<span data-ttu-id="970f4-106">Erstellen Sie eine neue App, oder aktualisieren Sie eine beendende App.</span><span class="sxs-lookup"><span data-stu-id="970f4-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="970f4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="970f4-107">EXAMPLES</span></span>

### <span data-ttu-id="970f4-108">Beispiel 1: Erstellen einer Quell-Cloud-App.</span><span class="sxs-lookup"><span data-stu-id="970f4-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="970f4-109">Erstellen Sie eine Quell-Cloud-App.</span><span class="sxs-lookup"><span data-stu-id="970f4-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="970f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="970f4-110">PARAMETERS</span></span>

### <span data-ttu-id="970f4-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="970f4-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="970f4-112">Name der aktiven Bereitstellung der App</span><span class="sxs-lookup"><span data-stu-id="970f4-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="970f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="970f4-113">-AsJob</span></span>
<span data-ttu-id="970f4-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="970f4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="970f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970f4-115">-DefaultProfile</span></span>
<span data-ttu-id="970f4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="970f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="970f4-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="970f4-117">-Fqdn</span></span>
<span data-ttu-id="970f4-118">Vollqualifizierter DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="970f4-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="970f4-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="970f4-119">-HttpsOnly</span></span>
<span data-ttu-id="970f4-120">Geben Sie an, ob nur https zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="970f4-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="970f4-121">-Location</span><span class="sxs-lookup"><span data-stu-id="970f4-121">-Location</span></span>
<span data-ttu-id="970f4-122">Der GEO-Standort der Anwendung, immer identisch mit der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="970f4-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="970f4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="970f4-123">-Name</span></span>
<span data-ttu-id="970f4-124">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="970f4-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="970f4-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="970f4-125">-NoWait</span></span>
<span data-ttu-id="970f4-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="970f4-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="970f4-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="970f4-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="970f4-128">Bereitstellungspfad des beständigen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="970f4-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="970f4-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="970f4-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="970f4-130">Größe des beständigen Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="970f4-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="970f4-131">-Public</span><span class="sxs-lookup"><span data-stu-id="970f4-131">-Public</span></span>
<span data-ttu-id="970f4-132">Gibt an, ob die App einen öffentlichen Endpunkt verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="970f4-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="970f4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="970f4-133">-ResourceGroupName</span></span>
<span data-ttu-id="970f4-134">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="970f4-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="970f4-135">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="970f4-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="970f4-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="970f4-136">-ServiceName</span></span>
<span data-ttu-id="970f4-137">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="970f4-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="970f4-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="970f4-138">-SubscriptionId</span></span>
<span data-ttu-id="970f4-139">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="970f4-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="970f4-140">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="970f4-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="970f4-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="970f4-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="970f4-142">Bereitstellungspfad des temporären Datenträgers</span><span class="sxs-lookup"><span data-stu-id="970f4-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="970f4-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="970f4-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="970f4-144">Größe des temporären Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="970f4-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="970f4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="970f4-145">-Confirm</span></span>
<span data-ttu-id="970f4-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="970f4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="970f4-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="970f4-147">-WhatIf</span></span>
<span data-ttu-id="970f4-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="970f4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="970f4-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="970f4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="970f4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970f4-150">CommonParameters</span></span>
<span data-ttu-id="970f4-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970f4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970f4-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="970f4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970f4-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="970f4-153">INPUTS</span></span>

## <span data-ttu-id="970f4-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="970f4-154">OUTPUTS</span></span>

### <span data-ttu-id="970f4-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="970f4-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="970f4-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="970f4-156">NOTES</span></span>

<span data-ttu-id="970f4-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="970f4-157">ALIASES</span></span>

## <span data-ttu-id="970f4-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="970f4-158">RELATED LINKS</span></span>

