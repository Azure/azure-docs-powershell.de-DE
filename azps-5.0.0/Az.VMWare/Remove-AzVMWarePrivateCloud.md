---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300724"
---
# <span data-ttu-id="ae425-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ae425-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="ae425-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae425-102">SYNOPSIS</span></span>
<span data-ttu-id="ae425-103">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-103">Delete a private cloud</span></span>

## <span data-ttu-id="ae425-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae425-104">SYNTAX</span></span>

### <span data-ttu-id="ae425-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae425-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae425-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ae425-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae425-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae425-107">DESCRIPTION</span></span>
<span data-ttu-id="ae425-108">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-108">Delete a private cloud</span></span>

## <span data-ttu-id="ae425-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae425-109">EXAMPLES</span></span>

### <span data-ttu-id="ae425-110">Beispiel 1: Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="ae425-111">Private Cloud löschen</span><span class="sxs-lookup"><span data-stu-id="ae425-111">Delete private cloud</span></span>

## <span data-ttu-id="ae425-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae425-112">PARAMETERS</span></span>

### <span data-ttu-id="ae425-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae425-113">-AsJob</span></span>
<span data-ttu-id="ae425-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ae425-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ae425-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae425-115">-DefaultProfile</span></span>
<span data-ttu-id="ae425-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae425-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae425-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ae425-117">-InputObject</span></span>
<span data-ttu-id="ae425-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ae425-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae425-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ae425-119">-Name</span></span>
<span data-ttu-id="ae425-120">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae425-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ae425-121">-NoWait</span></span>
<span data-ttu-id="ae425-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ae425-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae425-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae425-123">-PassThru</span></span>
<span data-ttu-id="ae425-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="ae425-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ae425-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae425-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae425-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae425-126">The name of the resource group.</span></span>
<span data-ttu-id="ae425-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ae425-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ae425-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ae425-128">-SubscriptionId</span></span>
<span data-ttu-id="ae425-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ae425-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ae425-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae425-130">-Confirm</span></span>
<span data-ttu-id="ae425-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae425-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae425-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae425-132">-WhatIf</span></span>
<span data-ttu-id="ae425-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae425-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae425-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae425-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae425-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae425-135">CommonParameters</span></span>
<span data-ttu-id="ae425-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae425-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae425-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae425-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae425-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae425-138">INPUTS</span></span>

### <span data-ttu-id="ae425-139">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ae425-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ae425-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae425-140">OUTPUTS</span></span>

### <span data-ttu-id="ae425-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae425-141">System.Boolean</span></span>

## <span data-ttu-id="ae425-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae425-142">NOTES</span></span>

<span data-ttu-id="ae425-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="ae425-143">ALIASES</span></span>

<span data-ttu-id="ae425-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae425-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae425-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae425-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae425-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ae425-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae425-147">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ae425-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae425-148">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ae425-149">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ae425-150">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ae425-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ae425-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae425-152">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="ae425-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ae425-153">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ae425-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ae425-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae425-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ae425-155">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ae425-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ae425-156">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ae425-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ae425-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae425-157">RELATED LINKS</span></span>

