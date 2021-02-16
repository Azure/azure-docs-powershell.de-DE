---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165785"
---
# <span data-ttu-id="b588a-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b588a-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="b588a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b588a-102">SYNOPSIS</span></span>
<span data-ttu-id="b588a-103">Gibt Informationen zu SQL Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="b588a-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="b588a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b588a-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b588a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b588a-105">DESCRIPTION</span></span>
<span data-ttu-id="b588a-106">Das **Cmdlet "Get-AzSqlServer"** gibt Informationen zu einem oder mehreren Azure SQL Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="b588a-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="b588a-107">Geben Sie den Namen eines Servers an, um nur Informationen für diesen Server zu sehen.</span><span class="sxs-lookup"><span data-stu-id="b588a-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="b588a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b588a-108">EXAMPLES</span></span>

### <span data-ttu-id="b588a-109">Beispiel 1: Alle Instanzen einer SQL Server Ressourcengruppe zugewiesen</span><span class="sxs-lookup"><span data-stu-id="b588a-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
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

<span data-ttu-id="b588a-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern ab, die der Ressourcengruppe "ResourceGroup01" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b588a-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b588a-111">Beispiel 2: Informationen zu einem Azure SQL Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="b588a-111">Example 2: Get information about an Azure SQL Database server</span></span>
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

<span data-ttu-id="b588a-112">Dieser Befehl ruft Informationen zum Azure SQL-Datenbankserver namens Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="b588a-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="b588a-113">Beispiel 3: Alle Instanzen von SQL Server im Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="b588a-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
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

<span data-ttu-id="b588a-114">Dieser Befehl ruft Informationen zu allen Azure SQL Datenbankservern im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b588a-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="b588a-115">Beispiel 4: Erhalten aller Instanzen von SQL Server, die einer Ressourcengruppe mithilfe von Filtern zugewiesen wurden</span><span class="sxs-lookup"><span data-stu-id="b588a-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
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

<span data-ttu-id="b588a-116">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern ab, die der Ressourcengruppe "ResourceGroup01" zugeordnet sind und mit "server" beginnen.</span><span class="sxs-lookup"><span data-stu-id="b588a-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="b588a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b588a-117">PARAMETERS</span></span>

### <span data-ttu-id="b588a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b588a-118">-DefaultProfile</span></span>
<span data-ttu-id="b588a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b588a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b588a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b588a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b588a-121">Gibt den Namen der Ressourcengruppe an, der Server zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b588a-121">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="b588a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b588a-122">-ServerName</span></span>
<span data-ttu-id="b588a-123">Gibt den Namen des Servers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b588a-123">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b588a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b588a-124">-Confirm</span></span>
<span data-ttu-id="b588a-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b588a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b588a-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b588a-126">-WhatIf</span></span>
<span data-ttu-id="b588a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b588a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b588a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b588a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b588a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b588a-129">CommonParameters</span></span>
<span data-ttu-id="b588a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b588a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b588a-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b588a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b588a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b588a-132">INPUTS</span></span>

### <span data-ttu-id="b588a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b588a-133">System.String</span></span>

## <span data-ttu-id="b588a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b588a-134">OUTPUTS</span></span>

### <span data-ttu-id="b588a-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b588a-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b588a-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b588a-136">NOTES</span></span>

## <span data-ttu-id="b588a-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b588a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b588a-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b588a-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="b588a-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b588a-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="b588a-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b588a-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="b588a-141">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="b588a-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


