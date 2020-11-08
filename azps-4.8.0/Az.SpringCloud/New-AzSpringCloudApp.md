---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: 966a0c0243d8ca8cd982420a9a3018f9d41ab52e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174138"
---
# <span data-ttu-id="2bcbf-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2bcbf-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="2bcbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bcbf-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcbf-103">Erstellen Sie eine neue APP, oder aktualisieren Sie eine beendende app.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="2bcbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bcbf-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2bcbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bcbf-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcbf-106">Erstellen Sie eine neue APP, oder aktualisieren Sie eine beendende app.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="2bcbf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bcbf-107">EXAMPLES</span></span>

### <span data-ttu-id="2bcbf-108">Beispiel 1: Erstellen einer APP für die Frühlings Wolke</span><span class="sxs-lookup"><span data-stu-id="2bcbf-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="2bcbf-109">Erstellen Sie eine APP für die Frühlings Wolke.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="2bcbf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bcbf-110">PARAMETERS</span></span>

### <span data-ttu-id="2bcbf-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2bcbf-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="2bcbf-112">Name der aktiven Bereitstellung der APP</span><span class="sxs-lookup"><span data-stu-id="2bcbf-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="2bcbf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bcbf-113">-AsJob</span></span>
<span data-ttu-id="2bcbf-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2bcbf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2bcbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcbf-115">-DefaultProfile</span></span>
<span data-ttu-id="2bcbf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bcbf-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2bcbf-117">-Fqdn</span></span>
<span data-ttu-id="2bcbf-118">Vollständig qualifizierter DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="2bcbf-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2bcbf-119">-HttpsOnly</span></span>
<span data-ttu-id="2bcbf-120">Geben Sie an, ob nur HTTPS zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="2bcbf-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2bcbf-121">-Location</span></span>
<span data-ttu-id="2bcbf-122">Die Geo-Position der Anwendung, immer identisch mit der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="2bcbf-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="2bcbf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2bcbf-123">-Name</span></span>
<span data-ttu-id="2bcbf-124">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="2bcbf-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2bcbf-125">-NoWait</span></span>
<span data-ttu-id="2bcbf-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2bcbf-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2bcbf-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2bcbf-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="2bcbf-128">Bereitstellungspfad des beständigen Datenträgers</span><span class="sxs-lookup"><span data-stu-id="2bcbf-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="2bcbf-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2bcbf-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="2bcbf-130">Größe des beständigen Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="2bcbf-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="2bcbf-131">-Öffentlich</span><span class="sxs-lookup"><span data-stu-id="2bcbf-131">-Public</span></span>
<span data-ttu-id="2bcbf-132">Gibt an, ob die APP öffentlichen Endpunkt verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="2bcbf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bcbf-133">-ResourceGroupName</span></span>
<span data-ttu-id="2bcbf-134">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2bcbf-135">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2bcbf-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2bcbf-136">-ServiceName</span></span>
<span data-ttu-id="2bcbf-137">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2bcbf-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2bcbf-138">-SubscriptionId</span></span>
<span data-ttu-id="2bcbf-139">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2bcbf-140">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2bcbf-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2bcbf-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="2bcbf-142">Bereitstellungspfad des temporären Datenträgers</span><span class="sxs-lookup"><span data-stu-id="2bcbf-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="2bcbf-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2bcbf-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="2bcbf-144">Größe des temporären Datenträgers in GB</span><span class="sxs-lookup"><span data-stu-id="2bcbf-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="2bcbf-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bcbf-145">-Confirm</span></span>
<span data-ttu-id="2bcbf-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bcbf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bcbf-147">-WhatIf</span></span>
<span data-ttu-id="2bcbf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bcbf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bcbf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcbf-150">CommonParameters</span></span>
<span data-ttu-id="2bcbf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bcbf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcbf-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bcbf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcbf-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bcbf-153">INPUTS</span></span>

## <span data-ttu-id="2bcbf-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bcbf-154">OUTPUTS</span></span>

### <span data-ttu-id="2bcbf-155">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="2bcbf-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="2bcbf-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bcbf-156">NOTES</span></span>

<span data-ttu-id="2bcbf-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="2bcbf-157">ALIASES</span></span>

## <span data-ttu-id="2bcbf-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bcbf-158">RELATED LINKS</span></span>

