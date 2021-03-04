---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0a06eae51b074cefb74b2ef3a175a056cc52ff84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949888"
---
# <span data-ttu-id="b3985-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3985-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="b3985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3985-102">SYNOPSIS</span></span>
<span data-ttu-id="b3985-103">Ruft nur azure AD-Authentifizierung für eine bestimmte verwaltete SQL ab.</span><span class="sxs-lookup"><span data-stu-id="b3985-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="b3985-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3985-104">SYNTAX</span></span>

### <span data-ttu-id="b3985-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3985-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3985-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3985-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3985-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3985-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3985-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3985-108">DESCRIPTION</span></span>
<span data-ttu-id="b3985-109">Das **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication-Cmdlet** ruft azure Active Directory (Azure AD) nur die Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b3985-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="b3985-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3985-110">EXAMPLES</span></span>

### <span data-ttu-id="b3985-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3985-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="b3985-112">Dieser Befehl ruft azure active Directory (Azure AD) nur die Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz mit dem Namen ManagedInstance01 ab, die einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b3985-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b3985-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b3985-113">PARAMETERS</span></span>

### <span data-ttu-id="b3985-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3985-114">-DefaultProfile</span></span>
<span data-ttu-id="b3985-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3985-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3985-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3985-116">-InputObject</span></span>
<span data-ttu-id="b3985-117">Das zu verwendende Objekt der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="b3985-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="b3985-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b3985-118">-InstanceName</span></span>
<span data-ttu-id="b3985-119">Der Name der Azure SQL Verwaltete Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="b3985-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="b3985-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3985-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3985-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3985-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="b3985-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3985-122">-ResourceId</span></span>
<span data-ttu-id="b3985-123">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="b3985-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="b3985-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3985-124">-Confirm</span></span>
<span data-ttu-id="b3985-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3985-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3985-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3985-126">-WhatIf</span></span>
<span data-ttu-id="b3985-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3985-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3985-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3985-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3985-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3985-129">CommonParameters</span></span>
<span data-ttu-id="b3985-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3985-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3985-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3985-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3985-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3985-132">INPUTS</span></span>

### <span data-ttu-id="b3985-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b3985-133">System.String</span></span>

## <span data-ttu-id="b3985-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3985-134">OUTPUTS</span></span>

### <span data-ttu-id="b3985-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="b3985-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="b3985-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b3985-136">NOTES</span></span>

## <span data-ttu-id="b3985-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b3985-137">RELATED LINKS</span></span>

[<span data-ttu-id="b3985-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3985-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="b3985-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3985-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="b3985-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3985-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="b3985-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3985-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

