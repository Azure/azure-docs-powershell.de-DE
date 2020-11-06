---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478193"
---
# <span data-ttu-id="44d0d-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44d0d-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="44d0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="44d0d-103">Ändert eine Firewallregel in Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="44d0d-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44d0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44d0d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44d0d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44d0d-105">DESCRIPTION</span></span>
<span data-ttu-id="44d0d-106">Das Cmdlet " **Satz-AzureRmSqlServerFirewallRule** " ändert eine Firewallregel in einem Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="44d0d-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="44d0d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44d0d-107">EXAMPLES</span></span>

### <span data-ttu-id="44d0d-108">Beispiel 1: Ändern einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="44d0d-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="44d0d-109">Mit diesem Befehl wird eine Firewallregel mit dem Namen Rule01 auf dem Server mit dem Namen Server01 geändert.</span><span class="sxs-lookup"><span data-stu-id="44d0d-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="44d0d-110">Der Befehl ändert die Start-und endip-Adressen.</span><span class="sxs-lookup"><span data-stu-id="44d0d-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="44d0d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="44d0d-111">PARAMETERS</span></span>

### <span data-ttu-id="44d0d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d0d-112">-DefaultProfile</span></span>
<span data-ttu-id="44d0d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="44d0d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44d0d-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="44d0d-114">-EndIpAddress</span></span>
<span data-ttu-id="44d0d-115">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="44d0d-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="44d0d-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="44d0d-116">-FirewallRuleName</span></span>
<span data-ttu-id="44d0d-117">Gibt den Namen der Firewall-Regel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="44d0d-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="44d0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="44d0d-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="44d0d-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="44d0d-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="44d0d-120">-ServerName</span></span>
<span data-ttu-id="44d0d-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="44d0d-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="44d0d-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="44d0d-122">-StartIpAddress</span></span>
<span data-ttu-id="44d0d-123">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="44d0d-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="44d0d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44d0d-124">-Confirm</span></span>
<span data-ttu-id="44d0d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44d0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44d0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44d0d-126">-WhatIf</span></span>
<span data-ttu-id="44d0d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d0d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44d0d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44d0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44d0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d0d-129">CommonParameters</span></span>
<span data-ttu-id="44d0d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d0d-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d0d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44d0d-132">INPUTS</span></span>

### <span data-ttu-id="44d0d-133">Keine</span><span class="sxs-lookup"><span data-stu-id="44d0d-133">None</span></span>
<span data-ttu-id="44d0d-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="44d0d-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44d0d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44d0d-135">OUTPUTS</span></span>

### <span data-ttu-id="44d0d-136">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="44d0d-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="44d0d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="44d0d-137">NOTES</span></span>

## <span data-ttu-id="44d0d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44d0d-138">RELATED LINKS</span></span>

[<span data-ttu-id="44d0d-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44d0d-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="44d0d-140">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44d0d-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="44d0d-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44d0d-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="44d0d-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="44d0d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


