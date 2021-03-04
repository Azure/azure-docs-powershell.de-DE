---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949224"
---
# <span data-ttu-id="1814a-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="1814a-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="1814a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1814a-102">SYNOPSIS</span></span>
<span data-ttu-id="1814a-103">Löschen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="1814a-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="1814a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1814a-104">SYNTAX</span></span>

### <span data-ttu-id="1814a-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="1814a-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1814a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1814a-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1814a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1814a-107">DESCRIPTION</span></span>
<span data-ttu-id="1814a-108">Löschen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="1814a-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="1814a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1814a-109">EXAMPLES</span></span>

### <span data-ttu-id="1814a-110">Beispiel 1: Löschen von HealthBot nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="1814a-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="1814a-111">Löschen von HealthBot nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="1814a-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="1814a-112">Beispiel 2: Löschen von HealthBot nach InputObject</span><span class="sxs-lookup"><span data-stu-id="1814a-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="1814a-113">Delete HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="1814a-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="1814a-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1814a-114">PARAMETERS</span></span>

### <span data-ttu-id="1814a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1814a-115">-AsJob</span></span>
<span data-ttu-id="1814a-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1814a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1814a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1814a-117">-DefaultProfile</span></span>
<span data-ttu-id="1814a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1814a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1814a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1814a-119">-InputObject</span></span>
<span data-ttu-id="1814a-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1814a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1814a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1814a-121">-Name</span></span>
<span data-ttu-id="1814a-122">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1814a-122">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1814a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1814a-123">-NoWait</span></span>
<span data-ttu-id="1814a-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1814a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1814a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1814a-125">-PassThru</span></span>
<span data-ttu-id="1814a-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1814a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1814a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1814a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1814a-128">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="1814a-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="1814a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1814a-129">-SubscriptionId</span></span>
<span data-ttu-id="1814a-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1814a-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1814a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1814a-131">-Confirm</span></span>
<span data-ttu-id="1814a-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1814a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1814a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1814a-133">-WhatIf</span></span>
<span data-ttu-id="1814a-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1814a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1814a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1814a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1814a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1814a-136">CommonParameters</span></span>
<span data-ttu-id="1814a-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1814a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1814a-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1814a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1814a-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1814a-139">INPUTS</span></span>

### <span data-ttu-id="1814a-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="1814a-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="1814a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1814a-141">OUTPUTS</span></span>

### <span data-ttu-id="1814a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1814a-142">System.Boolean</span></span>

## <span data-ttu-id="1814a-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1814a-143">NOTES</span></span>

<span data-ttu-id="1814a-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1814a-144">ALIASES</span></span>

<span data-ttu-id="1814a-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1814a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1814a-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1814a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1814a-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1814a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1814a-148">INPUTOBJECT <IHealthBotIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1814a-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1814a-149">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1814a-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="1814a-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1814a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1814a-151">`[ResourceGroupName <String>]`: Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="1814a-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="1814a-152">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1814a-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1814a-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1814a-153">RELATED LINKS</span></span>

