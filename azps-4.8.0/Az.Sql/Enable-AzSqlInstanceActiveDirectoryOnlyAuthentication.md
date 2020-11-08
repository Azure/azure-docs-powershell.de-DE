---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165543"
---
# <span data-ttu-id="cd4dd-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cd4dd-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="cd4dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4dd-103">Aktiviert die Azure AD-Authentifizierung nur für eine bestimmte SQL-verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="cd4dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd4dd-104">SYNTAX</span></span>

### <span data-ttu-id="cd4dd-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd4dd-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4dd-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd4dd-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4dd-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd4dd-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd4dd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd4dd-108">DESCRIPTION</span></span>
<span data-ttu-id="cd4dd-109">Das Cmdlet **enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** ermöglicht die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für eine AzureSQL-verwaltete Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="cd4dd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd4dd-110">EXAMPLES</span></span>

### <span data-ttu-id="cd4dd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd4dd-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="cd4dd-112">Dieser Befehl aktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz mit dem Namen ManagedInstance01, die einer Ressourcengruppe namens ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cd4dd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd4dd-113">PARAMETERS</span></span>

### <span data-ttu-id="cd4dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4dd-114">-DefaultProfile</span></span>
<span data-ttu-id="cd4dd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd4dd-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd4dd-116">-InputObject</span></span>
<span data-ttu-id="cd4dd-117">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4dd-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cd4dd-118">-InstanceName</span></span>
<span data-ttu-id="cd4dd-119">Der Name der verwalteten Azure SQL-Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd4dd-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4dd-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cd4dd-122">-ResourceId</span></span>
<span data-ttu-id="cd4dd-123">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="cd4dd-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="cd4dd-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd4dd-124">-Confirm</span></span>
<span data-ttu-id="cd4dd-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4dd-126">-WhatIf</span></span>
<span data-ttu-id="cd4dd-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd4dd-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4dd-129">CommonParameters</span></span>
<span data-ttu-id="cd4dd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4dd-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd4dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4dd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd4dd-132">INPUTS</span></span>

### <span data-ttu-id="cd4dd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd4dd-133">System.String</span></span>

## <span data-ttu-id="cd4dd-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd4dd-134">OUTPUTS</span></span>

### <span data-ttu-id="cd4dd-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="cd4dd-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="cd4dd-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd4dd-136">NOTES</span></span>

## <span data-ttu-id="cd4dd-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd4dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd4dd-138">Deaktivieren-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cd4dd-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="cd4dd-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cd4dd-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="cd4dd-140">Satz-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cd4dd-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="cd4dd-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cd4dd-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)