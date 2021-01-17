---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458440"
---
# <span data-ttu-id="31f21-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="31f21-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="31f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f21-102">SYNOPSIS</span></span>
<span data-ttu-id="31f21-103">Löscht eine Firewallregel von einem SQL Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="31f21-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="31f21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31f21-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31f21-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31f21-105">DESCRIPTION</span></span>
<span data-ttu-id="31f21-106">Das **Cmdlet "Remove-AzSqlServerFirewallRule"** löscht eine Firewallregel vom angegebenen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="31f21-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="31f21-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31f21-107">EXAMPLES</span></span>

### <span data-ttu-id="31f21-108">Beispiel 1: Löschen einer Regel</span><span class="sxs-lookup"><span data-stu-id="31f21-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="31f21-109">Mit diesem Befehl wird eine Firewallregel mit dem Namen "Rule01" auf dem Server "Server01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="31f21-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="31f21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31f21-110">PARAMETERS</span></span>

### <span data-ttu-id="31f21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f21-111">-DefaultProfile</span></span>
<span data-ttu-id="31f21-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31f21-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="31f21-113">-FirewallRuleName</span></span>
<span data-ttu-id="31f21-114">Gibt den Namen der Firewallregel an, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="31f21-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-115">-Force</span><span class="sxs-lookup"><span data-stu-id="31f21-115">-Force</span></span>
<span data-ttu-id="31f21-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="31f21-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31f21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f21-117">-ResourceGroupName</span></span>
<span data-ttu-id="31f21-118">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="31f21-118">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31f21-119">-ServerName</span></span>
<span data-ttu-id="31f21-120">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="31f21-120">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31f21-121">-Confirm</span></span>
<span data-ttu-id="31f21-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31f21-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="31f21-123">-WhatIf</span></span>
<span data-ttu-id="31f21-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31f21-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f21-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31f21-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f21-126">CommonParameters</span></span>
<span data-ttu-id="31f21-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f21-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f21-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f21-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31f21-129">INPUTS</span></span>

### <span data-ttu-id="31f21-130">System.String</span><span class="sxs-lookup"><span data-stu-id="31f21-130">System.String</span></span>

## <span data-ttu-id="31f21-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31f21-131">OUTPUTS</span></span>

### <span data-ttu-id="31f21-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="31f21-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="31f21-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="31f21-133">NOTES</span></span>

## <span data-ttu-id="31f21-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="31f21-134">RELATED LINKS</span></span>

[<span data-ttu-id="31f21-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="31f21-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="31f21-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="31f21-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="31f21-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="31f21-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="31f21-138">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="31f21-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


