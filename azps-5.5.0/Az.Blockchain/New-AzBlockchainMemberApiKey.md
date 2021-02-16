---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145185"
---
# <span data-ttu-id="d3bf3-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="d3bf3-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="d3bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="d3bf3-103">Generieren Sie die API-Schlüssel für ein Mitglied erneut.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d3bf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3bf3-104">SYNTAX</span></span>

### <span data-ttu-id="d3bf3-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3bf3-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3bf3-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d3bf3-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3bf3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="d3bf3-108">Generieren Sie die API-Schlüssel für ein Mitglied erneut.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d3bf3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="d3bf3-110">Beispiel 1: Neuer generieren von API-Schlüsseln für ein Mitglied unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="d3bf3-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d3bf3-111">Mit diesem Befehl werden die API-Schlüssel für ein Mitglied erneut generiert, indem der Name, die Ressourcengruppe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="d3bf3-112">Beispiel 2: Neuer generieren von API-Schlüsseln für ein Mitglied mit Idenity</span><span class="sxs-lookup"><span data-stu-id="d3bf3-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d3bf3-113">Mit diesem Befehl werden die API-Schlüssel für ein Mitglied einer Person mithilfe der Identität erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="d3bf3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3bf3-114">PARAMETERS</span></span>

### <span data-ttu-id="d3bf3-115">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="d3bf3-115">-BlockchainMemberName</span></span>
<span data-ttu-id="d3bf3-116">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3bf3-117">-DefaultProfile</span></span>
<span data-ttu-id="d3bf3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3bf3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3bf3-119">-InputObject</span></span>
<span data-ttu-id="d3bf3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d3bf3-121">-KeyName</span></span>
<span data-ttu-id="d3bf3-122">Ruft den Namen des API-Schlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3bf3-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3bf3-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d3bf3-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3bf3-126">-SubscriptionId</span></span>
<span data-ttu-id="d3bf3-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3bf3-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-129">-Value</span><span class="sxs-lookup"><span data-stu-id="d3bf3-129">-Value</span></span>
<span data-ttu-id="d3bf3-130">Ruft den Wert des API-Schlüssels ab oder legt den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-130">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bf3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3bf3-131">-Confirm</span></span>
<span data-ttu-id="d3bf3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3bf3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d3bf3-133">-WhatIf</span></span>
<span data-ttu-id="d3bf3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3bf3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3bf3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3bf3-136">CommonParameters</span></span>
<span data-ttu-id="d3bf3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3bf3-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3bf3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3bf3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3bf3-139">INPUTS</span></span>

### <span data-ttu-id="d3bf3-140">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d3bf3-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d3bf3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3bf3-141">OUTPUTS</span></span>

### <span data-ttu-id="d3bf3-142">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="d3bf3-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="d3bf3-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3bf3-143">NOTES</span></span>

<span data-ttu-id="d3bf3-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d3bf3-144">ALIASES</span></span>

<span data-ttu-id="d3bf3-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d3bf3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3bf3-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3bf3-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3bf3-148">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d3bf3-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3bf3-149">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d3bf3-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d3bf3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3bf3-151">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d3bf3-152">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d3bf3-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d3bf3-154">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d3bf3-155">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d3bf3-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d3bf3-157">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="d3bf3-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d3bf3-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3bf3-158">RELATED LINKS</span></span>

