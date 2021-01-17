---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375316"
---
# <span data-ttu-id="07d94-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="07d94-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="07d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d94-102">SYNOPSIS</span></span>
<span data-ttu-id="07d94-103">Deaktiviert nur die Azure AD-Authentifizierung für eine bestimmte SQL Server.</span><span class="sxs-lookup"><span data-stu-id="07d94-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="07d94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07d94-104">SYNTAX</span></span>

### <span data-ttu-id="07d94-105">UseResourceGroupAndServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07d94-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07d94-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07d94-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07d94-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07d94-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07d94-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07d94-108">DESCRIPTION</span></span>
<span data-ttu-id="07d94-109">Das **Cmdlet "Disable-AzSqlServerActiveDirectoryOnlyAuthentication"** deaktiviert im aktuellen Abonnement nur die Authentifizierungsanforderung für Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="07d94-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="07d94-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07d94-110">EXAMPLES</span></span>

### <span data-ttu-id="07d94-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07d94-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="07d94-112">Mit diesem Befehl wird die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für einen AzureSQL-Server namens Server01 deaktiviert, der einer Ressourcengruppe mit dem Namen "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07d94-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="07d94-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07d94-113">PARAMETERS</span></span>

### <span data-ttu-id="07d94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d94-114">-DefaultProfile</span></span>
<span data-ttu-id="07d94-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07d94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07d94-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d94-116">-InputObject</span></span>
<span data-ttu-id="07d94-117">Das SQL server-Objekt, das Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="07d94-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="07d94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d94-118">-ResourceGroupName</span></span>
<span data-ttu-id="07d94-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07d94-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="07d94-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07d94-120">-ResourceId</span></span>
<span data-ttu-id="07d94-121">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="07d94-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="07d94-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07d94-122">-ServerName</span></span>
<span data-ttu-id="07d94-123">Der Name des Azure SQL Server, in dem nur die Azure Active Directory-Authentifizierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="07d94-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="07d94-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07d94-124">-Confirm</span></span>
<span data-ttu-id="07d94-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07d94-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d94-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07d94-126">-WhatIf</span></span>
<span data-ttu-id="07d94-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07d94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d94-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07d94-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07d94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d94-129">CommonParameters</span></span>
<span data-ttu-id="07d94-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d94-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07d94-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d94-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07d94-132">INPUTS</span></span>

### <span data-ttu-id="07d94-133">System.String</span><span class="sxs-lookup"><span data-stu-id="07d94-133">System.String</span></span>

## <span data-ttu-id="07d94-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07d94-134">OUTPUTS</span></span>

### <span data-ttu-id="07d94-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="07d94-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="07d94-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07d94-136">NOTES</span></span>

## <span data-ttu-id="07d94-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07d94-137">RELATED LINKS</span></span>

[<span data-ttu-id="07d94-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="07d94-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="07d94-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="07d94-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="07d94-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="07d94-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="07d94-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="07d94-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="07d94-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="07d94-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)