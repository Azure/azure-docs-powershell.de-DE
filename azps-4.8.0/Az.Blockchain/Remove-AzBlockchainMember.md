---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009362"
---
# <span data-ttu-id="5e421-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="5e421-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="5e421-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e421-102">SYNOPSIS</span></span>
<span data-ttu-id="5e421-103">Löschen Sie ein blockchain-Mitglied.</span><span class="sxs-lookup"><span data-stu-id="5e421-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="5e421-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e421-104">SYNTAX</span></span>

### <span data-ttu-id="5e421-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e421-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e421-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e421-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e421-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e421-107">DESCRIPTION</span></span>
<span data-ttu-id="5e421-108">Löschen Sie ein blockchain-Mitglied.</span><span class="sxs-lookup"><span data-stu-id="5e421-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="5e421-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e421-109">EXAMPLES</span></span>

### <span data-ttu-id="5e421-110">Beispiel 1: Entfernen eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="5e421-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="5e421-111">Mit diesem Befehl wird ein blockchain-Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e421-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="5e421-112">Beispiel 2: Entfernen eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="5e421-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="5e421-113">Mit diesem Befehl wird ein blockchain-Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e421-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="5e421-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e421-114">PARAMETERS</span></span>

### <span data-ttu-id="5e421-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e421-115">-AsJob</span></span>
<span data-ttu-id="5e421-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5e421-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5e421-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e421-117">-DefaultProfile</span></span>
<span data-ttu-id="5e421-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e421-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e421-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e421-119">-InputObject</span></span>
<span data-ttu-id="5e421-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5e421-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e421-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e421-121">-Name</span></span>
<span data-ttu-id="5e421-122">Blockchain-Mitgliedsname</span><span class="sxs-lookup"><span data-stu-id="5e421-122">Blockchain member name</span></span>

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

### <span data-ttu-id="5e421-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e421-123">-NoWait</span></span>
<span data-ttu-id="5e421-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5e421-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e421-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e421-125">-PassThru</span></span>
<span data-ttu-id="5e421-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="5e421-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e421-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e421-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e421-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5e421-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5e421-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5e421-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5e421-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e421-130">-SubscriptionId</span></span>
<span data-ttu-id="5e421-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5e421-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e421-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5e421-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5e421-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e421-133">-Confirm</span></span>
<span data-ttu-id="5e421-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e421-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e421-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e421-135">-WhatIf</span></span>
<span data-ttu-id="5e421-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e421-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e421-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e421-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e421-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e421-138">CommonParameters</span></span>
<span data-ttu-id="5e421-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e421-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e421-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e421-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e421-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e421-141">INPUTS</span></span>

### <span data-ttu-id="5e421-142">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="5e421-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="5e421-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e421-143">OUTPUTS</span></span>

### <span data-ttu-id="5e421-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e421-144">System.Boolean</span></span>

## <span data-ttu-id="5e421-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e421-145">NOTES</span></span>

<span data-ttu-id="5e421-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="5e421-146">ALIASES</span></span>

<span data-ttu-id="5e421-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e421-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e421-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e421-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e421-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5e421-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e421-150">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5e421-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e421-151">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="5e421-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="5e421-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5e421-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e421-153">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="5e421-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="5e421-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="5e421-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="5e421-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5e421-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5e421-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5e421-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5e421-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5e421-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="5e421-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5e421-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="5e421-159">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="5e421-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="5e421-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e421-160">RELATED LINKS</span></span>

