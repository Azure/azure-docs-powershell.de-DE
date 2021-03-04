---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 2c16d60bc9a2b11e34c968eba552c6f8693f92f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920920"
---
# <span data-ttu-id="7bb43-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="7bb43-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="7bb43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb43-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb43-103">Starten Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="7bb43-103">Start the deployment.</span></span>

## <span data-ttu-id="7bb43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bb43-104">SYNTAX</span></span>

### <span data-ttu-id="7bb43-105">Start (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bb43-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7bb43-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7bb43-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7bb43-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bb43-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb43-108">Starten Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="7bb43-108">Start the deployment.</span></span>

## <span data-ttu-id="7bb43-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bb43-109">EXAMPLES</span></span>

### <span data-ttu-id="7bb43-110">Beispiel 1: Starten des Quellwolkendiensts nach Name.</span><span class="sxs-lookup"><span data-stu-id="7bb43-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="7bb43-111">Starten Sie den Spring Cloud Service nach Name.</span><span class="sxs-lookup"><span data-stu-id="7bb43-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="7bb43-112">Beispiel 2: Starten des Quellwolkendiensts über pipe.</span><span class="sxs-lookup"><span data-stu-id="7bb43-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="7bb43-113">Starten Sie den Frühlingswolkendienst über pipe.</span><span class="sxs-lookup"><span data-stu-id="7bb43-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="7bb43-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7bb43-114">PARAMETERS</span></span>

### <span data-ttu-id="7bb43-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="7bb43-115">-AppName</span></span>
<span data-ttu-id="7bb43-116">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bb43-117">-AsJob</span></span>
<span data-ttu-id="7bb43-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7bb43-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7bb43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb43-119">-DefaultProfile</span></span>
<span data-ttu-id="7bb43-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bb43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb43-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bb43-121">-InputObject</span></span>
<span data-ttu-id="7bb43-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7bb43-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7bb43-123">-Name</span></span>
<span data-ttu-id="7bb43-124">Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7bb43-125">-NoWait</span></span>
<span data-ttu-id="7bb43-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7bb43-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7bb43-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bb43-127">-PassThru</span></span>
<span data-ttu-id="7bb43-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb43-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7bb43-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb43-129">-ResourceGroupName</span></span>
<span data-ttu-id="7bb43-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7bb43-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7bb43-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7bb43-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7bb43-132">-ServiceName</span></span>
<span data-ttu-id="7bb43-133">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bb43-134">-SubscriptionId</span></span>
<span data-ttu-id="7bb43-135">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7bb43-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7bb43-136">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7bb43-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb43-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bb43-137">-Confirm</span></span>
<span data-ttu-id="7bb43-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bb43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb43-139">-WhatIf</span></span>
<span data-ttu-id="7bb43-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb43-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb43-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bb43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb43-142">CommonParameters</span></span>
<span data-ttu-id="7bb43-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb43-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bb43-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb43-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bb43-145">INPUTS</span></span>

### <span data-ttu-id="7bb43-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7bb43-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7bb43-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bb43-147">OUTPUTS</span></span>

### <span data-ttu-id="7bb43-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bb43-148">System.Boolean</span></span>

## <span data-ttu-id="7bb43-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7bb43-149">NOTES</span></span>

<span data-ttu-id="7bb43-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7bb43-150">ALIASES</span></span>

<span data-ttu-id="7bb43-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7bb43-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7bb43-152">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7bb43-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bb43-153">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7bb43-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7bb43-154">INPUTOBJECT <ISpringCloudIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7bb43-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7bb43-155">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7bb43-156">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7bb43-157">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7bb43-158">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7bb43-159">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7bb43-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7bb43-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7bb43-161">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="7bb43-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7bb43-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7bb43-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7bb43-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7bb43-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7bb43-164">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7bb43-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7bb43-165">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7bb43-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7bb43-166">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7bb43-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7bb43-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7bb43-167">RELATED LINKS</span></span>

