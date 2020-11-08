---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174134"
---
# <span data-ttu-id="c28d4-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="c28d4-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="c28d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c28d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c28d4-103">Vorgang zum Löschen einer App.</span><span class="sxs-lookup"><span data-stu-id="c28d4-103">Operation to delete an App.</span></span>

## <span data-ttu-id="c28d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c28d4-104">SYNTAX</span></span>

### <span data-ttu-id="c28d4-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c28d4-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c28d4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c28d4-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c28d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c28d4-107">DESCRIPTION</span></span>
<span data-ttu-id="c28d4-108">Vorgang zum Löschen einer App.</span><span class="sxs-lookup"><span data-stu-id="c28d4-108">Operation to delete an App.</span></span>

## <span data-ttu-id="c28d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c28d4-109">EXAMPLES</span></span>

### <span data-ttu-id="c28d4-110">Beispiel 1: Entfernen Sie die APP für die Frühlings Wolke nach dem Namen.</span><span class="sxs-lookup"><span data-stu-id="c28d4-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="c28d4-111">Entfernen Sie die APP für die Frühlings Wolke nach Namen.</span><span class="sxs-lookup"><span data-stu-id="c28d4-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="c28d4-112">Beispiel 2: Entfernen Sie die APP für die Frühlings Wolke aus Pipe.</span><span class="sxs-lookup"><span data-stu-id="c28d4-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="c28d4-113">Entfernen Sie die Frühlings Wolke-App aus Pipe.</span><span class="sxs-lookup"><span data-stu-id="c28d4-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="c28d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c28d4-114">PARAMETERS</span></span>

### <span data-ttu-id="c28d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28d4-115">-DefaultProfile</span></span>
<span data-ttu-id="c28d4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c28d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28d4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c28d4-117">-InputObject</span></span>
<span data-ttu-id="c28d4-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c28d4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c28d4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c28d4-119">-Name</span></span>
<span data-ttu-id="c28d4-120">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="c28d4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c28d4-121">-PassThru</span></span>
<span data-ttu-id="c28d4-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="c28d4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c28d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c28d4-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c28d4-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c28d4-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c28d4-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c28d4-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c28d4-126">-ServiceName</span></span>
<span data-ttu-id="c28d4-127">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c28d4-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c28d4-128">-SubscriptionId</span></span>
<span data-ttu-id="c28d4-129">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c28d4-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c28d4-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c28d4-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c28d4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c28d4-131">-Confirm</span></span>
<span data-ttu-id="c28d4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c28d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28d4-133">-WhatIf</span></span>
<span data-ttu-id="c28d4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c28d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28d4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c28d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28d4-136">CommonParameters</span></span>
<span data-ttu-id="c28d4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28d4-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c28d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28d4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c28d4-139">INPUTS</span></span>

### <span data-ttu-id="c28d4-140">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="c28d4-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c28d4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c28d4-141">OUTPUTS</span></span>

### <span data-ttu-id="c28d4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c28d4-142">System.Boolean</span></span>

## <span data-ttu-id="c28d4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c28d4-143">NOTES</span></span>

<span data-ttu-id="c28d4-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="c28d4-144">ALIASES</span></span>

<span data-ttu-id="c28d4-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c28d4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c28d4-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c28d4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c28d4-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c28d4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c28d4-148">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c28d4-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c28d4-149">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c28d4-150">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c28d4-151">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c28d4-152">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c28d4-153">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c28d4-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c28d4-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c28d4-155">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="c28d4-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c28d4-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c28d4-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c28d4-157">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c28d4-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c28d4-158">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="c28d4-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c28d4-159">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c28d4-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c28d4-160">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c28d4-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c28d4-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c28d4-161">RELATED LINKS</span></span>

