---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: 486490a3b88025fb97b8790df202c944c05d888e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925152"
---
# <span data-ttu-id="74b12-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="74b12-101">Remove-AzBotService</span></span>

## <span data-ttu-id="74b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b12-102">SYNOPSIS</span></span>
<span data-ttu-id="74b12-103">Löscht einen Botdienst aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74b12-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="74b12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74b12-104">SYNTAX</span></span>

### <span data-ttu-id="74b12-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="74b12-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74b12-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74b12-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74b12-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74b12-107">DESCRIPTION</span></span>
<span data-ttu-id="74b12-108">Löscht einen Botdienst aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74b12-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="74b12-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74b12-109">EXAMPLES</span></span>

### <span data-ttu-id="74b12-110">Beispiel 1: Löschen des BotService nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b12-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="74b12-111">Löschen des BotService Nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b12-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="74b12-112">Beispiel 2: Löschen des BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="74b12-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="74b12-113">Löschen des BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="74b12-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="74b12-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="74b12-114">PARAMETERS</span></span>

### <span data-ttu-id="74b12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b12-115">-DefaultProfile</span></span>
<span data-ttu-id="74b12-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74b12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b12-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74b12-117">-InputObject</span></span>
<span data-ttu-id="74b12-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="74b12-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74b12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="74b12-119">-Name</span></span>
<span data-ttu-id="74b12-120">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="74b12-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="74b12-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74b12-121">-PassThru</span></span>
<span data-ttu-id="74b12-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74b12-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74b12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b12-123">-ResourceGroupName</span></span>
<span data-ttu-id="74b12-124">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="74b12-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="74b12-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74b12-125">-SubscriptionId</span></span>
<span data-ttu-id="74b12-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="74b12-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="74b12-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74b12-127">-Confirm</span></span>
<span data-ttu-id="74b12-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74b12-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b12-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b12-129">-WhatIf</span></span>
<span data-ttu-id="74b12-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74b12-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b12-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74b12-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b12-132">CommonParameters</span></span>
<span data-ttu-id="74b12-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b12-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74b12-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b12-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74b12-135">INPUTS</span></span>

### <span data-ttu-id="74b12-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="74b12-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="74b12-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74b12-137">OUTPUTS</span></span>

### <span data-ttu-id="74b12-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74b12-138">System.Boolean</span></span>

## <span data-ttu-id="74b12-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="74b12-139">NOTES</span></span>

<span data-ttu-id="74b12-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="74b12-140">ALIASES</span></span>

<span data-ttu-id="74b12-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="74b12-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74b12-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="74b12-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74b12-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74b12-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74b12-144">INPUTOBJECT <IBotServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="74b12-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74b12-145">`[ChannelName <ChannelName?>]`: Der Name der Kanalressource.</span><span class="sxs-lookup"><span data-stu-id="74b12-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="74b12-146">`[ConnectionName <String>]`: Der Name der Ressource "Bot Service Connection Setting"</span><span class="sxs-lookup"><span data-stu-id="74b12-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="74b12-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="74b12-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74b12-148">`[ResourceGroupName <String>]`: Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="74b12-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="74b12-149">`[ResourceName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="74b12-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="74b12-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="74b12-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="74b12-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="74b12-151">RELATED LINKS</span></span>

