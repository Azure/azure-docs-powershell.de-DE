---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: fee3eb40bdab571df4f1f2c0aa384f341c70d637
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948584"
---
# <span data-ttu-id="1b3dd-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="1b3dd-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="1b3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3dd-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-103">Deletes a server.</span></span>

## <span data-ttu-id="1b3dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b3dd-104">SYNTAX</span></span>

### <span data-ttu-id="1b3dd-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b3dd-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b3dd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b3dd-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b3dd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="1b3dd-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-108">Deletes a server.</span></span>

## <span data-ttu-id="1b3dd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b3dd-109">EXAMPLES</span></span>

### <span data-ttu-id="1b3dd-110">Beispiel 1: Entfernen des MySql-Servers nach resourceGroup und Servername</span><span class="sxs-lookup"><span data-stu-id="1b3dd-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="1b3dd-111">Dieses Cmdlet entfernt den MySql-Server nach resourceGroup- und Servername.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="1b3dd-112">Beispiel 2: Entfernen des MySql-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="1b3dd-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="1b3dd-113">Diese Cmdlets entfernen den MySql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="1b3dd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b3dd-114">PARAMETERS</span></span>

### <span data-ttu-id="1b3dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b3dd-115">-AsJob</span></span>
<span data-ttu-id="1b3dd-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1b3dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1b3dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3dd-117">-DefaultProfile</span></span>
<span data-ttu-id="1b3dd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b3dd-119">-InputObject</span></span>
<span data-ttu-id="1b3dd-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3dd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1b3dd-121">-Name</span></span>
<span data-ttu-id="1b3dd-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3dd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b3dd-123">-NoWait</span></span>
<span data-ttu-id="1b3dd-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1b3dd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b3dd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b3dd-125">-PassThru</span></span>
<span data-ttu-id="1b3dd-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1b3dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b3dd-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-128">The name of the resource group.</span></span>
<span data-ttu-id="1b3dd-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1b3dd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b3dd-130">-SubscriptionId</span></span>
<span data-ttu-id="1b3dd-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1b3dd-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b3dd-132">-Confirm</span></span>
<span data-ttu-id="1b3dd-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b3dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b3dd-134">-WhatIf</span></span>
<span data-ttu-id="1b3dd-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b3dd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b3dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3dd-137">CommonParameters</span></span>
<span data-ttu-id="1b3dd-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3dd-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b3dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3dd-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b3dd-140">INPUTS</span></span>

### <span data-ttu-id="1b3dd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1b3dd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="1b3dd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b3dd-142">OUTPUTS</span></span>

### <span data-ttu-id="1b3dd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b3dd-143">System.Boolean</span></span>

## <span data-ttu-id="1b3dd-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b3dd-144">NOTES</span></span>

<span data-ttu-id="1b3dd-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1b3dd-145">ALIASES</span></span>

<span data-ttu-id="1b3dd-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1b3dd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b3dd-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b3dd-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b3dd-149">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1b3dd-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b3dd-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1b3dd-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1b3dd-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1b3dd-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1b3dd-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b3dd-154">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="1b3dd-155">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1b3dd-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1b3dd-157">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="1b3dd-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1b3dd-159">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1b3dd-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1b3dd-161">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1b3dd-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1b3dd-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b3dd-162">RELATED LINKS</span></span>

