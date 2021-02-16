---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 859ea1febad82dbb09e88debe3f825feab18b1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168777"
---
# <span data-ttu-id="02e6d-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="02e6d-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="02e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="02e6d-103">Starten Sie die Bereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="02e6d-103">Restart the deployment.</span></span>

## <span data-ttu-id="02e6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02e6d-104">SYNTAX</span></span>

### <span data-ttu-id="02e6d-105">Neu starten (Standard)</span><span class="sxs-lookup"><span data-stu-id="02e6d-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02e6d-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="02e6d-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02e6d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e6d-107">DESCRIPTION</span></span>
<span data-ttu-id="02e6d-108">Starten Sie die Bereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="02e6d-108">Restart the deployment.</span></span>

## <span data-ttu-id="02e6d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02e6d-109">EXAMPLES</span></span>

### <span data-ttu-id="02e6d-110">Beispiel 1: Neustarten des Clouddiensts "Spring" nach Name.</span><span class="sxs-lookup"><span data-stu-id="02e6d-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="02e6d-111">Starten Sie den Spring Cloud Service nach Name neu.</span><span class="sxs-lookup"><span data-stu-id="02e6d-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="02e6d-112">Beispiel 2: Neustarten des Clouddiensts "Spring" von Pipe aus.</span><span class="sxs-lookup"><span data-stu-id="02e6d-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="02e6d-113">Starten Sie den Spring Cloud Service von Pipe neu.</span><span class="sxs-lookup"><span data-stu-id="02e6d-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="02e6d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02e6d-114">PARAMETERS</span></span>

### <span data-ttu-id="02e6d-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="02e6d-115">-AppName</span></span>
<span data-ttu-id="02e6d-116">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02e6d-117">-AsJob</span></span>
<span data-ttu-id="02e6d-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="02e6d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="02e6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e6d-119">-DefaultProfile</span></span>
<span data-ttu-id="02e6d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02e6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02e6d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02e6d-121">-InputObject</span></span>
<span data-ttu-id="02e6d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="02e6d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="02e6d-123">-Name</span></span>
<span data-ttu-id="02e6d-124">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02e6d-125">-NoWait</span></span>
<span data-ttu-id="02e6d-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="02e6d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02e6d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02e6d-127">-PassThru</span></span>
<span data-ttu-id="02e6d-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="02e6d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="02e6d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e6d-129">-ResourceGroupName</span></span>
<span data-ttu-id="02e6d-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="02e6d-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="02e6d-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="02e6d-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02e6d-132">-ServiceName</span></span>
<span data-ttu-id="02e6d-133">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02e6d-134">-SubscriptionId</span></span>
<span data-ttu-id="02e6d-135">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02e6d-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="02e6d-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02e6d-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e6d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02e6d-137">-Confirm</span></span>
<span data-ttu-id="02e6d-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02e6d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02e6d-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02e6d-139">-WhatIf</span></span>
<span data-ttu-id="02e6d-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02e6d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02e6d-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02e6d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02e6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e6d-142">CommonParameters</span></span>
<span data-ttu-id="02e6d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e6d-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02e6d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e6d-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02e6d-145">INPUTS</span></span>

### <span data-ttu-id="02e6d-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="02e6d-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="02e6d-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02e6d-147">OUTPUTS</span></span>

### <span data-ttu-id="02e6d-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02e6d-148">System.Boolean</span></span>

## <span data-ttu-id="02e6d-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02e6d-149">NOTES</span></span>

<span data-ttu-id="02e6d-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="02e6d-150">ALIASES</span></span>

<span data-ttu-id="02e6d-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="02e6d-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02e6d-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02e6d-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02e6d-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02e6d-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02e6d-154">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="02e6d-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02e6d-155">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="02e6d-156">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="02e6d-157">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="02e6d-158">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="02e6d-159">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="02e6d-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="02e6d-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02e6d-161">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="02e6d-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="02e6d-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="02e6d-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="02e6d-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="02e6d-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="02e6d-164">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="02e6d-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="02e6d-165">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02e6d-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="02e6d-166">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02e6d-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02e6d-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02e6d-167">RELATED LINKS</span></span>

