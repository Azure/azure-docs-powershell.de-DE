---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8d1918599832f5740515dc6334192bf9b4cc54ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926179"
---
# <span data-ttu-id="a4891-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a4891-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="a4891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4891-102">SYNOPSIS</span></span>
<span data-ttu-id="a4891-103">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-103">Delete a private cloud</span></span>

## <span data-ttu-id="a4891-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4891-104">SYNTAX</span></span>

### <span data-ttu-id="a4891-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4891-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4891-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4891-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4891-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4891-107">DESCRIPTION</span></span>
<span data-ttu-id="a4891-108">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-108">Delete a private cloud</span></span>

## <span data-ttu-id="a4891-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4891-109">EXAMPLES</span></span>

### <span data-ttu-id="a4891-110">Beispiel 1: Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="a4891-111">Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-111">Delete private cloud</span></span>

## <span data-ttu-id="a4891-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4891-112">PARAMETERS</span></span>

### <span data-ttu-id="a4891-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4891-113">-AsJob</span></span>
<span data-ttu-id="a4891-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a4891-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a4891-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4891-115">-DefaultProfile</span></span>
<span data-ttu-id="a4891-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4891-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4891-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4891-117">-InputObject</span></span>
<span data-ttu-id="a4891-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a4891-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4891-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4891-119">-Name</span></span>
<span data-ttu-id="a4891-120">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="a4891-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a4891-121">-NoWait</span></span>
<span data-ttu-id="a4891-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a4891-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a4891-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4891-123">-PassThru</span></span>
<span data-ttu-id="a4891-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4891-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4891-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4891-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4891-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4891-126">The name of the resource group.</span></span>
<span data-ttu-id="a4891-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a4891-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4891-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4891-128">-SubscriptionId</span></span>
<span data-ttu-id="a4891-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a4891-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a4891-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4891-130">-Confirm</span></span>
<span data-ttu-id="a4891-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4891-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4891-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4891-132">-WhatIf</span></span>
<span data-ttu-id="a4891-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4891-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4891-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4891-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4891-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4891-135">CommonParameters</span></span>
<span data-ttu-id="a4891-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4891-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4891-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4891-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4891-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4891-138">INPUTS</span></span>

### <span data-ttu-id="a4891-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="a4891-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="a4891-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4891-140">OUTPUTS</span></span>

### <span data-ttu-id="a4891-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4891-141">System.Boolean</span></span>

## <span data-ttu-id="a4891-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4891-142">NOTES</span></span>

<span data-ttu-id="a4891-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a4891-143">ALIASES</span></span>

<span data-ttu-id="a4891-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a4891-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4891-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a4891-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4891-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4891-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4891-147">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a4891-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4891-148">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="a4891-149">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="a4891-150">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="a4891-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a4891-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4891-152">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="a4891-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="a4891-153">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a4891-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="a4891-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4891-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4891-155">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a4891-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4891-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a4891-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a4891-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4891-157">RELATED LINKS</span></span>

