---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501370"
---
# <span data-ttu-id="6c6e9-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c6e9-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="6c6e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6e9-103">Gibt Informationen zu SQL-Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c6e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c6e9-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c6e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="6c6e9-106">Das Cmdlet " **Get-AzureRmSqlServer** " gibt Informationen zu einem oder mehreren Azure SQL-Datenbankservern zurück.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="6c6e9-107">Geben Sie den Namen eines Servers an, um Informationen nur für diesen Server anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="6c6e9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c6e9-108">EXAMPLES</span></span>

### <span data-ttu-id="6c6e9-109">Beispiel 1: Abrufen aller Instanzen von SQL Server, die einer Ressourcengruppe zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="6c6e9-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="6c6e9-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern ab, die der Ressourcengruppe ResourceGroup01 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6c6e9-111">Beispiel 2: Abrufen von Informationen zu einem Azure SQL-Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="6c6e9-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="6c6e9-112">Dieser Befehl ruft Informationen zum Azure SQL-Datenbankserver mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="6c6e9-113">Beispiel 3: Abrufen aller Instanzen von SQL Server im Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c6e9-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
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

<span data-ttu-id="6c6e9-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbankservern im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="6c6e9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c6e9-115">PARAMETERS</span></span>

### <span data-ttu-id="6c6e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6e9-116">-DefaultProfile</span></span>
<span data-ttu-id="6c6e9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c6e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c6e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c6e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="6c6e9-119">Gibt den Namen der Ressourcengruppe an, der Server zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c6e9-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="6c6e9-120">-ServerName</span></span>
<span data-ttu-id="6c6e9-121">Gibt den Namen des Servers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c6e9-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c6e9-122">-Confirm</span></span>
<span data-ttu-id="6c6e9-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c6e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c6e9-124">-WhatIf</span></span>
<span data-ttu-id="6c6e9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c6e9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c6e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6e9-127">CommonParameters</span></span>
<span data-ttu-id="6c6e9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6e9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c6e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6e9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c6e9-130">INPUTS</span></span>

### <span data-ttu-id="6c6e9-131">Keine</span><span class="sxs-lookup"><span data-stu-id="6c6e9-131">None</span></span>
<span data-ttu-id="6c6e9-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c6e9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c6e9-133">OUTPUTS</span></span>

### <span data-ttu-id="6c6e9-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6c6e9-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6c6e9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c6e9-135">NOTES</span></span>

## <span data-ttu-id="6c6e9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c6e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c6e9-137">Neu – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c6e9-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="6c6e9-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c6e9-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="6c6e9-139">Satz-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c6e9-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="6c6e9-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6c6e9-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


