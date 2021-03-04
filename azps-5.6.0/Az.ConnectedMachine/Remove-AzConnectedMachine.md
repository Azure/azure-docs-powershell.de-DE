---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: 72e7df2a9f543af6b3247e400d55ac0f9c14ce0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948803"
---
# <span data-ttu-id="41a32-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="41a32-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="41a32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41a32-102">SYNOPSIS</span></span>
<span data-ttu-id="41a32-103">Der Vorgang zum Entfernen einer Hybridcomputeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="41a32-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="41a32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41a32-104">SYNTAX</span></span>

### <span data-ttu-id="41a32-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="41a32-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41a32-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41a32-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41a32-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41a32-107">DESCRIPTION</span></span>
<span data-ttu-id="41a32-108">Der Vorgang zum Entfernen einer Hybridcomputeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="41a32-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="41a32-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41a32-109">EXAMPLES</span></span>

### <span data-ttu-id="41a32-110">Beispiel 1: Entfernen eines verbundenen Computers</span><span class="sxs-lookup"><span data-stu-id="41a32-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="41a32-111">Löscht den verbundenen Computer.</span><span class="sxs-lookup"><span data-stu-id="41a32-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="41a32-112">Beispiel 2: Entfernen verbundener Computer über die Pipeline</span><span class="sxs-lookup"><span data-stu-id="41a32-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="41a32-113">Entfernt alle Computer in der `contoso-connected-machines` Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41a32-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="41a32-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41a32-114">PARAMETERS</span></span>

### <span data-ttu-id="41a32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a32-115">-DefaultProfile</span></span>
<span data-ttu-id="41a32-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41a32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a32-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41a32-117">-InputObject</span></span>
<span data-ttu-id="41a32-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="41a32-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41a32-119">-Name</span><span class="sxs-lookup"><span data-stu-id="41a32-119">-Name</span></span>
<span data-ttu-id="41a32-120">Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="41a32-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="41a32-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41a32-121">-PassThru</span></span>
<span data-ttu-id="41a32-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41a32-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41a32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a32-123">-ResourceGroupName</span></span>
<span data-ttu-id="41a32-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41a32-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="41a32-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41a32-125">-SubscriptionId</span></span>
<span data-ttu-id="41a32-126">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="41a32-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41a32-127">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="41a32-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41a32-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41a32-128">-Confirm</span></span>
<span data-ttu-id="41a32-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41a32-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41a32-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a32-130">-WhatIf</span></span>
<span data-ttu-id="41a32-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41a32-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a32-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41a32-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41a32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a32-133">CommonParameters</span></span>
<span data-ttu-id="41a32-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a32-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41a32-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a32-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41a32-136">INPUTS</span></span>

### <span data-ttu-id="41a32-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="41a32-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="41a32-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41a32-138">OUTPUTS</span></span>

### <span data-ttu-id="41a32-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41a32-139">System.Boolean</span></span>

## <span data-ttu-id="41a32-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41a32-140">NOTES</span></span>

<span data-ttu-id="41a32-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="41a32-141">ALIASES</span></span>

<span data-ttu-id="41a32-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="41a32-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41a32-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="41a32-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41a32-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41a32-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41a32-145">INPUTOBJECT <IConnectedMachineIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="41a32-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41a32-146">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="41a32-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="41a32-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="41a32-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41a32-148">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="41a32-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="41a32-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41a32-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="41a32-150">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="41a32-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41a32-151">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="41a32-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41a32-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41a32-152">RELATED LINKS</span></span>

