---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003384"
---
# <span data-ttu-id="99373-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99373-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="99373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99373-102">SYNOPSIS</span></span>
<span data-ttu-id="99373-103">Löscht eine Firewall-Regel von einem SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="99373-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="99373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99373-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99373-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99373-105">DESCRIPTION</span></span>
<span data-ttu-id="99373-106">Mit dem Cmdlet **Remove-AzSqlServerFirewallRule** wird eine Firewallregel aus dem angegebenen Azure SQL-Datenbankserver gelöscht.</span><span class="sxs-lookup"><span data-stu-id="99373-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="99373-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99373-107">EXAMPLES</span></span>

### <span data-ttu-id="99373-108">Beispiel 1: Löschen einer Regel</span><span class="sxs-lookup"><span data-stu-id="99373-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="99373-109">Mit diesem Befehl wird eine Firewallregel namens Rule01 auf dem Server mit dem Namen "Server01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="99373-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="99373-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99373-110">PARAMETERS</span></span>

### <span data-ttu-id="99373-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99373-111">-DefaultProfile</span></span>
<span data-ttu-id="99373-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="99373-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99373-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="99373-113">-FirewallRuleName</span></span>
<span data-ttu-id="99373-114">Gibt den Namen der Firewall-Regel an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="99373-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="99373-115">-Force</span><span class="sxs-lookup"><span data-stu-id="99373-115">-Force</span></span>
<span data-ttu-id="99373-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="99373-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99373-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99373-117">-ResourceGroupName</span></span>
<span data-ttu-id="99373-118">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="99373-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="99373-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="99373-119">-ServerName</span></span>
<span data-ttu-id="99373-120">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="99373-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="99373-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99373-121">-Confirm</span></span>
<span data-ttu-id="99373-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99373-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99373-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99373-123">-WhatIf</span></span>
<span data-ttu-id="99373-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99373-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99373-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99373-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99373-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99373-126">CommonParameters</span></span>
<span data-ttu-id="99373-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99373-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99373-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99373-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99373-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99373-129">INPUTS</span></span>

### <span data-ttu-id="99373-130">System. String</span><span class="sxs-lookup"><span data-stu-id="99373-130">System.String</span></span>

## <span data-ttu-id="99373-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99373-131">OUTPUTS</span></span>

### <span data-ttu-id="99373-132">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="99373-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="99373-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="99373-133">NOTES</span></span>

## <span data-ttu-id="99373-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99373-134">RELATED LINKS</span></span>

[<span data-ttu-id="99373-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99373-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="99373-136">Neu – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99373-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="99373-137">Satz-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99373-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="99373-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="99373-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


