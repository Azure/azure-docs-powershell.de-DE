---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471054"
---
# <span data-ttu-id="27476-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="27476-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="27476-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27476-102">SYNOPSIS</span></span>
<span data-ttu-id="27476-103">Löschen Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="27476-103">Delete the transaction node.</span></span>

## <span data-ttu-id="27476-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27476-104">SYNTAX</span></span>

### <span data-ttu-id="27476-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="27476-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="27476-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27476-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27476-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27476-107">DESCRIPTION</span></span>
<span data-ttu-id="27476-108">Löschen Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="27476-108">Delete the transaction node.</span></span>

## <span data-ttu-id="27476-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27476-109">EXAMPLES</span></span>

### <span data-ttu-id="27476-110">Beispiel 1: Entfernen eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="27476-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="27476-111">Mit diesem Befehl wird ein Transaktionsknoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="27476-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="27476-112">Beispiel 2: Entfernen eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="27476-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="27476-113">Mit diesem Befehl wird ein Transaktionsknoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="27476-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="27476-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27476-114">PARAMETERS</span></span>

### <span data-ttu-id="27476-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27476-115">-AsJob</span></span>
<span data-ttu-id="27476-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="27476-116">Run the command as a job</span></span>

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

### <span data-ttu-id="27476-117">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="27476-117">-BlockchainMemberName</span></span>
<span data-ttu-id="27476-118">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="27476-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="27476-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27476-119">-DefaultProfile</span></span>
<span data-ttu-id="27476-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27476-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27476-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27476-121">-InputObject</span></span>
<span data-ttu-id="27476-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="27476-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27476-123">-Name</span><span class="sxs-lookup"><span data-stu-id="27476-123">-Name</span></span>
<span data-ttu-id="27476-124">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="27476-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27476-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="27476-125">-NoWait</span></span>
<span data-ttu-id="27476-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="27476-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27476-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27476-127">-PassThru</span></span>
<span data-ttu-id="27476-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="27476-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="27476-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27476-129">-ResourceGroupName</span></span>
<span data-ttu-id="27476-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="27476-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="27476-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="27476-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="27476-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27476-132">-SubscriptionId</span></span>
<span data-ttu-id="27476-133">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27476-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="27476-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="27476-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27476-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27476-135">-Confirm</span></span>
<span data-ttu-id="27476-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27476-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27476-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27476-137">-WhatIf</span></span>
<span data-ttu-id="27476-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27476-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27476-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27476-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27476-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27476-140">CommonParameters</span></span>
<span data-ttu-id="27476-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27476-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27476-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27476-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27476-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27476-143">INPUTS</span></span>

### <span data-ttu-id="27476-144">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="27476-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="27476-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27476-145">OUTPUTS</span></span>

### <span data-ttu-id="27476-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27476-146">System.Boolean</span></span>

## <span data-ttu-id="27476-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27476-147">NOTES</span></span>

<span data-ttu-id="27476-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="27476-148">ALIASES</span></span>

<span data-ttu-id="27476-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="27476-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27476-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27476-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27476-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27476-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27476-152">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="27476-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27476-153">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="27476-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="27476-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="27476-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27476-155">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="27476-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="27476-156">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="27476-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="27476-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="27476-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="27476-158">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="27476-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="27476-159">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27476-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="27476-160">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="27476-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="27476-161">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="27476-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="27476-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27476-162">RELATED LINKS</span></span>

