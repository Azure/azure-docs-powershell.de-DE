---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176862"
---
# <span data-ttu-id="84875-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="84875-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="84875-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84875-102">SYNOPSIS</span></span>
<span data-ttu-id="84875-103">Erstellt eine Firewall-Regel für einen SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="84875-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="84875-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84875-104">SYNTAX</span></span>

### <span data-ttu-id="84875-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="84875-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84875-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="84875-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84875-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84875-107">DESCRIPTION</span></span>
<span data-ttu-id="84875-108">Das Cmdlet **New-AzSqlServerFirewallRule** erstellt eine Firewallregel für den angegebenen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="84875-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="84875-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84875-109">EXAMPLES</span></span>

### <span data-ttu-id="84875-110">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="84875-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="84875-111">Mit diesem Befehl wird eine Firewallregel mit dem Namen Rule01 auf dem Server mit dem Namen "Server01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="84875-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="84875-112">Die Regel enthält die angegebenen Start-und endip-Adressen.</span><span class="sxs-lookup"><span data-stu-id="84875-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="84875-113">Beispiel 2: Erstellen einer Firewallregel, die es allen Azure-IP-Adressen ermöglicht, auf den Server zuzugreifen</span><span class="sxs-lookup"><span data-stu-id="84875-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="84875-114">Mit diesem Befehl wird eine Firewallregel auf dem Server namens "Server01" erstellt, die zur Ressourcengruppe mit dem Namen "ResourceGroup01" gehört.</span><span class="sxs-lookup"><span data-stu-id="84875-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="84875-115">Seit der Verwendung des *AllowAllAzureIPs* -Parameters können mit der Firewallregel alle Azure-IP-Adressen auf den Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="84875-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="84875-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="84875-116">PARAMETERS</span></span>

### <span data-ttu-id="84875-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="84875-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="84875-118">Gibt an, dass diese Firewallregel alle Azure-IP-Adressen für den Zugriff auf den Server zulässt.</span><span class="sxs-lookup"><span data-stu-id="84875-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="84875-119">Sie können diesen Parameter nicht verwenden, wenn Sie beabsichtigen, die *FirewallRuleName* -, *StartIpAddress* -und *EndIpAddress* -Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84875-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="84875-120">Wenn Sie Azure IPS den Zugriff auf den Server gestatten möchten, sollte dieser Parameter in einem separaten Cmdlet-Aufruf verwendet werden, der die *FirewallRuleName* -, *StartIpAddress* -und *EndIpAddress* -Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="84875-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84875-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84875-121">-DefaultProfile</span></span>
<span data-ttu-id="84875-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="84875-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84875-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="84875-123">-EndIpAddress</span></span>
<span data-ttu-id="84875-124">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="84875-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84875-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="84875-125">-FirewallRuleName</span></span>
<span data-ttu-id="84875-126">Gibt den Namen der neuen Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="84875-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84875-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84875-127">-ResourceGroupName</span></span>
<span data-ttu-id="84875-128">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="84875-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="84875-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="84875-129">-ServerName</span></span>
<span data-ttu-id="84875-130">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="84875-130">Specifies the name of a server.</span></span>
<span data-ttu-id="84875-131">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="84875-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="84875-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="84875-132">-StartIpAddress</span></span>
<span data-ttu-id="84875-133">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="84875-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84875-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84875-134">-Confirm</span></span>
<span data-ttu-id="84875-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84875-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84875-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84875-136">-WhatIf</span></span>
<span data-ttu-id="84875-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84875-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84875-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84875-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84875-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84875-139">CommonParameters</span></span>
<span data-ttu-id="84875-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84875-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84875-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84875-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84875-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84875-142">INPUTS</span></span>

### <span data-ttu-id="84875-143">System. String</span><span class="sxs-lookup"><span data-stu-id="84875-143">System.String</span></span>

## <span data-ttu-id="84875-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84875-144">OUTPUTS</span></span>

### <span data-ttu-id="84875-145">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="84875-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="84875-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="84875-146">NOTES</span></span>

## <span data-ttu-id="84875-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84875-147">RELATED LINKS</span></span>

[<span data-ttu-id="84875-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="84875-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="84875-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="84875-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="84875-150">Satz-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="84875-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="84875-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="84875-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


