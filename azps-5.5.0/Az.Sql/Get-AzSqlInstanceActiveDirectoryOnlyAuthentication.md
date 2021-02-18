---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175145"
---
# <span data-ttu-id="379c5-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="379c5-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="379c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379c5-102">SYNOPSIS</span></span>
<span data-ttu-id="379c5-103">Ruft nur die Azure AD-Authentifizierung für eine SQL verwaltete Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="379c5-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="379c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="379c5-104">SYNTAX</span></span>

### <span data-ttu-id="379c5-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="379c5-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379c5-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="379c5-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379c5-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="379c5-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="379c5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="379c5-108">DESCRIPTION</span></span>
<span data-ttu-id="379c5-109">Das **Cmdlet "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication"** ruft im aktuellen Abonnement nur die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für eine azureSQL-verwaltete Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="379c5-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="379c5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="379c5-110">EXAMPLES</span></span>

### <span data-ttu-id="379c5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="379c5-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="379c5-112">Dieser Befehl ruft nur die Authentifizierungsanforderung für Azure Active Directory (Azure AD) für eine azureSQL-verwaltete Instanz namens "ManagedInstance01" ab, die einer Ressourcengruppe mit dem Namen "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="379c5-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="379c5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379c5-113">PARAMETERS</span></span>

### <span data-ttu-id="379c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379c5-114">-DefaultProfile</span></span>
<span data-ttu-id="379c5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="379c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379c5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="379c5-116">-InputObject</span></span>
<span data-ttu-id="379c5-117">Das zu verwendende verwaltete Instanzobjekt.</span><span class="sxs-lookup"><span data-stu-id="379c5-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="379c5-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="379c5-118">-InstanceName</span></span>
<span data-ttu-id="379c5-119">Der Name der Azure SQL verwalteten Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="379c5-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="379c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="379c5-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="379c5-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="379c5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379c5-122">-ResourceId</span></span>
<span data-ttu-id="379c5-123">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="379c5-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="379c5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="379c5-124">-Confirm</span></span>
<span data-ttu-id="379c5-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="379c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379c5-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="379c5-126">-WhatIf</span></span>
<span data-ttu-id="379c5-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="379c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379c5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="379c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379c5-129">CommonParameters</span></span>
<span data-ttu-id="379c5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379c5-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="379c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379c5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="379c5-132">INPUTS</span></span>

### <span data-ttu-id="379c5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="379c5-133">System.String</span></span>

## <span data-ttu-id="379c5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="379c5-134">OUTPUTS</span></span>

### <span data-ttu-id="379c5-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="379c5-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="379c5-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="379c5-136">NOTES</span></span>

## <span data-ttu-id="379c5-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="379c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="379c5-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="379c5-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="379c5-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="379c5-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="379c5-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="379c5-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="379c5-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="379c5-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

