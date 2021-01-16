---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293800"
---
# <span data-ttu-id="e1953-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e1953-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="e1953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1953-102">SYNOPSIS</span></span>
<span data-ttu-id="e1953-103">Aktiviert die Azure AD-Authentifizierung nur für eine bestimmte SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="e1953-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="e1953-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1953-104">SYNTAX</span></span>

### <span data-ttu-id="e1953-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1953-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1953-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1953-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1953-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1953-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1953-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1953-108">DESCRIPTION</span></span>
<span data-ttu-id="e1953-109">Das **Cmdlet "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication"** aktiviert die Authentifizierungsanforderung für Azure Active Directory (Azure AD) nur für eine azureSQL-verwaltete Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1953-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="e1953-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1953-110">EXAMPLES</span></span>

### <span data-ttu-id="e1953-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1953-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="e1953-112">Dieser Befehl aktiviert nur die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für eine azureSQL-verwaltete Instanz namens "ManagedInstance01", die einer Ressourcengruppe namens "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e1953-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e1953-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1953-113">PARAMETERS</span></span>

### <span data-ttu-id="e1953-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1953-114">-DefaultProfile</span></span>
<span data-ttu-id="e1953-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1953-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1953-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1953-116">-InputObject</span></span>
<span data-ttu-id="e1953-117">Das zu verwendende verwaltete Instanzobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1953-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="e1953-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e1953-118">-InstanceName</span></span>
<span data-ttu-id="e1953-119">Der Name der Azure SQL verwalteten Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="e1953-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="e1953-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1953-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1953-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1953-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e1953-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1953-122">-ResourceId</span></span>
<span data-ttu-id="e1953-123">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="e1953-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="e1953-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1953-124">-Confirm</span></span>
<span data-ttu-id="e1953-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1953-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1953-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1953-126">-WhatIf</span></span>
<span data-ttu-id="e1953-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1953-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1953-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1953-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1953-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1953-129">CommonParameters</span></span>
<span data-ttu-id="e1953-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1953-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1953-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1953-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1953-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1953-132">INPUTS</span></span>

### <span data-ttu-id="e1953-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e1953-133">System.String</span></span>

## <span data-ttu-id="e1953-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1953-134">OUTPUTS</span></span>

### <span data-ttu-id="e1953-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="e1953-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="e1953-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1953-136">NOTES</span></span>

## <span data-ttu-id="e1953-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1953-137">RELATED LINKS</span></span>

[<span data-ttu-id="e1953-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e1953-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="e1953-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e1953-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="e1953-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e1953-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e1953-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e1953-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)