---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166843"
---
# <span data-ttu-id="cd59d-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="cd59d-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="cd59d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd59d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd59d-103">Beenden Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="cd59d-103">Stop the deployment.</span></span>

## <span data-ttu-id="cd59d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd59d-104">SYNTAX</span></span>

### <span data-ttu-id="cd59d-105">Stopp (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd59d-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd59d-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd59d-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd59d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd59d-107">DESCRIPTION</span></span>
<span data-ttu-id="cd59d-108">Beenden Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="cd59d-108">Stop the deployment.</span></span>

## <span data-ttu-id="cd59d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd59d-109">EXAMPLES</span></span>

### <span data-ttu-id="cd59d-110">Beispiel 1: Beenden Sie den Spring Cloud-Dienst nach dem Namen.</span><span class="sxs-lookup"><span data-stu-id="cd59d-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="cd59d-111">Beenden Sie den Spring Cloud-Dienst nach Namen.</span><span class="sxs-lookup"><span data-stu-id="cd59d-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="cd59d-112">Beispiel 2: Beenden des Spring Cloud-Diensts aus Pipe</span><span class="sxs-lookup"><span data-stu-id="cd59d-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="cd59d-113">Beenden Sie den Spring Cloud-Dienst von Pipe.</span><span class="sxs-lookup"><span data-stu-id="cd59d-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="cd59d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd59d-114">PARAMETERS</span></span>

### <span data-ttu-id="cd59d-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="cd59d-115">-AppName</span></span>
<span data-ttu-id="cd59d-116">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd59d-117">-AsJob</span></span>
<span data-ttu-id="cd59d-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="cd59d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="cd59d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd59d-119">-DefaultProfile</span></span>
<span data-ttu-id="cd59d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd59d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd59d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd59d-121">-InputObject</span></span>
<span data-ttu-id="cd59d-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cd59d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cd59d-123">-Name</span></span>
<span data-ttu-id="cd59d-124">Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cd59d-125">-NoWait</span></span>
<span data-ttu-id="cd59d-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="cd59d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd59d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd59d-127">-PassThru</span></span>
<span data-ttu-id="cd59d-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="cd59d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd59d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd59d-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd59d-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="cd59d-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cd59d-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="cd59d-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd59d-132">-ServiceName</span></span>
<span data-ttu-id="cd59d-133">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cd59d-134">-SubscriptionId</span></span>
<span data-ttu-id="cd59d-135">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cd59d-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd59d-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cd59d-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd59d-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd59d-137">-Confirm</span></span>
<span data-ttu-id="cd59d-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd59d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd59d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd59d-139">-WhatIf</span></span>
<span data-ttu-id="cd59d-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd59d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd59d-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd59d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd59d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd59d-142">CommonParameters</span></span>
<span data-ttu-id="cd59d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd59d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd59d-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd59d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd59d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd59d-145">INPUTS</span></span>

### <span data-ttu-id="cd59d-146">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="cd59d-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cd59d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd59d-147">OUTPUTS</span></span>

### <span data-ttu-id="cd59d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd59d-148">System.Boolean</span></span>

## <span data-ttu-id="cd59d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd59d-149">NOTES</span></span>

<span data-ttu-id="cd59d-150">Aliase</span><span class="sxs-lookup"><span data-stu-id="cd59d-150">ALIASES</span></span>

<span data-ttu-id="cd59d-151">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd59d-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd59d-152">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd59d-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd59d-153">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="cd59d-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd59d-154">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="cd59d-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd59d-155">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cd59d-156">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cd59d-157">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cd59d-158">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cd59d-159">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cd59d-160">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="cd59d-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd59d-161">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="cd59d-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cd59d-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="cd59d-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cd59d-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="cd59d-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cd59d-164">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="cd59d-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cd59d-165">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cd59d-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cd59d-166">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cd59d-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd59d-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd59d-167">RELATED LINKS</span></span>

