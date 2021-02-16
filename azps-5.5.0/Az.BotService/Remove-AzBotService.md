---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162425"
---
# <span data-ttu-id="cb569-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="cb569-101">Remove-AzBotService</span></span>

## <span data-ttu-id="cb569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb569-102">SYNOPSIS</span></span>
<span data-ttu-id="cb569-103">Löscht einen Botdienst aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb569-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="cb569-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb569-104">SYNTAX</span></span>

### <span data-ttu-id="cb569-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb569-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb569-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb569-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb569-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb569-107">DESCRIPTION</span></span>
<span data-ttu-id="cb569-108">Löscht einen Botdienst aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb569-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="cb569-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb569-109">EXAMPLES</span></span>

### <span data-ttu-id="cb569-110">Beispiel 1: Löschen von BotService nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb569-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="cb569-111">Löschen von BotService nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb569-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="cb569-112">Beispiel 2: Löschen des BotService von InputObject</span><span class="sxs-lookup"><span data-stu-id="cb569-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="cb569-113">Löschen des BotService von InputObject</span><span class="sxs-lookup"><span data-stu-id="cb569-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="cb569-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb569-114">PARAMETERS</span></span>

### <span data-ttu-id="cb569-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb569-115">-DefaultProfile</span></span>
<span data-ttu-id="cb569-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb569-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb569-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb569-117">-InputObject</span></span>
<span data-ttu-id="cb569-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cb569-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb569-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cb569-119">-Name</span></span>
<span data-ttu-id="cb569-120">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cb569-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="cb569-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb569-121">-PassThru</span></span>
<span data-ttu-id="cb569-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb569-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb569-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb569-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb569-124">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="cb569-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="cb569-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb569-125">-SubscriptionId</span></span>
<span data-ttu-id="cb569-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cb569-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cb569-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb569-127">-Confirm</span></span>
<span data-ttu-id="cb569-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb569-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb569-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cb569-129">-WhatIf</span></span>
<span data-ttu-id="cb569-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb569-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb569-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb569-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb569-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb569-132">CommonParameters</span></span>
<span data-ttu-id="cb569-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb569-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb569-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb569-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb569-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb569-135">INPUTS</span></span>

### <span data-ttu-id="cb569-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cb569-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="cb569-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb569-137">OUTPUTS</span></span>

### <span data-ttu-id="cb569-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb569-138">System.Boolean</span></span>

## <span data-ttu-id="cb569-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb569-139">NOTES</span></span>

<span data-ttu-id="cb569-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cb569-140">ALIASES</span></span>

<span data-ttu-id="cb569-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cb569-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb569-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb569-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb569-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb569-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb569-144">INPUTOBJECT <IBotServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cb569-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb569-145">`[ChannelName <ChannelName?>]`: Der Name der Kanalressource.</span><span class="sxs-lookup"><span data-stu-id="cb569-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="cb569-146">`[ConnectionName <String>]`: Der Name der Ressource "Bot Service Connection Setting"</span><span class="sxs-lookup"><span data-stu-id="cb569-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="cb569-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cb569-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb569-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="cb569-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="cb569-149">`[ResourceName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cb569-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="cb569-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cb569-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cb569-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb569-151">RELATED LINKS</span></span>

