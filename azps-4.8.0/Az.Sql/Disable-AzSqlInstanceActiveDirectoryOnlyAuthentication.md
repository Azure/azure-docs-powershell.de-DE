---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165545"
---
# <span data-ttu-id="80978-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="80978-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="80978-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80978-102">SYNOPSIS</span></span>
<span data-ttu-id="80978-103">Deaktiviert die Azure AD-Authentifizierung nur für eine bestimmte SQL-verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="80978-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="80978-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80978-104">SYNTAX</span></span>

### <span data-ttu-id="80978-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="80978-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80978-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80978-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80978-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80978-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80978-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80978-108">DESCRIPTION</span></span>
<span data-ttu-id="80978-109">Das Cmdlet **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für eine AzureSQL-verwaltete Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80978-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="80978-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80978-110">EXAMPLES</span></span>

### <span data-ttu-id="80978-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80978-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="80978-112">Dieser Befehl deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz mit dem Namen ManagedInstance01, die einer Ressourcengruppe namens ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="80978-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="80978-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="80978-113">PARAMETERS</span></span>

### <span data-ttu-id="80978-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80978-114">-DefaultProfile</span></span>
<span data-ttu-id="80978-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80978-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80978-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80978-116">-InputObject</span></span>
<span data-ttu-id="80978-117">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="80978-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="80978-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="80978-118">-InstanceName</span></span>
<span data-ttu-id="80978-119">Der Name der verwalteten Azure SQL-Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="80978-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="80978-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80978-120">-ResourceGroupName</span></span>
<span data-ttu-id="80978-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80978-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="80978-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="80978-122">-ResourceId</span></span>
<span data-ttu-id="80978-123">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="80978-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="80978-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80978-124">-Confirm</span></span>
<span data-ttu-id="80978-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80978-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80978-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80978-126">-WhatIf</span></span>
<span data-ttu-id="80978-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80978-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80978-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80978-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80978-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80978-129">CommonParameters</span></span>
<span data-ttu-id="80978-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80978-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80978-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80978-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80978-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80978-132">INPUTS</span></span>

### <span data-ttu-id="80978-133">System. String</span><span class="sxs-lookup"><span data-stu-id="80978-133">System.String</span></span>

## <span data-ttu-id="80978-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80978-134">OUTPUTS</span></span>

### <span data-ttu-id="80978-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="80978-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="80978-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="80978-136">NOTES</span></span>

## <span data-ttu-id="80978-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80978-137">RELATED LINKS</span></span>

[<span data-ttu-id="80978-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="80978-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="80978-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="80978-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="80978-140">Satz-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="80978-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="80978-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="80978-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)