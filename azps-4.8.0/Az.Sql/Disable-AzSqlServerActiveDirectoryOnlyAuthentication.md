---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007781"
---
# <span data-ttu-id="14fcb-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="14fcb-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="14fcb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="14fcb-103">Deaktiviert die Azure AD only-Authentifizierung für einen bestimmten SQL Server.</span><span class="sxs-lookup"><span data-stu-id="14fcb-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="14fcb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14fcb-104">SYNTAX</span></span>

### <span data-ttu-id="14fcb-105">UseResourceGroupAndServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="14fcb-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fcb-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fcb-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fcb-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fcb-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14fcb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14fcb-108">DESCRIPTION</span></span>
<span data-ttu-id="14fcb-109">Das Cmdlet **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für einen AzureSQL-Server im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14fcb-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="14fcb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14fcb-110">EXAMPLES</span></span>

### <span data-ttu-id="14fcb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14fcb-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="14fcb-112">Dieser Befehl deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für einen AzureSQL-Server mit dem Namen Server01, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14fcb-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="14fcb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="14fcb-113">PARAMETERS</span></span>

### <span data-ttu-id="14fcb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fcb-114">-DefaultProfile</span></span>
<span data-ttu-id="14fcb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14fcb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fcb-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="14fcb-116">-InputObject</span></span>
<span data-ttu-id="14fcb-117">Das zu verwendende SQL Server-Objekt.</span><span class="sxs-lookup"><span data-stu-id="14fcb-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="14fcb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fcb-118">-ResourceGroupName</span></span>
<span data-ttu-id="14fcb-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14fcb-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="14fcb-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="14fcb-120">-ResourceId</span></span>
<span data-ttu-id="14fcb-121">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="14fcb-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="14fcb-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="14fcb-122">-ServerName</span></span>
<span data-ttu-id="14fcb-123">Der Name des Azure SQL Server, in dem sich die Azure Active Directory only-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="14fcb-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="14fcb-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14fcb-124">-Confirm</span></span>
<span data-ttu-id="14fcb-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14fcb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fcb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fcb-126">-WhatIf</span></span>
<span data-ttu-id="14fcb-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14fcb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14fcb-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14fcb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fcb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fcb-129">CommonParameters</span></span>
<span data-ttu-id="14fcb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fcb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fcb-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14fcb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fcb-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14fcb-132">INPUTS</span></span>

### <span data-ttu-id="14fcb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="14fcb-133">System.String</span></span>

## <span data-ttu-id="14fcb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14fcb-134">OUTPUTS</span></span>

### <span data-ttu-id="14fcb-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="14fcb-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="14fcb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="14fcb-136">NOTES</span></span>

## <span data-ttu-id="14fcb-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14fcb-137">RELATED LINKS</span></span>

[<span data-ttu-id="14fcb-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="14fcb-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="14fcb-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="14fcb-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="14fcb-140">Satz-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="14fcb-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="14fcb-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="14fcb-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="14fcb-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="14fcb-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)