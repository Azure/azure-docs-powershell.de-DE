---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939387"
---
# <span data-ttu-id="5e574-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e574-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5e574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e574-102">SYNOPSIS</span></span>
<span data-ttu-id="5e574-103">Ändert eine Firewallregel in Azure SQL Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="5e574-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="5e574-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e574-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e574-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e574-105">DESCRIPTION</span></span>
<span data-ttu-id="5e574-106">Das **Cmdlet Set-AzSqlServerFirewallRule** ändert eine Firewallregel in einem Azure SQL Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="5e574-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="5e574-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e574-107">EXAMPLES</span></span>

### <span data-ttu-id="5e574-108">Beispiel 1: Ändern einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="5e574-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="5e574-109">Mit diesem Befehl wird eine Firewallregel namens Regel01 auf dem Server mit dem Namen Server01 geändert.</span><span class="sxs-lookup"><span data-stu-id="5e574-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="5e574-110">Mit dem Befehl werden die START- und End-IP-Adressen geändert.</span><span class="sxs-lookup"><span data-stu-id="5e574-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="5e574-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e574-111">PARAMETERS</span></span>

### <span data-ttu-id="5e574-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e574-112">-DefaultProfile</span></span>
<span data-ttu-id="5e574-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5e574-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e574-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5e574-114">-EndIpAddress</span></span>
<span data-ttu-id="5e574-115">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="5e574-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e574-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5e574-116">-FirewallRuleName</span></span>
<span data-ttu-id="5e574-117">Gibt den Namen der Firewallregel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5e574-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5e574-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e574-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e574-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5e574-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5e574-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="5e574-120">-ServerName</span></span>
<span data-ttu-id="5e574-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="5e574-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5e574-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5e574-122">-StartIpAddress</span></span>
<span data-ttu-id="5e574-123">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="5e574-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e574-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e574-124">-Confirm</span></span>
<span data-ttu-id="5e574-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e574-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e574-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e574-126">-WhatIf</span></span>
<span data-ttu-id="5e574-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e574-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e574-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e574-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e574-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e574-129">CommonParameters</span></span>
<span data-ttu-id="5e574-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e574-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e574-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e574-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e574-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e574-132">INPUTS</span></span>

### <span data-ttu-id="5e574-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5e574-133">System.String</span></span>

## <span data-ttu-id="5e574-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e574-134">OUTPUTS</span></span>

### <span data-ttu-id="5e574-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5e574-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5e574-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e574-136">NOTES</span></span>

## <span data-ttu-id="5e574-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e574-137">RELATED LINKS</span></span>

[<span data-ttu-id="5e574-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e574-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5e574-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e574-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5e574-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e574-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5e574-141">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5e574-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


