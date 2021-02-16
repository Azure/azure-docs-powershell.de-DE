---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171420"
---
# <span data-ttu-id="4aba9-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="4aba9-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="4aba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aba9-102">SYNOPSIS</span></span>
<span data-ttu-id="4aba9-103">Löschen Sie ein geeste Mitglied.</span><span class="sxs-lookup"><span data-stu-id="4aba9-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="4aba9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aba9-104">SYNTAX</span></span>

### <span data-ttu-id="4aba9-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aba9-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4aba9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4aba9-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4aba9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aba9-107">DESCRIPTION</span></span>
<span data-ttu-id="4aba9-108">Löschen Sie ein geeste Mitglied.</span><span class="sxs-lookup"><span data-stu-id="4aba9-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="4aba9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aba9-109">EXAMPLES</span></span>

### <span data-ttu-id="4aba9-110">Beispiel 1: Entfernen eines Mitglieds</span><span class="sxs-lookup"><span data-stu-id="4aba9-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="4aba9-111">Mit diesem Befehl wird ein Mitglied aus "member" entfernt.</span><span class="sxs-lookup"><span data-stu-id="4aba9-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="4aba9-112">Beispiel 2: Entfernen eines Mitglieds</span><span class="sxs-lookup"><span data-stu-id="4aba9-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="4aba9-113">Mit diesem Befehl wird ein Mitglied aus "member" entfernt.</span><span class="sxs-lookup"><span data-stu-id="4aba9-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="4aba9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aba9-114">PARAMETERS</span></span>

### <span data-ttu-id="4aba9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aba9-115">-AsJob</span></span>
<span data-ttu-id="4aba9-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4aba9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4aba9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aba9-117">-DefaultProfile</span></span>
<span data-ttu-id="4aba9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aba9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aba9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aba9-119">-InputObject</span></span>
<span data-ttu-id="4aba9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4aba9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aba9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4aba9-121">-Name</span></span>
<span data-ttu-id="4aba9-122">Name des Mitgliedes</span><span class="sxs-lookup"><span data-stu-id="4aba9-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aba9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4aba9-123">-NoWait</span></span>
<span data-ttu-id="4aba9-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4aba9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4aba9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aba9-125">-PassThru</span></span>
<span data-ttu-id="4aba9-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4aba9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4aba9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aba9-127">-ResourceGroupName</span></span>
<span data-ttu-id="4aba9-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="4aba9-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4aba9-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="4aba9-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4aba9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aba9-130">-SubscriptionId</span></span>
<span data-ttu-id="4aba9-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4aba9-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4aba9-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4aba9-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4aba9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aba9-133">-Confirm</span></span>
<span data-ttu-id="4aba9-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aba9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aba9-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4aba9-135">-WhatIf</span></span>
<span data-ttu-id="4aba9-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aba9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aba9-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aba9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aba9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aba9-138">CommonParameters</span></span>
<span data-ttu-id="4aba9-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aba9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aba9-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aba9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aba9-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aba9-141">INPUTS</span></span>

### <span data-ttu-id="4aba9-142">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="4aba9-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="4aba9-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aba9-143">OUTPUTS</span></span>

### <span data-ttu-id="4aba9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4aba9-144">System.Boolean</span></span>

## <span data-ttu-id="4aba9-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aba9-145">NOTES</span></span>

<span data-ttu-id="4aba9-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4aba9-146">ALIASES</span></span>

<span data-ttu-id="4aba9-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4aba9-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4aba9-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4aba9-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4aba9-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4aba9-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4aba9-150">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4aba9-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4aba9-151">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="4aba9-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="4aba9-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="4aba9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4aba9-153">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="4aba9-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="4aba9-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="4aba9-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="4aba9-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="4aba9-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4aba9-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="4aba9-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4aba9-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4aba9-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="4aba9-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4aba9-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="4aba9-159">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="4aba9-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="4aba9-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aba9-160">RELATED LINKS</span></span>

