---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365404"
---
# <span data-ttu-id="577d1-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="577d1-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="577d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577d1-102">SYNOPSIS</span></span>
<span data-ttu-id="577d1-103">Löschen Sie ein unzingees Mitglied.</span><span class="sxs-lookup"><span data-stu-id="577d1-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="577d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="577d1-104">SYNTAX</span></span>

### <span data-ttu-id="577d1-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="577d1-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="577d1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="577d1-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="577d1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="577d1-107">DESCRIPTION</span></span>
<span data-ttu-id="577d1-108">Löschen Sie ein unzingees Mitglied.</span><span class="sxs-lookup"><span data-stu-id="577d1-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="577d1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="577d1-109">EXAMPLES</span></span>

### <span data-ttu-id="577d1-110">Beispiel 1: Entfernen eines Mitglieds</span><span class="sxs-lookup"><span data-stu-id="577d1-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="577d1-111">Mit diesem Befehl wird ein Member aus "member" entfernt.</span><span class="sxs-lookup"><span data-stu-id="577d1-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="577d1-112">Beispiel 2: Entfernen eines Mitglieds</span><span class="sxs-lookup"><span data-stu-id="577d1-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="577d1-113">Mit diesem Befehl wird ein Member aus "member" entfernt.</span><span class="sxs-lookup"><span data-stu-id="577d1-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="577d1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577d1-114">PARAMETERS</span></span>

### <span data-ttu-id="577d1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="577d1-115">-AsJob</span></span>
<span data-ttu-id="577d1-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="577d1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="577d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577d1-117">-DefaultProfile</span></span>
<span data-ttu-id="577d1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="577d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="577d1-119">-InputObject</span></span>
<span data-ttu-id="577d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="577d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="577d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="577d1-121">-Name</span></span>
<span data-ttu-id="577d1-122">Name des Mitgliedes</span><span class="sxs-lookup"><span data-stu-id="577d1-122">Blockchain member name</span></span>

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

### <span data-ttu-id="577d1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="577d1-123">-NoWait</span></span>
<span data-ttu-id="577d1-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="577d1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="577d1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="577d1-125">-PassThru</span></span>
<span data-ttu-id="577d1-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="577d1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="577d1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577d1-127">-ResourceGroupName</span></span>
<span data-ttu-id="577d1-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="577d1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="577d1-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="577d1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="577d1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="577d1-130">-SubscriptionId</span></span>
<span data-ttu-id="577d1-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="577d1-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="577d1-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="577d1-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="577d1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577d1-133">-Confirm</span></span>
<span data-ttu-id="577d1-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="577d1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577d1-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="577d1-135">-WhatIf</span></span>
<span data-ttu-id="577d1-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="577d1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577d1-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="577d1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577d1-138">CommonParameters</span></span>
<span data-ttu-id="577d1-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577d1-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="577d1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577d1-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="577d1-141">INPUTS</span></span>

### <span data-ttu-id="577d1-142">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="577d1-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="577d1-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="577d1-143">OUTPUTS</span></span>

### <span data-ttu-id="577d1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="577d1-144">System.Boolean</span></span>

## <span data-ttu-id="577d1-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="577d1-145">NOTES</span></span>

<span data-ttu-id="577d1-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="577d1-146">ALIASES</span></span>

<span data-ttu-id="577d1-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="577d1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="577d1-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="577d1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="577d1-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="577d1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="577d1-150">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="577d1-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="577d1-151">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="577d1-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="577d1-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="577d1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="577d1-153">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="577d1-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="577d1-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="577d1-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="577d1-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="577d1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="577d1-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="577d1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="577d1-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="577d1-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="577d1-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="577d1-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="577d1-159">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="577d1-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="577d1-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="577d1-160">RELATED LINKS</span></span>

