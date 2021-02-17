---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165020"
---
# <span data-ttu-id="da248-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="da248-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="da248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da248-102">SYNOPSIS</span></span>
<span data-ttu-id="da248-103">Vorgang zum Löschen eines Diensts.</span><span class="sxs-lookup"><span data-stu-id="da248-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="da248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da248-104">SYNTAX</span></span>

### <span data-ttu-id="da248-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="da248-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da248-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da248-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da248-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da248-107">DESCRIPTION</span></span>
<span data-ttu-id="da248-108">Vorgang zum Löschen eines Diensts.</span><span class="sxs-lookup"><span data-stu-id="da248-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="da248-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da248-109">EXAMPLES</span></span>

### <span data-ttu-id="da248-110">Beispiel 1: Entfernen des Quell-Cloud-Diensts nach Name.</span><span class="sxs-lookup"><span data-stu-id="da248-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="da248-111">Entfernen Sie den Spring Cloud Service nach Name.</span><span class="sxs-lookup"><span data-stu-id="da248-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="da248-112">Beispiel 2: Entfernen des Spring Cloud Service von Pipe.</span><span class="sxs-lookup"><span data-stu-id="da248-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="da248-113">Entfernen Sie den Spring Cloud Service aus dem Pipe.</span><span class="sxs-lookup"><span data-stu-id="da248-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="da248-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da248-114">PARAMETERS</span></span>

### <span data-ttu-id="da248-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da248-115">-AsJob</span></span>
<span data-ttu-id="da248-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="da248-116">Run the command as a job</span></span>

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

### <span data-ttu-id="da248-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da248-117">-DefaultProfile</span></span>
<span data-ttu-id="da248-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da248-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da248-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da248-119">-InputObject</span></span>
<span data-ttu-id="da248-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="da248-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da248-121">-Name</span><span class="sxs-lookup"><span data-stu-id="da248-121">-Name</span></span>
<span data-ttu-id="da248-122">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="da248-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da248-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da248-123">-NoWait</span></span>
<span data-ttu-id="da248-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="da248-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da248-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da248-125">-PassThru</span></span>
<span data-ttu-id="da248-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="da248-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da248-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da248-127">-ResourceGroupName</span></span>
<span data-ttu-id="da248-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="da248-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="da248-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="da248-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="da248-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da248-130">-SubscriptionId</span></span>
<span data-ttu-id="da248-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="da248-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="da248-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="da248-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da248-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da248-133">-Confirm</span></span>
<span data-ttu-id="da248-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da248-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da248-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da248-135">-WhatIf</span></span>
<span data-ttu-id="da248-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da248-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da248-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da248-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da248-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da248-138">CommonParameters</span></span>
<span data-ttu-id="da248-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da248-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da248-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da248-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da248-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da248-141">INPUTS</span></span>

### <span data-ttu-id="da248-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="da248-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="da248-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da248-143">OUTPUTS</span></span>

### <span data-ttu-id="da248-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da248-144">System.Boolean</span></span>

## <span data-ttu-id="da248-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da248-145">NOTES</span></span>

<span data-ttu-id="da248-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="da248-146">ALIASES</span></span>

<span data-ttu-id="da248-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="da248-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da248-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da248-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da248-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da248-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da248-150">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="da248-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da248-151">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="da248-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="da248-152">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="da248-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="da248-153">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="da248-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="da248-154">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="da248-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="da248-155">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="da248-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="da248-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="da248-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da248-157">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="da248-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="da248-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="da248-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="da248-159">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="da248-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="da248-160">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="da248-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="da248-161">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="da248-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="da248-162">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="da248-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="da248-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da248-163">RELATED LINKS</span></span>

