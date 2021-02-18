---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 1a3125939e1640a6bd734ee8f75f36a4c34196ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173228"
---
# <span data-ttu-id="55b15-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="55b15-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="55b15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b15-102">SYNOPSIS</span></span>
<span data-ttu-id="55b15-103">Löschen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="55b15-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="55b15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55b15-104">SYNTAX</span></span>

### <span data-ttu-id="55b15-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="55b15-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55b15-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55b15-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55b15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55b15-107">DESCRIPTION</span></span>
<span data-ttu-id="55b15-108">Löschen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="55b15-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="55b15-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55b15-109">EXAMPLES</span></span>

### <span data-ttu-id="55b15-110">Beispiel 1: Löschen von HealthBot nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="55b15-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="55b15-111">Delete HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="55b15-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="55b15-112">Beispiel 2: Löschen von HealthBot von InputObject</span><span class="sxs-lookup"><span data-stu-id="55b15-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="55b15-113">Delete HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="55b15-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="55b15-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55b15-114">PARAMETERS</span></span>

### <span data-ttu-id="55b15-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b15-115">-AsJob</span></span>
<span data-ttu-id="55b15-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="55b15-116">Run the command as a job</span></span>

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

### <span data-ttu-id="55b15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b15-117">-DefaultProfile</span></span>
<span data-ttu-id="55b15-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55b15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b15-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55b15-119">-InputObject</span></span>
<span data-ttu-id="55b15-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="55b15-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55b15-121">-Name</span><span class="sxs-lookup"><span data-stu-id="55b15-121">-Name</span></span>
<span data-ttu-id="55b15-122">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="55b15-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="55b15-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55b15-123">-NoWait</span></span>
<span data-ttu-id="55b15-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="55b15-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55b15-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55b15-125">-PassThru</span></span>
<span data-ttu-id="55b15-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="55b15-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55b15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b15-127">-ResourceGroupName</span></span>
<span data-ttu-id="55b15-128">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="55b15-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="55b15-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55b15-129">-SubscriptionId</span></span>
<span data-ttu-id="55b15-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="55b15-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="55b15-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55b15-131">-Confirm</span></span>
<span data-ttu-id="55b15-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55b15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b15-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55b15-133">-WhatIf</span></span>
<span data-ttu-id="55b15-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55b15-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b15-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55b15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b15-136">CommonParameters</span></span>
<span data-ttu-id="55b15-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b15-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b15-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b15-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55b15-139">INPUTS</span></span>

### <span data-ttu-id="55b15-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="55b15-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="55b15-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55b15-141">OUTPUTS</span></span>

### <span data-ttu-id="55b15-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55b15-142">System.Boolean</span></span>

## <span data-ttu-id="55b15-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55b15-143">NOTES</span></span>

<span data-ttu-id="55b15-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="55b15-144">ALIASES</span></span>

<span data-ttu-id="55b15-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="55b15-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55b15-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55b15-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55b15-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55b15-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55b15-148">INPUTOBJECT <IHealthBotIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="55b15-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55b15-149">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="55b15-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="55b15-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="55b15-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55b15-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="55b15-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="55b15-152">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="55b15-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="55b15-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55b15-153">RELATED LINKS</span></span>

