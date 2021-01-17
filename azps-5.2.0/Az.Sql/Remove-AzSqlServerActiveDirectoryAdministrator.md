---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369534"
---
# <span data-ttu-id="4f063-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4f063-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="4f063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f063-102">SYNOPSIS</span></span>
<span data-ttu-id="4f063-103">Entfernt einen Azure AD-Administrator für SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4f063-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="4f063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f063-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f063-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f063-105">DESCRIPTION</span></span>
<span data-ttu-id="4f063-106">Das **Cmdlet "Remove-AzSqlServerActiveDirectoryAdministrator"** entfernt einen Azure Active Directory (Azure AD)-Administrator für AzureSQL Server im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f063-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="4f063-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f063-107">EXAMPLES</span></span>

### <span data-ttu-id="4f063-108">Beispiel 1: Entfernen eines Administrators</span><span class="sxs-lookup"><span data-stu-id="4f063-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="4f063-109">Mit diesem Befehl wird der Azure -AD-Administrator für den Server namens Server01 entfernt, der der Ressourcengruppe "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4f063-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="4f063-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f063-110">PARAMETERS</span></span>

### <span data-ttu-id="4f063-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f063-111">-DefaultProfile</span></span>
<span data-ttu-id="4f063-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f063-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f063-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4f063-113">-Force</span></span>
<span data-ttu-id="4f063-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4f063-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f063-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f063-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f063-116">Gibt den Namen der Ressourcengruppe an, der die SQL Server wird.</span><span class="sxs-lookup"><span data-stu-id="4f063-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="4f063-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f063-117">-ServerName</span></span>
<span data-ttu-id="4f063-118">Gibt den Namen des Felds SQL Server für das dieses Cmdlet einen Administrator entfernt.</span><span class="sxs-lookup"><span data-stu-id="4f063-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="4f063-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f063-119">-Confirm</span></span>
<span data-ttu-id="4f063-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f063-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f063-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f063-121">-WhatIf</span></span>
<span data-ttu-id="4f063-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f063-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f063-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f063-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f063-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f063-124">CommonParameters</span></span>
<span data-ttu-id="4f063-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f063-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f063-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f063-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f063-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f063-127">INPUTS</span></span>

### <span data-ttu-id="4f063-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4f063-128">System.String</span></span>

## <span data-ttu-id="4f063-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f063-129">OUTPUTS</span></span>

### <span data-ttu-id="4f063-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="4f063-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="4f063-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f063-131">NOTES</span></span>

## <span data-ttu-id="4f063-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f063-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f063-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4f063-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4f063-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4f063-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4f063-135">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="4f063-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


