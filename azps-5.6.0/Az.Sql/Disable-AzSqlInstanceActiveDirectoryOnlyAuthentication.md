---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 013731d7c6ec414f14985dcc83cdf6cd7bf6e205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948355"
---
# <span data-ttu-id="23f96-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="23f96-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="23f96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f96-102">SYNOPSIS</span></span>
<span data-ttu-id="23f96-103">Deaktiviert die Azure AD-Authentifizierung nur für eine bestimmte SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="23f96-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="23f96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23f96-104">SYNTAX</span></span>

### <span data-ttu-id="23f96-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23f96-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f96-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f96-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f96-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f96-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f96-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23f96-108">DESCRIPTION</span></span>
<span data-ttu-id="23f96-109">Das **Cmdlet Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** deaktiviert azure Active Directory (Azure AD) nur die Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23f96-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="23f96-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23f96-110">EXAMPLES</span></span>

### <span data-ttu-id="23f96-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23f96-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="23f96-112">Mit diesem Befehl wird die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für eine verwaltete AzureSQL-Instanz mit dem Namen ManagedInstance01 deaktiviert, die einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="23f96-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="23f96-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23f96-113">PARAMETERS</span></span>

### <span data-ttu-id="23f96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f96-114">-DefaultProfile</span></span>
<span data-ttu-id="23f96-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23f96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f96-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23f96-116">-InputObject</span></span>
<span data-ttu-id="23f96-117">Das zu verwendende Objekt der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="23f96-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="23f96-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23f96-118">-InstanceName</span></span>
<span data-ttu-id="23f96-119">Der Name der Azure SQL Verwaltete Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="23f96-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="23f96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f96-120">-ResourceGroupName</span></span>
<span data-ttu-id="23f96-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="23f96-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="23f96-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23f96-122">-ResourceId</span></span>
<span data-ttu-id="23f96-123">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="23f96-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="23f96-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23f96-124">-Confirm</span></span>
<span data-ttu-id="23f96-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23f96-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f96-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f96-126">-WhatIf</span></span>
<span data-ttu-id="23f96-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23f96-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f96-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23f96-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f96-129">CommonParameters</span></span>
<span data-ttu-id="23f96-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f96-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23f96-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f96-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23f96-132">INPUTS</span></span>

### <span data-ttu-id="23f96-133">System.String</span><span class="sxs-lookup"><span data-stu-id="23f96-133">System.String</span></span>

## <span data-ttu-id="23f96-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23f96-134">OUTPUTS</span></span>

### <span data-ttu-id="23f96-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="23f96-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="23f96-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23f96-136">NOTES</span></span>

## <span data-ttu-id="23f96-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23f96-137">RELATED LINKS</span></span>

[<span data-ttu-id="23f96-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="23f96-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="23f96-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="23f96-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="23f96-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="23f96-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="23f96-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="23f96-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)