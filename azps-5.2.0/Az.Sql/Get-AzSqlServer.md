---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304544"
---
# <span data-ttu-id="c4069-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="c4069-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="c4069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4069-102">SYNOPSIS</span></span>
<span data-ttu-id="c4069-103">Gibt Informationen zu SQL Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="c4069-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="c4069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4069-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4069-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4069-105">DESCRIPTION</span></span>
<span data-ttu-id="c4069-106">Das **Cmdlet "Get-AzSqlServer"** gibt Informationen zu einem oder mehreren Azure SQL Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="c4069-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="c4069-107">Geben Sie den Namen eines Servers an, um nur Informationen für diesen Server zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c4069-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="c4069-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4069-108">EXAMPLES</span></span>

### <span data-ttu-id="c4069-109">Beispiel 1: Alle Instanzen einer SQL Server Ressourcengruppe zugewiesen</span><span class="sxs-lookup"><span data-stu-id="c4069-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="c4069-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern ab, die der Ressourcengruppe "ResourceGroup01" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="c4069-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c4069-111">Beispiel 2: Informationen zu einem Azure SQL Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="c4069-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="c4069-112">Dieser Befehl ruft Informationen zum Azure SQL Datenbankserver namens Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="c4069-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="c4069-113">Beispiel 3: Alle Instanzen von SQL Server im Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="c4069-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="c4069-114">Dieser Befehl ruft Informationen zu allen Azure SQL Datenbankservern im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c4069-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="c4069-115">Beispiel 4: Erhalten aller Instanzen von SQL Server, die einer Ressourcengruppe mithilfe von Filtern zugewiesen wurden</span><span class="sxs-lookup"><span data-stu-id="c4069-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="c4069-116">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern ab, die der Ressourcengruppe "ResourceGroup01" zugeordnet sind und mit "server" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c4069-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="c4069-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4069-117">PARAMETERS</span></span>

### <span data-ttu-id="c4069-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4069-118">-DefaultProfile</span></span>
<span data-ttu-id="c4069-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c4069-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4069-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4069-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4069-121">Gibt den Namen der Ressourcengruppe an, der Server zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c4069-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4069-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4069-122">-ServerName</span></span>
<span data-ttu-id="c4069-123">Gibt den Namen des Servers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c4069-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4069-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4069-124">-Confirm</span></span>
<span data-ttu-id="c4069-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4069-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4069-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4069-126">-WhatIf</span></span>
<span data-ttu-id="c4069-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4069-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4069-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4069-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4069-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4069-129">CommonParameters</span></span>
<span data-ttu-id="c4069-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4069-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4069-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4069-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4069-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4069-132">INPUTS</span></span>

### <span data-ttu-id="c4069-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4069-133">System.String</span></span>

## <span data-ttu-id="c4069-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4069-134">OUTPUTS</span></span>

### <span data-ttu-id="c4069-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c4069-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c4069-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4069-136">NOTES</span></span>

## <span data-ttu-id="c4069-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4069-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4069-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="c4069-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="c4069-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="c4069-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="c4069-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="c4069-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="c4069-141">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c4069-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


