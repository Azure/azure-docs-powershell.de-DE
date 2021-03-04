---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: c6dccbaa5e398d5d00b02a28cc8942b9e5264859
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931496"
---
# <span data-ttu-id="b2d31-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="b2d31-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="b2d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d31-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d31-103">Vorgang zum Löschen einer App.</span><span class="sxs-lookup"><span data-stu-id="b2d31-103">Operation to delete an App.</span></span>

## <span data-ttu-id="b2d31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2d31-104">SYNTAX</span></span>

### <span data-ttu-id="b2d31-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2d31-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b2d31-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2d31-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2d31-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2d31-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d31-108">Vorgang zum Löschen einer App.</span><span class="sxs-lookup"><span data-stu-id="b2d31-108">Operation to delete an App.</span></span>

## <span data-ttu-id="b2d31-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2d31-109">EXAMPLES</span></span>

### <span data-ttu-id="b2d31-110">Beispiel 1: Entfernen Der Name der Spring Cloud App.</span><span class="sxs-lookup"><span data-stu-id="b2d31-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="b2d31-111">Entfernen Sie die Spring Cloud App nach Name.</span><span class="sxs-lookup"><span data-stu-id="b2d31-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="b2d31-112">Beispiel 2: Entfernen der Spring Cloud App aus pipe.</span><span class="sxs-lookup"><span data-stu-id="b2d31-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="b2d31-113">Entfernen Sie die Spring Cloud App aus pipe.</span><span class="sxs-lookup"><span data-stu-id="b2d31-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="b2d31-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2d31-114">PARAMETERS</span></span>

### <span data-ttu-id="b2d31-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2d31-115">-AsJob</span></span>
<span data-ttu-id="b2d31-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b2d31-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b2d31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d31-117">-DefaultProfile</span></span>
<span data-ttu-id="b2d31-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2d31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2d31-119">-InputObject</span></span>
<span data-ttu-id="b2d31-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b2d31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2d31-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2d31-121">-Name</span></span>
<span data-ttu-id="b2d31-122">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d31-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b2d31-123">-NoWait</span></span>
<span data-ttu-id="b2d31-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b2d31-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b2d31-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2d31-125">-PassThru</span></span>
<span data-ttu-id="b2d31-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d31-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b2d31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d31-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2d31-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b2d31-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b2d31-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b2d31-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b2d31-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2d31-130">-ServiceName</span></span>
<span data-ttu-id="b2d31-131">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b2d31-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2d31-132">-SubscriptionId</span></span>
<span data-ttu-id="b2d31-133">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b2d31-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2d31-134">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b2d31-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2d31-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2d31-135">-Confirm</span></span>
<span data-ttu-id="b2d31-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2d31-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d31-137">-WhatIf</span></span>
<span data-ttu-id="b2d31-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d31-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2d31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d31-140">CommonParameters</span></span>
<span data-ttu-id="b2d31-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d31-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2d31-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d31-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2d31-143">INPUTS</span></span>

### <span data-ttu-id="b2d31-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b2d31-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b2d31-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2d31-145">OUTPUTS</span></span>

### <span data-ttu-id="b2d31-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2d31-146">System.Boolean</span></span>

## <span data-ttu-id="b2d31-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2d31-147">NOTES</span></span>

<span data-ttu-id="b2d31-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b2d31-148">ALIASES</span></span>

<span data-ttu-id="b2d31-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b2d31-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2d31-150">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b2d31-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2d31-151">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2d31-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2d31-152">INPUTOBJECT <ISpringCloudIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b2d31-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2d31-153">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b2d31-154">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b2d31-155">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b2d31-156">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b2d31-157">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b2d31-158">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b2d31-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2d31-159">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="b2d31-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b2d31-160">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b2d31-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b2d31-161">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b2d31-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b2d31-162">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="b2d31-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b2d31-163">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b2d31-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b2d31-164">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b2d31-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b2d31-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2d31-165">RELATED LINKS</span></span>

