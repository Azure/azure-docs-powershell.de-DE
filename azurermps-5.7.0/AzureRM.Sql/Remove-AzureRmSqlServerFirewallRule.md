---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480825"
---
# <span data-ttu-id="dcbca-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dcbca-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="dcbca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dcbca-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbca-103">Löscht eine Firewall-Regel von einem SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="dcbca-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcbca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcbca-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcbca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcbca-105">DESCRIPTION</span></span>
<span data-ttu-id="dcbca-106">Mit dem Cmdlet **Remove-AzureRmSqlServerFirewallRule** wird eine Firewallregel aus dem angegebenen Azure SQL-Datenbankserver gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dcbca-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="dcbca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcbca-107">EXAMPLES</span></span>

### <span data-ttu-id="dcbca-108">Beispiel 1: Löschen einer Regel</span><span class="sxs-lookup"><span data-stu-id="dcbca-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="dcbca-109">Mit diesem Befehl wird eine Firewallregel namens Rule01 auf dem Server mit dem Namen "Server01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dcbca-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="dcbca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcbca-110">PARAMETERS</span></span>

### <span data-ttu-id="dcbca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbca-111">-DefaultProfile</span></span>
<span data-ttu-id="dcbca-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dcbca-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="dcbca-113">-FirewallRuleName</span></span>
<span data-ttu-id="dcbca-114">Gibt den Namen der Firewall-Regel an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="dcbca-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dcbca-115">-Force</span></span>
<span data-ttu-id="dcbca-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="dcbca-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbca-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcbca-118">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dcbca-118">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="dcbca-119">-ServerName</span></span>
<span data-ttu-id="dcbca-120">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="dcbca-120">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dcbca-121">-Confirm</span></span>
<span data-ttu-id="dcbca-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcbca-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcbca-123">-WhatIf</span></span>
<span data-ttu-id="dcbca-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcbca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcbca-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcbca-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbca-126">CommonParameters</span></span>
<span data-ttu-id="dcbca-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbca-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbca-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dcbca-129">INPUTS</span></span>

### <span data-ttu-id="dcbca-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="dcbca-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="dcbca-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dcbca-131">OUTPUTS</span></span>

## <span data-ttu-id="dcbca-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="dcbca-132">NOTES</span></span>

## <span data-ttu-id="dcbca-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dcbca-133">RELATED LINKS</span></span>

[<span data-ttu-id="dcbca-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dcbca-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="dcbca-135">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dcbca-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="dcbca-136">Satz-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dcbca-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="dcbca-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="dcbca-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


