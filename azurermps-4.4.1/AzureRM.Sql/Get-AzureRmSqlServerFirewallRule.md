---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663810"
---
# <span data-ttu-id="945d6-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="945d6-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="945d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="945d6-102">SYNOPSIS</span></span>
<span data-ttu-id="945d6-103">Ruft Firewallregeln für einen SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="945d6-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="945d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="945d6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="945d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="945d6-105">DESCRIPTION</span></span>
<span data-ttu-id="945d6-106">Das Cmdlet " **Get-AzureRmSqlServerFirewallRule** " ruft Firewallregeln für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="945d6-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="945d6-107">Wenn Sie den Namen einer Firewallregel angeben, ruft dieses Cmdlet Informationen zu dieser bestimmten Firewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="945d6-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="945d6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="945d6-108">EXAMPLES</span></span>

### <span data-ttu-id="945d6-109">Beispiel 1: Abrufen aller Regeln für einen Server</span><span class="sxs-lookup"><span data-stu-id="945d6-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="945d6-110">Dieser Befehl ruft alle Firewallregeln für den Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="945d6-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="945d6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="945d6-111">PARAMETERS</span></span>

### <span data-ttu-id="945d6-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="945d6-112">-FirewallRuleName</span></span>
<span data-ttu-id="945d6-113">Gibt den Namen der Firewall-Regel an.</span><span class="sxs-lookup"><span data-stu-id="945d6-113">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945d6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945d6-114">-ResourceGroupName</span></span>
<span data-ttu-id="945d6-115">Gibt den Namen der Ressourcengruppe an, der der SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="945d6-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="945d6-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="945d6-116">-ServerName</span></span>
<span data-ttu-id="945d6-117">Gibt den Namen des SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="945d6-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="945d6-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="945d6-118">-Confirm</span></span>
<span data-ttu-id="945d6-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="945d6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="945d6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="945d6-120">-WhatIf</span></span>
<span data-ttu-id="945d6-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="945d6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="945d6-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="945d6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="945d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945d6-123">-DefaultProfile</span></span>
<span data-ttu-id="945d6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="945d6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="945d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945d6-125">CommonParameters</span></span>
<span data-ttu-id="945d6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945d6-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945d6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="945d6-128">INPUTS</span></span>

## <span data-ttu-id="945d6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="945d6-129">OUTPUTS</span></span>

### <span data-ttu-id="945d6-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="945d6-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="945d6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="945d6-131">NOTES</span></span>

## <span data-ttu-id="945d6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="945d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="945d6-133">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="945d6-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="945d6-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="945d6-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="945d6-135">Satz-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="945d6-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="945d6-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="945d6-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


