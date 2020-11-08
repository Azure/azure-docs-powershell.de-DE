---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005778"
---
# <span data-ttu-id="05128-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05128-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="05128-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05128-102">SYNOPSIS</span></span>
<span data-ttu-id="05128-103">Ruft Firewallregeln für Azure SQL-Daten Bank Server ab.</span><span class="sxs-lookup"><span data-stu-id="05128-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="05128-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05128-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="05128-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05128-105">DESCRIPTION</span></span>
<span data-ttu-id="05128-106">Das Cmdlet " **Get-AzureSqlDatabaseServerFirewallRule** " ruft Firewallregeln für eine Instanz des Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="05128-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="05128-107">Wenn Sie eine Firewallregel mit dem Namen angeben, gibt dieses Cmdlet Informationen zu dieser Firewallregel zurück.</span><span class="sxs-lookup"><span data-stu-id="05128-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="05128-108">Andernfalls gibt das Cmdlet Informationen zu allen Firewallregeln auf dem angegebenen Azure SQL-Datenbankserver zurück.</span><span class="sxs-lookup"><span data-stu-id="05128-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="05128-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05128-109">EXAMPLES</span></span>

### <span data-ttu-id="05128-110">Beispiel 1: Abrufen aller Firewallregeln auf einem Server</span><span class="sxs-lookup"><span data-stu-id="05128-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="05128-111">Dieser Befehl ruft alle Firewallregeln auf dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y ab.</span><span class="sxs-lookup"><span data-stu-id="05128-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="05128-112">Beispiel 2: Abrufen einer Firewallregel mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="05128-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="05128-113">Dieser Befehl ruft die Firewallregel mit dem Namen FirewallRule24 auf dem Server mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="05128-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="05128-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="05128-114">PARAMETERS</span></span>

### <span data-ttu-id="05128-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="05128-115">-Profile</span></span>
<span data-ttu-id="05128-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="05128-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05128-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="05128-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05128-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="05128-118">-RuleName</span></span>
<span data-ttu-id="05128-119">Gibt den Namen der Firewall-Regel an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="05128-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05128-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="05128-120">-ServerName</span></span>
<span data-ttu-id="05128-121">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="05128-121">Specifies the name of a server.</span></span>
<span data-ttu-id="05128-122">Dieses Cmdlet ruft Firewallregeln vom Server ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="05128-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="05128-123">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="05128-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="05128-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05128-124">CommonParameters</span></span>
<span data-ttu-id="05128-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05128-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05128-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05128-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05128-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05128-127">INPUTS</span></span>

### <span data-ttu-id="05128-128">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="05128-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="05128-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05128-129">OUTPUTS</span></span>

### <span data-ttu-id="05128-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="05128-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="05128-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="05128-131">NOTES</span></span>

## <span data-ttu-id="05128-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05128-132">RELATED LINKS</span></span>

[<span data-ttu-id="05128-133">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="05128-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="05128-134">Listen Firewall-Regeln</span><span class="sxs-lookup"><span data-stu-id="05128-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="05128-135">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="05128-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="05128-136">Neu – AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05128-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="05128-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05128-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="05128-138">Satz-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05128-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


