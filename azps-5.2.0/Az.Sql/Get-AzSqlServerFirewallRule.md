---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304483"
---
# <span data-ttu-id="5b596-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b596-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5b596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b596-102">SYNOPSIS</span></span>
<span data-ttu-id="5b596-103">Ruft Firewallregeln für einen SQL Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="5b596-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="5b596-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b596-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b596-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b596-105">DESCRIPTION</span></span>
<span data-ttu-id="5b596-106">Das **Cmdlet "Get-AzSqlServerFirewallRule"** ruft Firewallregeln für einen Azure SQL Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="5b596-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="5b596-107">Wenn Sie den Namen einer Firewallregel angeben, ruft dieses Cmdlet Informationen zu dieser bestimmten Firewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="5b596-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="5b596-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b596-108">EXAMPLES</span></span>

### <span data-ttu-id="5b596-109">Beispiel 1: Alle Regeln für einen Server erhalten</span><span class="sxs-lookup"><span data-stu-id="5b596-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="5b596-110">Dieser Befehl ruft alle Firewallregeln für den Server mit dem Namen Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="5b596-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="5b596-111">Beispiel 2: Erhalten aller Regeln für einen Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="5b596-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="5b596-112">Dieser Befehl ruft alle Firewallregeln für den Server namens Server01 ab, die mit "Regel" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5b596-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="5b596-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b596-113">PARAMETERS</span></span>

### <span data-ttu-id="5b596-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b596-114">-DefaultProfile</span></span>
<span data-ttu-id="5b596-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5b596-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b596-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5b596-116">-FirewallRuleName</span></span>
<span data-ttu-id="5b596-117">Gibt den Namen der Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="5b596-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b596-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b596-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b596-119">Gibt den Namen der Ressourcengruppe an, der die SQL Server wird.</span><span class="sxs-lookup"><span data-stu-id="5b596-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5b596-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b596-120">-ServerName</span></span>
<span data-ttu-id="5b596-121">Gibt den Namen der SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5b596-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="5b596-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b596-122">-Confirm</span></span>
<span data-ttu-id="5b596-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b596-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b596-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5b596-124">-WhatIf</span></span>
<span data-ttu-id="5b596-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b596-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b596-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b596-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b596-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b596-127">CommonParameters</span></span>
<span data-ttu-id="5b596-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b596-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b596-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b596-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b596-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b596-130">INPUTS</span></span>

### <span data-ttu-id="5b596-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5b596-131">System.String</span></span>

## <span data-ttu-id="5b596-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b596-132">OUTPUTS</span></span>

### <span data-ttu-id="5b596-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5b596-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5b596-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b596-134">NOTES</span></span>

## <span data-ttu-id="5b596-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b596-135">RELATED LINKS</span></span>

[<span data-ttu-id="5b596-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b596-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5b596-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b596-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5b596-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b596-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5b596-139">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5b596-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


