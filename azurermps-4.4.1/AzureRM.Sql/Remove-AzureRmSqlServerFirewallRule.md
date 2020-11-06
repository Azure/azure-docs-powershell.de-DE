---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478850"
---
# <span data-ttu-id="ab909-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab909-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="ab909-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab909-102">SYNOPSIS</span></span>
<span data-ttu-id="ab909-103">Löscht eine Firewall-Regel von einem SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="ab909-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab909-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab909-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab909-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab909-105">DESCRIPTION</span></span>
<span data-ttu-id="ab909-106">Mit dem Cmdlet **Remove-AzureRmSqlServerFirewallRule** wird eine Firewallregel aus dem angegebenen Azure SQL-Datenbankserver gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ab909-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="ab909-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab909-107">EXAMPLES</span></span>

### <span data-ttu-id="ab909-108">Beispiel 1: Löschen einer Regel</span><span class="sxs-lookup"><span data-stu-id="ab909-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ab909-109">Mit diesem Befehl wird eine Firewallregel namens Rule01 auf dem Server mit dem Namen "Server01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ab909-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="ab909-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab909-110">PARAMETERS</span></span>

### <span data-ttu-id="ab909-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ab909-111">-FirewallRuleName</span></span>
<span data-ttu-id="ab909-112">Gibt den Namen der Firewall-Regel an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="ab909-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ab909-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ab909-113">-Force</span></span>
<span data-ttu-id="ab909-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ab909-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab909-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab909-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab909-116">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ab909-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ab909-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="ab909-117">-ServerName</span></span>
<span data-ttu-id="ab909-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="ab909-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ab909-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab909-119">-Confirm</span></span>
<span data-ttu-id="ab909-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab909-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab909-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab909-121">-WhatIf</span></span>
<span data-ttu-id="ab909-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab909-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab909-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab909-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab909-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab909-124">-DefaultProfile</span></span>
<span data-ttu-id="ab909-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab909-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab909-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab909-126">CommonParameters</span></span>
<span data-ttu-id="ab909-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab909-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab909-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab909-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab909-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab909-129">INPUTS</span></span>

### <span data-ttu-id="ab909-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ab909-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ab909-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab909-131">OUTPUTS</span></span>

## <span data-ttu-id="ab909-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab909-132">NOTES</span></span>

## <span data-ttu-id="ab909-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab909-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab909-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab909-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ab909-135">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab909-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ab909-136">Satz-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab909-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ab909-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ab909-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


