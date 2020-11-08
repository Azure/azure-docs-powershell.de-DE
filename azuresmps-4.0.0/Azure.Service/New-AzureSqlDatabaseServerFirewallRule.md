---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006175"
---
# <span data-ttu-id="c4101-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4101-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="c4101-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4101-102">SYNOPSIS</span></span>
<span data-ttu-id="c4101-103">Erstellt eine Firewall-Regel in Azure SQL-Daten Bank Server.</span><span class="sxs-lookup"><span data-stu-id="c4101-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="c4101-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4101-104">SYNTAX</span></span>

### <span data-ttu-id="c4101-105">IpRange (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4101-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4101-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="c4101-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4101-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4101-107">DESCRIPTION</span></span>
<span data-ttu-id="c4101-108">Das Cmdlet **New-AzureSqlDatabaseServerFirewallRule** erstellt eine Firewallregel in der angegebenen Instanz des Azure SQL-Datenbankservers im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4101-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="c4101-109">Verwenden Sie die *StartIpAddress* -und *EndIpAddress* -Parameter, um einen Bereich von IP-Adressen anzugeben, die von dieser Regel zum Herstellen einer Verbindung mit dem Azure SQL-Datenbankserver zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c4101-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="c4101-110">Geben Sie den *AllowAllAzureServices* -Parameter an, um eine Regel zu erstellen, die Azure-Verbindungen mit dem Server ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c4101-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="c4101-111">Die Regel hat die Anfangs-und Endwerte der IP-Adressen von 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="c4101-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="c4101-112">Wenn Sie keinen Firewallregel-Regelnamen angeben, weist dieses Cmdlet den Standardnamen AllowAllAzureServices zu.</span><span class="sxs-lookup"><span data-stu-id="c4101-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="c4101-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4101-113">EXAMPLES</span></span>

### <span data-ttu-id="c4101-114">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="c4101-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="c4101-115">Mit diesem Befehl wird ein Firewallregel-FirewallRule24 auf dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4101-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="c4101-116">Der Befehl gibt einen IP-Adressbereich an.</span><span class="sxs-lookup"><span data-stu-id="c4101-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="c4101-117">Beispiel 2: Erstellen einer Regel, die alle Azure-Dienste zulässt</span><span class="sxs-lookup"><span data-stu-id="c4101-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="c4101-118">Dieser Befehl erstellt eine Firewallregel mit dem Namen AzureConnections auf dem Server mit dem Namen lpqd0zbr8y, der Azure-Verbindungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="c4101-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="c4101-119">Beispiel 3: Erstellen einer Regel, mit der alle Azure-Dienste, die den Standardnamen verwenden, eine Regel erstellen, die alle Azure-Dienste zulässt, die den Standardnamen verwenden</span><span class="sxs-lookup"><span data-stu-id="c4101-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="c4101-120">Mit diesem Befehl wird eine Firewallregel auf dem angegebenen Server mit dem Namen "lpqd0zbr8y" erstellt, die Azure-Verbindungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="c4101-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="c4101-121">Der Befehl weist den standardmäßigen Regelnamen AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="c4101-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="c4101-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4101-122">PARAMETERS</span></span>

### <span data-ttu-id="c4101-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="c4101-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="c4101-124">Gibt an, dass diese Firewall-Regel alle Azure-IP-Adressen für den Zugriff auf den Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4101-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4101-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4101-125">-EndIpAddress</span></span>
<span data-ttu-id="c4101-126">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="c4101-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4101-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c4101-127">-Force</span></span>
<span data-ttu-id="c4101-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c4101-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4101-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4101-129">-Profile</span></span>
<span data-ttu-id="c4101-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c4101-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4101-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c4101-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4101-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c4101-132">-RuleName</span></span>
<span data-ttu-id="c4101-133">Gibt den Namen der neuen Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="c4101-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4101-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="c4101-134">-ServerName</span></span>
<span data-ttu-id="c4101-135">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="c4101-135">Specifies the name of a server.</span></span>
<span data-ttu-id="c4101-136">Mit diesem Cmdlet wird eine Firewallregel auf dem Server erstellt, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4101-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="c4101-137">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="c4101-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="c4101-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4101-138">-StartIpAddress</span></span>
<span data-ttu-id="c4101-139">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="c4101-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4101-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4101-140">-Confirm</span></span>
<span data-ttu-id="c4101-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4101-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4101-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4101-142">-WhatIf</span></span>
<span data-ttu-id="c4101-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4101-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4101-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4101-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4101-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4101-145">CommonParameters</span></span>
<span data-ttu-id="c4101-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4101-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4101-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4101-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4101-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4101-148">INPUTS</span></span>

## <span data-ttu-id="c4101-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4101-149">OUTPUTS</span></span>

### <span data-ttu-id="c4101-150">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="c4101-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="c4101-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4101-151">NOTES</span></span>

## <span data-ttu-id="c4101-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4101-152">RELATED LINKS</span></span>

[<span data-ttu-id="c4101-153">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="c4101-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c4101-154">Firewall-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="c4101-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="c4101-155">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="c4101-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c4101-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4101-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c4101-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4101-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c4101-158">Satz-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4101-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


