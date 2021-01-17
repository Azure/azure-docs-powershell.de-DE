---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468424"
---
# <span data-ttu-id="8c87b-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8c87b-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8c87b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c87b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c87b-103">Ruft Informationen zu einem Azure AD-Administrator für SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8c87b-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="8c87b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c87b-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c87b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c87b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c87b-106">Das **Cmdlet "Get-AzSqlServerActiveDirectoryAdministrator"** ruft Informationen über einen Azure Active Directory (Azure AD)-Administrator für einen AzureSQL Server im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8c87b-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="8c87b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c87b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c87b-108">Beispiel 1: Ruft Informationen zu einem Administrator für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="8c87b-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="8c87b-109">Dieser Befehl ruft Informationen über einen Azure -AD-Administrator für einen Server namens Server01 ab, der einer Ressourcengruppe mit dem Namen "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8c87b-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8c87b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c87b-110">PARAMETERS</span></span>

### <span data-ttu-id="8c87b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c87b-111">-DefaultProfile</span></span>
<span data-ttu-id="8c87b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8c87b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c87b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c87b-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c87b-114">Gibt den Namen der Ressourcengruppe an, der die SQL Server wird.</span><span class="sxs-lookup"><span data-stu-id="8c87b-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="8c87b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c87b-115">-ServerName</span></span>
<span data-ttu-id="8c87b-116">Gibt den Namen der SQL Server an, für die dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="8c87b-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="8c87b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c87b-117">-Confirm</span></span>
<span data-ttu-id="8c87b-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c87b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c87b-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c87b-119">-WhatIf</span></span>
<span data-ttu-id="8c87b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c87b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c87b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c87b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c87b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c87b-122">CommonParameters</span></span>
<span data-ttu-id="8c87b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c87b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c87b-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c87b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c87b-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c87b-125">INPUTS</span></span>

### <span data-ttu-id="8c87b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8c87b-126">System.String</span></span>

## <span data-ttu-id="8c87b-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c87b-127">OUTPUTS</span></span>

### <span data-ttu-id="8c87b-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="8c87b-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="8c87b-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c87b-129">NOTES</span></span>

## <span data-ttu-id="8c87b-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c87b-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c87b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8c87b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8c87b-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8c87b-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8c87b-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8c87b-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="8c87b-134">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="8c87b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


