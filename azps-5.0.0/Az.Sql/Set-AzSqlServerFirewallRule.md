---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300447"
---
# <span data-ttu-id="86b77-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b77-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="86b77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86b77-102">SYNOPSIS</span></span>
<span data-ttu-id="86b77-103">Ändert eine Firewallregel in Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="86b77-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="86b77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86b77-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b77-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86b77-105">DESCRIPTION</span></span>
<span data-ttu-id="86b77-106">Das Cmdlet " **Satz-AzSqlServerFirewallRule** " ändert eine Firewallregel in einem Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="86b77-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="86b77-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86b77-107">EXAMPLES</span></span>

### <span data-ttu-id="86b77-108">Beispiel 1: Ändern einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="86b77-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="86b77-109">Mit diesem Befehl wird eine Firewallregel mit dem Namen Rule01 auf dem Server mit dem Namen Server01 geändert.</span><span class="sxs-lookup"><span data-stu-id="86b77-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="86b77-110">Der Befehl ändert die Start-und endip-Adressen.</span><span class="sxs-lookup"><span data-stu-id="86b77-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="86b77-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="86b77-111">PARAMETERS</span></span>

### <span data-ttu-id="86b77-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b77-112">-DefaultProfile</span></span>
<span data-ttu-id="86b77-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="86b77-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86b77-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="86b77-114">-EndIpAddress</span></span>
<span data-ttu-id="86b77-115">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="86b77-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="86b77-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="86b77-116">-FirewallRuleName</span></span>
<span data-ttu-id="86b77-117">Gibt den Namen der Firewall-Regel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="86b77-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="86b77-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b77-118">-ResourceGroupName</span></span>
<span data-ttu-id="86b77-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="86b77-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="86b77-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="86b77-120">-ServerName</span></span>
<span data-ttu-id="86b77-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="86b77-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="86b77-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="86b77-122">-StartIpAddress</span></span>
<span data-ttu-id="86b77-123">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="86b77-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="86b77-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86b77-124">-Confirm</span></span>
<span data-ttu-id="86b77-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86b77-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b77-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b77-126">-WhatIf</span></span>
<span data-ttu-id="86b77-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86b77-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b77-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86b77-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b77-129">CommonParameters</span></span>
<span data-ttu-id="86b77-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b77-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86b77-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b77-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86b77-132">INPUTS</span></span>

### <span data-ttu-id="86b77-133">System. String</span><span class="sxs-lookup"><span data-stu-id="86b77-133">System.String</span></span>

## <span data-ttu-id="86b77-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86b77-134">OUTPUTS</span></span>

### <span data-ttu-id="86b77-135">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="86b77-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="86b77-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="86b77-136">NOTES</span></span>

## <span data-ttu-id="86b77-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86b77-137">RELATED LINKS</span></span>

[<span data-ttu-id="86b77-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b77-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b77-139">Neu – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b77-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b77-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b77-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b77-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="86b77-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


