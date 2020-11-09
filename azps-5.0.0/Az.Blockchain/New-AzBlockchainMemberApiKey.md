---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301582"
---
# <span data-ttu-id="0b025-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="0b025-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="0b025-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b025-102">SYNOPSIS</span></span>
<span data-ttu-id="0b025-103">Generieren Sie die API-Schlüssel für ein blockchain-Mitglied neu.</span><span class="sxs-lookup"><span data-stu-id="0b025-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="0b025-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b025-104">SYNTAX</span></span>

### <span data-ttu-id="0b025-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b025-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b025-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0b025-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b025-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b025-107">DESCRIPTION</span></span>
<span data-ttu-id="0b025-108">Generieren Sie die API-Schlüssel für ein blockchain-Mitglied neu.</span><span class="sxs-lookup"><span data-stu-id="0b025-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="0b025-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b025-109">EXAMPLES</span></span>

### <span data-ttu-id="0b025-110">Beispiel 1: Erneutes Generieren von API-Schlüsseln für ein blockchain-Element mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="0b025-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="0b025-111">Mit diesem Befehl werden API-Schlüssel für ein blockchain-Element mit Name, Ressourcengruppe neu generiert.</span><span class="sxs-lookup"><span data-stu-id="0b025-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="0b025-112">Beispiel 2: Erneutes Generieren von API-Schlüsseln für ein blockchain-Element mithilfe von idenity</span><span class="sxs-lookup"><span data-stu-id="0b025-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="0b025-113">Mit diesem Befehl werden API-Schlüssel für ein blockchain-Element mithilfe von Identity neu generiert.</span><span class="sxs-lookup"><span data-stu-id="0b025-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="0b025-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b025-114">PARAMETERS</span></span>

### <span data-ttu-id="0b025-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="0b025-115">-BlockchainMemberName</span></span>
<span data-ttu-id="0b025-116">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="0b025-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="0b025-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b025-117">-DefaultProfile</span></span>
<span data-ttu-id="0b025-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b025-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b025-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b025-119">-InputObject</span></span>
<span data-ttu-id="0b025-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0b025-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b025-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b025-121">-KeyName</span></span>
<span data-ttu-id="0b025-122">Ruft den Namen des API-Schlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="0b025-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="0b025-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b025-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b025-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="0b025-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0b025-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="0b025-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0b025-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0b025-126">-SubscriptionId</span></span>
<span data-ttu-id="0b025-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0b025-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b025-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="0b025-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0b025-129">-Wert</span><span class="sxs-lookup"><span data-stu-id="0b025-129">-Value</span></span>
<span data-ttu-id="0b025-130">Ruft den API-Schlüsselwert ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="0b025-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="0b025-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b025-131">-Confirm</span></span>
<span data-ttu-id="0b025-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b025-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b025-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b025-133">-WhatIf</span></span>
<span data-ttu-id="0b025-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b025-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b025-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b025-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b025-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b025-136">CommonParameters</span></span>
<span data-ttu-id="0b025-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b025-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b025-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b025-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b025-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b025-139">INPUTS</span></span>

### <span data-ttu-id="0b025-140">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="0b025-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="0b025-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b025-141">OUTPUTS</span></span>

### <span data-ttu-id="0b025-142">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="0b025-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="0b025-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b025-143">NOTES</span></span>

<span data-ttu-id="0b025-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="0b025-144">ALIASES</span></span>

<span data-ttu-id="0b025-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b025-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b025-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0b025-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b025-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0b025-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b025-148">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0b025-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b025-149">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="0b025-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="0b025-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0b025-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b025-151">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="0b025-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="0b025-152">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="0b025-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="0b025-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="0b025-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0b025-154">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="0b025-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0b025-155">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0b025-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0b025-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="0b025-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="0b025-157">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="0b025-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="0b025-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b025-158">RELATED LINKS</span></span>

