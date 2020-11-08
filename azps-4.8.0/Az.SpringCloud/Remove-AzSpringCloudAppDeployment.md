---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010468"
---
# <span data-ttu-id="d2647-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d2647-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d2647-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2647-102">SYNOPSIS</span></span>
<span data-ttu-id="d2647-103">Vorgang zum Löschen einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d2647-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="d2647-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2647-104">SYNTAX</span></span>

### <span data-ttu-id="d2647-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2647-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2647-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2647-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2647-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2647-107">DESCRIPTION</span></span>
<span data-ttu-id="d2647-108">Vorgang zum Löschen einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d2647-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="d2647-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2647-109">EXAMPLES</span></span>

### <span data-ttu-id="d2647-110">Beispiel 1: Entfernen Sie die Bereitstellung der Feder Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="d2647-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="d2647-111">Entfernen Sie die Bereitstellung der Quell Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="d2647-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="d2647-112">Beispiel 2: Entfernen der Bereitstellung für die Quell Wolke aus Pipe</span><span class="sxs-lookup"><span data-stu-id="d2647-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="d2647-113">Entfernen Sie die Bereitstellung der Quell Wolke aus Pipe.</span><span class="sxs-lookup"><span data-stu-id="d2647-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="d2647-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2647-114">PARAMETERS</span></span>

### <span data-ttu-id="d2647-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="d2647-115">-AppName</span></span>
<span data-ttu-id="d2647-116">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="d2647-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2647-117">-DefaultProfile</span></span>
<span data-ttu-id="d2647-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2647-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2647-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2647-119">-InputObject</span></span>
<span data-ttu-id="d2647-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d2647-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2647-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d2647-121">-Name</span></span>
<span data-ttu-id="d2647-122">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-122">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="d2647-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2647-123">-PassThru</span></span>
<span data-ttu-id="d2647-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="d2647-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2647-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2647-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2647-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d2647-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d2647-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d2647-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d2647-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2647-128">-ServiceName</span></span>
<span data-ttu-id="d2647-129">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d2647-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d2647-130">-SubscriptionId</span></span>
<span data-ttu-id="d2647-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d2647-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2647-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d2647-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2647-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2647-133">-Confirm</span></span>
<span data-ttu-id="d2647-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2647-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2647-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2647-135">-WhatIf</span></span>
<span data-ttu-id="d2647-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2647-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2647-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2647-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2647-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2647-138">CommonParameters</span></span>
<span data-ttu-id="d2647-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2647-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2647-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2647-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2647-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2647-141">INPUTS</span></span>

### <span data-ttu-id="d2647-142">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d2647-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d2647-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2647-143">OUTPUTS</span></span>

### <span data-ttu-id="d2647-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2647-144">System.Boolean</span></span>

## <span data-ttu-id="d2647-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2647-145">NOTES</span></span>

<span data-ttu-id="d2647-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="d2647-146">ALIASES</span></span>

<span data-ttu-id="d2647-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2647-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2647-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2647-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2647-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d2647-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2647-150">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d2647-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2647-151">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d2647-152">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d2647-153">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d2647-154">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d2647-155">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d2647-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d2647-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2647-157">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="d2647-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d2647-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d2647-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d2647-159">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d2647-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d2647-160">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="d2647-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d2647-161">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d2647-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d2647-162">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d2647-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2647-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2647-163">RELATED LINKS</span></span>

