---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: fd4d35991364f533eb1a311cc8aac0ce25e1ae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935960"
---
# <span data-ttu-id="9a0a5-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="9a0a5-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="9a0a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0a5-103">Starten Sie die Bereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-103">Restart the deployment.</span></span>

## <span data-ttu-id="9a0a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a0a5-104">SYNTAX</span></span>

### <span data-ttu-id="9a0a5-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a0a5-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a0a5-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a0a5-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a0a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a0a5-107">DESCRIPTION</span></span>
<span data-ttu-id="9a0a5-108">Starten Sie die Bereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-108">Restart the deployment.</span></span>

## <span data-ttu-id="9a0a5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a0a5-109">EXAMPLES</span></span>

### <span data-ttu-id="9a0a5-110">Beispiel 1: Starten Sie den Spring Cloud Service nach Name neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="9a0a5-111">Starten Sie den Spring Cloud Service nach Name neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="9a0a5-112">Beispiel 2: Starten Sie den Quellwolkendienst von pipe neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="9a0a5-113">Starten Sie den Spring Cloud Service von pipe neu.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="9a0a5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9a0a5-114">PARAMETERS</span></span>

### <span data-ttu-id="9a0a5-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="9a0a5-115">-AppName</span></span>
<span data-ttu-id="9a0a5-116">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="9a0a5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a0a5-117">-AsJob</span></span>
<span data-ttu-id="9a0a5-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9a0a5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9a0a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0a5-119">-DefaultProfile</span></span>
<span data-ttu-id="9a0a5-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0a5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a0a5-121">-InputObject</span></span>
<span data-ttu-id="9a0a5-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9a0a5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9a0a5-123">-Name</span></span>
<span data-ttu-id="9a0a5-124">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="9a0a5-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a0a5-125">-NoWait</span></span>
<span data-ttu-id="9a0a5-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9a0a5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a0a5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a0a5-127">-PassThru</span></span>
<span data-ttu-id="9a0a5-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a0a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a0a5-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9a0a5-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9a0a5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9a0a5-132">-ServiceName</span></span>
<span data-ttu-id="9a0a5-133">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="9a0a5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a0a5-134">-SubscriptionId</span></span>
<span data-ttu-id="9a0a5-135">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a0a5-136">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9a0a5-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a0a5-137">-Confirm</span></span>
<span data-ttu-id="9a0a5-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a0a5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a0a5-139">-WhatIf</span></span>
<span data-ttu-id="9a0a5-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a0a5-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a0a5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0a5-142">CommonParameters</span></span>
<span data-ttu-id="9a0a5-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0a5-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a0a5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0a5-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a0a5-145">INPUTS</span></span>

### <span data-ttu-id="9a0a5-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="9a0a5-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="9a0a5-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a0a5-147">OUTPUTS</span></span>

### <span data-ttu-id="9a0a5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a0a5-148">System.Boolean</span></span>

## <span data-ttu-id="9a0a5-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9a0a5-149">NOTES</span></span>

<span data-ttu-id="9a0a5-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9a0a5-150">ALIASES</span></span>

<span data-ttu-id="9a0a5-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9a0a5-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a0a5-152">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a0a5-153">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a0a5-154">INPUTOBJECT <ISpringCloudIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="9a0a5-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a0a5-155">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="9a0a5-156">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="9a0a5-157">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="9a0a5-158">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="9a0a5-159">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="9a0a5-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9a0a5-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a0a5-161">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="9a0a5-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="9a0a5-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9a0a5-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9a0a5-164">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="9a0a5-165">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9a0a5-166">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="9a0a5-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9a0a5-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9a0a5-167">RELATED LINKS</span></span>

