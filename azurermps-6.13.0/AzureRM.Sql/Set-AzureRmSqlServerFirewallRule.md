---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e3d2d706a954bf8cbd7359be4ee7a835fdd4f431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481973"
---
# <span data-ttu-id="a101b-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a101b-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a101b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a101b-102">SYNOPSIS</span></span>
<span data-ttu-id="a101b-103">Ändert eine Firewallregel in Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="a101b-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a101b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a101b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a101b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a101b-105">DESCRIPTION</span></span>
<span data-ttu-id="a101b-106">Das Cmdlet " **Satz-AzureRmSqlServerFirewallRule** " ändert eine Firewallregel in einem Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="a101b-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="a101b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a101b-107">EXAMPLES</span></span>

### <span data-ttu-id="a101b-108">Beispiel 1: Ändern einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="a101b-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="a101b-109">Mit diesem Befehl wird eine Firewallregel mit dem Namen Rule01 auf dem Server mit dem Namen Server01 geändert.</span><span class="sxs-lookup"><span data-stu-id="a101b-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="a101b-110">Der Befehl ändert die Start-und endip-Adressen.</span><span class="sxs-lookup"><span data-stu-id="a101b-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="a101b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a101b-111">PARAMETERS</span></span>

### <span data-ttu-id="a101b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a101b-112">-DefaultProfile</span></span>
<span data-ttu-id="a101b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a101b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a101b-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a101b-114">-EndIpAddress</span></span>
<span data-ttu-id="a101b-115">Gibt den Endwert des IP-Adressbereichs für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="a101b-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="a101b-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a101b-116">-FirewallRuleName</span></span>
<span data-ttu-id="a101b-117">Gibt den Namen der Firewall-Regel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a101b-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a101b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a101b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a101b-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a101b-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a101b-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="a101b-120">-ServerName</span></span>
<span data-ttu-id="a101b-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="a101b-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a101b-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a101b-122">-StartIpAddress</span></span>
<span data-ttu-id="a101b-123">Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.</span><span class="sxs-lookup"><span data-stu-id="a101b-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="a101b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a101b-124">-Confirm</span></span>
<span data-ttu-id="a101b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a101b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a101b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a101b-126">-WhatIf</span></span>
<span data-ttu-id="a101b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a101b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a101b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a101b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a101b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a101b-129">CommonParameters</span></span>
<span data-ttu-id="a101b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a101b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a101b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a101b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a101b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a101b-132">INPUTS</span></span>

### <span data-ttu-id="a101b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a101b-133">System.String</span></span>

## <span data-ttu-id="a101b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a101b-134">OUTPUTS</span></span>

### <span data-ttu-id="a101b-135">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a101b-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a101b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a101b-136">NOTES</span></span>

## <span data-ttu-id="a101b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a101b-137">RELATED LINKS</span></span>

[<span data-ttu-id="a101b-138">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a101b-138">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a101b-139">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a101b-139">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a101b-140">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a101b-140">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a101b-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a101b-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


