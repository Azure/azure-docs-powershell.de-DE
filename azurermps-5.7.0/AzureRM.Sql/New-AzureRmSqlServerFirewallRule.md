---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498721"
---
# <span data-ttu-id="72e8f-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72e8f-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="72e8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="72e8f-103">Erstellt eine Firewall-Regel für einen SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="72e8f-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e8f-104">SYNTAX</span></span>

### <span data-ttu-id="72e8f-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="72e8f-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e8f-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="72e8f-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e8f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72e8f-107">DESCRIPTION</span></span>
<span data-ttu-id="72e8f-108">Das Cmdlet **New-AzureRmSqlServerFirewallRule** erstellt eine Firewallregel für den angegebenen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="72e8f-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="72e8f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="72e8f-110">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="72e8f-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="72e8f-111">Mit diesem Befehl wird eine Firewallregel mit dem Namen Rule01 auf dem Server mit dem Namen "Server01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="72e8f-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="72e8f-112">Die Regel enthält die angegebenen Start-und endip-Adressen.</span><span class="sxs-lookup"><span data-stu-id="72e8f-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="72e8f-113">Beispiel 2: Erstellen einer Firewallregel, die es allen Azure-IP-Adressen ermöglicht, auf den Server zuzugreifen</span><span class="sxs-lookup"><span data-stu-id="72e8f-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="72e8f-114">Mit diesem Befehl wird eine Firewallregel auf dem Server namens "Server01" erstellt, die zur Ressourcengruppe mit dem Namen "ResourceGroup01" gehört.</span><span class="sxs-lookup"><span data-stu-id="72e8f-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="72e8f-115">Seit der Verwendung des *AllowAllAzureIPs* -Parameters können mit der Firewallregel alle Azure-IP-Adressen auf den Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="72e8f-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="72e8f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e8f-116">PARAMETERS</span></span>

### <span data-ttu-id="72e8f-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="72e8f-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="72e8f-118">Gibt an, dass diese Firewallregel alle Azure-IP-Adressen für den Zugriff auf den Server zulässt.</span><span class="sxs-lookup"><span data-stu-id="72e8f-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="72e8f-119">Sie können diesen Parameter nicht verwenden, wenn Sie beabsichtigen, die *FirewallRuleName* -, *StartIpAddress* -und *EndIpAddress* -Parameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="72e8f-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="72e8f-120">Wenn Sie Azure IPS den Zugriff auf den Server gestatten möchten, sollte dieser Parameter in einem separaten Cmdlet-Aufruf verwendet werden, der die *FirewallRuleName* -, *StartIpAddress* -und *EndIpAddress* -Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="72e8f-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e8f-121">-DefaultProfile</span></span>
<span data-ttu-id="72e8f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="72e8f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72e8f-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="72e8f-123">-EndIpAddress</span></span>
<span data-ttu-id="72e8f-124">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="72e8f-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e8f-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="72e8f-125">-FirewallRuleName</span></span>
<span data-ttu-id="72e8f-126">Gibt den Namen der neuen Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="72e8f-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="72e8f-128">Gibt den Namen einer Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="72e8f-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72e8f-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="72e8f-129">-ServerName</span></span>
<span data-ttu-id="72e8f-130">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="72e8f-130">Specifies the name of a server.</span></span>
<span data-ttu-id="72e8f-131">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="72e8f-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="72e8f-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="72e8f-132">-StartIpAddress</span></span>
<span data-ttu-id="72e8f-133">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="72e8f-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e8f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72e8f-134">-Confirm</span></span>
<span data-ttu-id="72e8f-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72e8f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e8f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e8f-136">-WhatIf</span></span>
<span data-ttu-id="72e8f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72e8f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e8f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e8f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e8f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e8f-139">CommonParameters</span></span>
<span data-ttu-id="72e8f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e8f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e8f-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e8f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e8f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72e8f-142">INPUTS</span></span>

### <span data-ttu-id="72e8f-143">Keine</span><span class="sxs-lookup"><span data-stu-id="72e8f-143">None</span></span>
<span data-ttu-id="72e8f-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="72e8f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72e8f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72e8f-145">OUTPUTS</span></span>

### <span data-ttu-id="72e8f-146">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="72e8f-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="72e8f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="72e8f-147">NOTES</span></span>

## <span data-ttu-id="72e8f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72e8f-148">RELATED LINKS</span></span>

[<span data-ttu-id="72e8f-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72e8f-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="72e8f-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72e8f-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="72e8f-151">Satz-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72e8f-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="72e8f-152">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="72e8f-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


