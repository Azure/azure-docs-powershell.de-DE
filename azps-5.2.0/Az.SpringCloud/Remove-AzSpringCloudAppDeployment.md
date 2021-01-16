---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294047"
---
# <span data-ttu-id="261c7-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="261c7-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="261c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261c7-102">SYNOPSIS</span></span>
<span data-ttu-id="261c7-103">Vorgang zum Löschen einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="261c7-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="261c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="261c7-104">SYNTAX</span></span>

### <span data-ttu-id="261c7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="261c7-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="261c7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="261c7-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="261c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="261c7-107">DESCRIPTION</span></span>
<span data-ttu-id="261c7-108">Vorgang zum Löschen einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="261c7-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="261c7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="261c7-109">EXAMPLES</span></span>

### <span data-ttu-id="261c7-110">Beispiel 1: Entfernen der Bereitstellung der Quellwolke nach Name.</span><span class="sxs-lookup"><span data-stu-id="261c7-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="261c7-111">Entfernen Sie die Bereitstellung der Quellwolke nach Name.</span><span class="sxs-lookup"><span data-stu-id="261c7-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="261c7-112">Beispiel 2: Entfernen der Bereitstellung der Quellwolke aus dem Pipe.</span><span class="sxs-lookup"><span data-stu-id="261c7-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="261c7-113">Entfernen Sie die Bereitstellung der Quellwolke aus dem Pipe.</span><span class="sxs-lookup"><span data-stu-id="261c7-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="261c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="261c7-114">PARAMETERS</span></span>

### <span data-ttu-id="261c7-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="261c7-115">-AppName</span></span>
<span data-ttu-id="261c7-116">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="261c7-117">-AsJob</span></span>
<span data-ttu-id="261c7-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="261c7-118">Run the command as a job</span></span>

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

### <span data-ttu-id="261c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261c7-119">-DefaultProfile</span></span>
<span data-ttu-id="261c7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="261c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261c7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="261c7-121">-InputObject</span></span>
<span data-ttu-id="261c7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="261c7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="261c7-123">-Name</span></span>
<span data-ttu-id="261c7-124">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="261c7-125">-NoWait</span></span>
<span data-ttu-id="261c7-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="261c7-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="261c7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="261c7-127">-PassThru</span></span>
<span data-ttu-id="261c7-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="261c7-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="261c7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261c7-129">-ResourceGroupName</span></span>
<span data-ttu-id="261c7-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="261c7-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="261c7-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="261c7-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="261c7-132">-ServiceName</span></span>
<span data-ttu-id="261c7-133">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="261c7-134">-SubscriptionId</span></span>
<span data-ttu-id="261c7-135">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="261c7-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="261c7-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="261c7-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261c7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="261c7-137">-Confirm</span></span>
<span data-ttu-id="261c7-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="261c7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261c7-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="261c7-139">-WhatIf</span></span>
<span data-ttu-id="261c7-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="261c7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261c7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="261c7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261c7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261c7-142">CommonParameters</span></span>
<span data-ttu-id="261c7-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261c7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261c7-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="261c7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261c7-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="261c7-145">INPUTS</span></span>

### <span data-ttu-id="261c7-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="261c7-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="261c7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="261c7-147">OUTPUTS</span></span>

### <span data-ttu-id="261c7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="261c7-148">System.Boolean</span></span>

## <span data-ttu-id="261c7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="261c7-149">NOTES</span></span>

<span data-ttu-id="261c7-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="261c7-150">ALIASES</span></span>

<span data-ttu-id="261c7-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="261c7-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="261c7-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="261c7-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="261c7-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="261c7-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="261c7-154">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="261c7-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="261c7-155">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="261c7-156">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="261c7-157">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="261c7-158">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="261c7-159">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="261c7-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="261c7-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="261c7-161">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="261c7-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="261c7-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="261c7-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="261c7-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="261c7-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="261c7-164">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="261c7-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="261c7-165">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="261c7-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="261c7-166">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="261c7-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="261c7-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="261c7-167">RELATED LINKS</span></span>

