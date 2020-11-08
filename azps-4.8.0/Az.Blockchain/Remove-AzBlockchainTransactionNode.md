---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009363"
---
# <span data-ttu-id="deb44-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="deb44-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="deb44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="deb44-102">SYNOPSIS</span></span>
<span data-ttu-id="deb44-103">Löschen des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="deb44-103">Delete the transaction node.</span></span>

## <span data-ttu-id="deb44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="deb44-104">SYNTAX</span></span>

### <span data-ttu-id="deb44-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="deb44-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="deb44-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="deb44-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="deb44-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="deb44-107">DESCRIPTION</span></span>
<span data-ttu-id="deb44-108">Löschen des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="deb44-108">Delete the transaction node.</span></span>

## <span data-ttu-id="deb44-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="deb44-109">EXAMPLES</span></span>

### <span data-ttu-id="deb44-110">Beispiel 1: Entfernen eines Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="deb44-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="deb44-111">Dieser Befehl entfernt einen Transaktions Knoten.</span><span class="sxs-lookup"><span data-stu-id="deb44-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="deb44-112">Beispiel 2: Entfernen eines Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="deb44-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="deb44-113">Dieser Befehl entfernt einen Transaktions Knoten.</span><span class="sxs-lookup"><span data-stu-id="deb44-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="deb44-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb44-114">PARAMETERS</span></span>

### <span data-ttu-id="deb44-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deb44-115">-AsJob</span></span>
<span data-ttu-id="deb44-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="deb44-116">Run the command as a job</span></span>

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

### <span data-ttu-id="deb44-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="deb44-117">-BlockchainMemberName</span></span>
<span data-ttu-id="deb44-118">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="deb44-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="deb44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb44-119">-DefaultProfile</span></span>
<span data-ttu-id="deb44-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="deb44-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb44-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="deb44-121">-InputObject</span></span>
<span data-ttu-id="deb44-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="deb44-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="deb44-123">-Name</span><span class="sxs-lookup"><span data-stu-id="deb44-123">-Name</span></span>
<span data-ttu-id="deb44-124">Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="deb44-124">Transaction node name.</span></span>

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

### <span data-ttu-id="deb44-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="deb44-125">-NoWait</span></span>
<span data-ttu-id="deb44-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="deb44-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="deb44-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="deb44-127">-PassThru</span></span>
<span data-ttu-id="deb44-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="deb44-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="deb44-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb44-129">-ResourceGroupName</span></span>
<span data-ttu-id="deb44-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="deb44-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="deb44-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="deb44-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="deb44-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="deb44-132">-SubscriptionId</span></span>
<span data-ttu-id="deb44-133">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="deb44-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="deb44-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="deb44-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="deb44-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="deb44-135">-Confirm</span></span>
<span data-ttu-id="deb44-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="deb44-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb44-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb44-137">-WhatIf</span></span>
<span data-ttu-id="deb44-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="deb44-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb44-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deb44-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb44-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb44-140">CommonParameters</span></span>
<span data-ttu-id="deb44-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb44-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb44-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb44-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb44-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="deb44-143">INPUTS</span></span>

### <span data-ttu-id="deb44-144">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="deb44-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="deb44-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="deb44-145">OUTPUTS</span></span>

### <span data-ttu-id="deb44-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="deb44-146">System.Boolean</span></span>

## <span data-ttu-id="deb44-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="deb44-147">NOTES</span></span>

<span data-ttu-id="deb44-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="deb44-148">ALIASES</span></span>

<span data-ttu-id="deb44-149">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="deb44-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="deb44-150">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="deb44-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="deb44-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="deb44-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="deb44-152">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="deb44-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="deb44-153">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="deb44-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="deb44-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="deb44-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="deb44-155">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="deb44-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="deb44-156">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="deb44-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="deb44-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="deb44-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="deb44-158">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="deb44-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="deb44-159">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="deb44-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="deb44-160">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="deb44-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="deb44-161">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="deb44-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="deb44-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="deb44-162">RELATED LINKS</span></span>

