---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145172"
---
# <span data-ttu-id="13023-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="13023-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="13023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13023-102">SYNOPSIS</span></span>
<span data-ttu-id="13023-103">Löschen Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="13023-103">Delete the transaction node.</span></span>

## <span data-ttu-id="13023-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13023-104">SYNTAX</span></span>

### <span data-ttu-id="13023-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="13023-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="13023-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13023-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13023-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13023-107">DESCRIPTION</span></span>
<span data-ttu-id="13023-108">Löschen Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="13023-108">Delete the transaction node.</span></span>

## <span data-ttu-id="13023-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13023-109">EXAMPLES</span></span>

### <span data-ttu-id="13023-110">Beispiel 1: Entfernen eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="13023-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="13023-111">Mit diesem Befehl wird ein Transaktionsknoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="13023-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="13023-112">Beispiel 2: Entfernen eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="13023-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="13023-113">Mit diesem Befehl wird ein Transaktionsknoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="13023-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="13023-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13023-114">PARAMETERS</span></span>

### <span data-ttu-id="13023-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13023-115">-AsJob</span></span>
<span data-ttu-id="13023-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="13023-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13023-117">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="13023-117">-BlockchainMemberName</span></span>
<span data-ttu-id="13023-118">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="13023-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="13023-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13023-119">-DefaultProfile</span></span>
<span data-ttu-id="13023-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13023-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13023-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13023-121">-InputObject</span></span>
<span data-ttu-id="13023-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="13023-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13023-123">-Name</span><span class="sxs-lookup"><span data-stu-id="13023-123">-Name</span></span>
<span data-ttu-id="13023-124">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="13023-124">Transaction node name.</span></span>

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

### <span data-ttu-id="13023-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13023-125">-NoWait</span></span>
<span data-ttu-id="13023-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="13023-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13023-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13023-127">-PassThru</span></span>
<span data-ttu-id="13023-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="13023-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="13023-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13023-129">-ResourceGroupName</span></span>
<span data-ttu-id="13023-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="13023-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="13023-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="13023-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="13023-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13023-132">-SubscriptionId</span></span>
<span data-ttu-id="13023-133">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="13023-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="13023-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="13023-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="13023-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13023-135">-Confirm</span></span>
<span data-ttu-id="13023-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13023-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13023-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="13023-137">-WhatIf</span></span>
<span data-ttu-id="13023-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13023-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13023-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13023-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13023-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13023-140">CommonParameters</span></span>
<span data-ttu-id="13023-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13023-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13023-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13023-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13023-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13023-143">INPUTS</span></span>

### <span data-ttu-id="13023-144">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="13023-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="13023-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13023-145">OUTPUTS</span></span>

### <span data-ttu-id="13023-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13023-146">System.Boolean</span></span>

## <span data-ttu-id="13023-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13023-147">NOTES</span></span>

<span data-ttu-id="13023-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="13023-148">ALIASES</span></span>

<span data-ttu-id="13023-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="13023-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13023-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13023-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13023-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13023-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13023-152">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="13023-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13023-153">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="13023-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="13023-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="13023-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13023-155">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="13023-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="13023-156">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="13023-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="13023-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="13023-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="13023-158">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="13023-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="13023-159">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="13023-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="13023-160">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="13023-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="13023-161">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="13023-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="13023-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13023-162">RELATED LINKS</span></span>

