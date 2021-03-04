---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948891"
---
# <span data-ttu-id="f8eb8-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="f8eb8-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="f8eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="f8eb8-103">Löschen der Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="f8eb8-103">Delete Organization resource</span></span>

## <span data-ttu-id="f8eb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8eb8-104">SYNTAX</span></span>

### <span data-ttu-id="f8eb8-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8eb8-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8eb8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8eb8-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8eb8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="f8eb8-108">Löschen der Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="f8eb8-108">Delete Organization resource</span></span>

## <span data-ttu-id="f8eb8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8eb8-109">EXAMPLES</span></span>

### <span data-ttu-id="f8eb8-110">Beispiel 1: Entfernen einer kongenenten Organisation nach Name</span><span class="sxs-lookup"><span data-stu-id="f8eb8-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="f8eb8-111">Mit diesem Befehl wird eine konfluente Organisation nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="f8eb8-112">Beispiel 2: Entfernen einer kongenenten Organisation per Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8eb8-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="f8eb8-113">Mit diesem Befehl wird eine konfluente Organisation per Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="f8eb8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f8eb8-114">PARAMETERS</span></span>

### <span data-ttu-id="f8eb8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8eb8-115">-AsJob</span></span>
<span data-ttu-id="f8eb8-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f8eb8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f8eb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8eb8-117">-DefaultProfile</span></span>
<span data-ttu-id="f8eb8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8eb8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8eb8-119">-InputObject</span></span>
<span data-ttu-id="f8eb8-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8eb8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8eb8-121">-Name</span></span>
<span data-ttu-id="f8eb8-122">Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="f8eb8-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8eb8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8eb8-123">-NoWait</span></span>
<span data-ttu-id="f8eb8-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f8eb8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8eb8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8eb8-125">-PassThru</span></span>
<span data-ttu-id="f8eb8-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8eb8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8eb8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8eb8-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f8eb8-128">Resource group name</span></span>

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

### <span data-ttu-id="f8eb8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8eb8-129">-SubscriptionId</span></span>
<span data-ttu-id="f8eb8-130">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="f8eb8-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="f8eb8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8eb8-131">-Confirm</span></span>
<span data-ttu-id="f8eb8-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8eb8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8eb8-133">-WhatIf</span></span>
<span data-ttu-id="f8eb8-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8eb8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8eb8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8eb8-136">CommonParameters</span></span>
<span data-ttu-id="f8eb8-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8eb8-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8eb8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8eb8-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8eb8-139">INPUTS</span></span>

### <span data-ttu-id="f8eb8-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="f8eb8-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="f8eb8-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8eb8-141">OUTPUTS</span></span>

### <span data-ttu-id="f8eb8-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8eb8-142">System.Boolean</span></span>

## <span data-ttu-id="f8eb8-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f8eb8-143">NOTES</span></span>

<span data-ttu-id="f8eb8-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f8eb8-144">ALIASES</span></span>

<span data-ttu-id="f8eb8-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f8eb8-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8eb8-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8eb8-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8eb8-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8eb8-148">INPUTOBJECT <IConfluentIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f8eb8-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8eb8-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f8eb8-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8eb8-150">`[OrganizationName <String>]`: Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="f8eb8-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="f8eb8-151">`[ResourceGroupName <String>]`: Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f8eb8-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="f8eb8-152">`[SubscriptionId <String>]`: Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="f8eb8-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="f8eb8-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f8eb8-153">RELATED LINKS</span></span>

