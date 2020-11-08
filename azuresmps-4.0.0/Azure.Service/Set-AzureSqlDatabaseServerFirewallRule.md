---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006069"
---
# <span data-ttu-id="0e626-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e626-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="0e626-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e626-102">SYNOPSIS</span></span>
<span data-ttu-id="0e626-103">Ändert eine vorhandene Firewall-Regel in einem Azure SQL-Daten Bank Server.</span><span class="sxs-lookup"><span data-stu-id="0e626-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="0e626-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e626-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e626-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e626-105">DESCRIPTION</span></span>
<span data-ttu-id="0e626-106">Das Cmdlet " **Satz-AzureSqlDatabaseServerFirewallRule** " ändert die Werte für Start-IP-Adresse und endip-Adresse einer vorhandenen Firewallregel in der angegebenen Instanz des Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="0e626-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="0e626-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e626-107">EXAMPLES</span></span>

### <span data-ttu-id="0e626-108">Beispiel 1: Ändern einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="0e626-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="0e626-109">Dieser Befehl ändert die Start-IP-Adresse und die endip-Adresse der Firewallregel mit dem Namen FirewallRule24 auf dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="0e626-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="0e626-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e626-110">PARAMETERS</span></span>

### <span data-ttu-id="0e626-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e626-111">-EndIpAddress</span></span>
<span data-ttu-id="0e626-112">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="0e626-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e626-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0e626-113">-Force</span></span>
<span data-ttu-id="0e626-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0e626-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e626-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="0e626-115">-Profile</span></span>
<span data-ttu-id="0e626-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0e626-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e626-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0e626-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e626-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="0e626-118">-RuleName</span></span>
<span data-ttu-id="0e626-119">Gibt den Namen der Firewall-Regel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0e626-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e626-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="0e626-120">-ServerName</span></span>
<span data-ttu-id="0e626-121">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="0e626-121">Specifies the name of a server.</span></span>
<span data-ttu-id="0e626-122">Mit diesem Cmdlet wird eine Firewallregel auf dem Server erstellt, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e626-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="0e626-123">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="0e626-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e626-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e626-124">-StartIpAddress</span></span>
<span data-ttu-id="0e626-125">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="0e626-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e626-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e626-126">-Confirm</span></span>
<span data-ttu-id="0e626-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e626-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e626-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e626-128">-WhatIf</span></span>
<span data-ttu-id="0e626-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e626-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e626-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e626-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e626-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e626-131">CommonParameters</span></span>
<span data-ttu-id="0e626-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e626-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e626-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e626-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e626-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e626-134">INPUTS</span></span>

### <span data-ttu-id="0e626-135">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="0e626-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="0e626-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e626-136">OUTPUTS</span></span>

### <span data-ttu-id="0e626-137">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="0e626-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="0e626-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e626-138">NOTES</span></span>

## <span data-ttu-id="0e626-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e626-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e626-140">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="0e626-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="0e626-141">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="0e626-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0e626-142">Firewall-Regel einrichten</span><span class="sxs-lookup"><span data-stu-id="0e626-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="0e626-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e626-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="0e626-144">Neu – AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e626-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="0e626-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e626-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


