---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 228dbf358a24cfb1942140dcf5d87dae8960bb00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931659"
---
# <span data-ttu-id="9ff72-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9ff72-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="9ff72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff72-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff72-103">Deaktiviert die Azure AD-Authentifizierung nur für einen bestimmten SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ff72-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="9ff72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ff72-104">SYNTAX</span></span>

### <span data-ttu-id="9ff72-105">UseResourceGroupAndServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ff72-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff72-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ff72-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff72-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ff72-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff72-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ff72-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff72-109">Das **Cmdlet Disable-AzSqlServerActiveDirectoryOnlyAuthentication** deaktiviert azure Active Directory (Azure AD) nur die Authentifizierungsanforderung für einen AzureSQL Server im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ff72-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="9ff72-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ff72-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff72-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ff72-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="9ff72-112">Mit diesem Befehl wird die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für einen AzureSQL-Server namens Server01 deaktiviert, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9ff72-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9ff72-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ff72-113">PARAMETERS</span></span>

### <span data-ttu-id="9ff72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff72-114">-DefaultProfile</span></span>
<span data-ttu-id="9ff72-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ff72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff72-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ff72-116">-InputObject</span></span>
<span data-ttu-id="9ff72-117">Das SQL zu verwendende Serverobjekt.</span><span class="sxs-lookup"><span data-stu-id="9ff72-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff72-118">-ResourceGroupName</span></span>
<span data-ttu-id="9ff72-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ff72-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff72-120">-ResourceId</span></span>
<span data-ttu-id="9ff72-121">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="9ff72-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="9ff72-122">-ServerName</span></span>
<span data-ttu-id="9ff72-123">Der Name der Azure-SQL Server azure Active Directory-Authentifizierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ff72-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ff72-124">-Confirm</span></span>
<span data-ttu-id="9ff72-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ff72-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff72-126">-WhatIf</span></span>
<span data-ttu-id="9ff72-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ff72-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff72-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ff72-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff72-129">CommonParameters</span></span>
<span data-ttu-id="9ff72-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff72-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff72-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff72-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ff72-132">INPUTS</span></span>

### <span data-ttu-id="9ff72-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9ff72-133">System.String</span></span>

## <span data-ttu-id="9ff72-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ff72-134">OUTPUTS</span></span>

### <span data-ttu-id="9ff72-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="9ff72-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="9ff72-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ff72-136">NOTES</span></span>

## <span data-ttu-id="9ff72-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ff72-137">RELATED LINKS</span></span>

[<span data-ttu-id="9ff72-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9ff72-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="9ff72-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="9ff72-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="9ff72-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9ff72-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="9ff72-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9ff72-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="9ff72-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="9ff72-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)