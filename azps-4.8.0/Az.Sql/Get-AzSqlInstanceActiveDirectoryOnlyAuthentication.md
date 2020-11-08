---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173465"
---
# <span data-ttu-id="bd55f-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="bd55f-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="bd55f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd55f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd55f-103">Ruft nur die Azure AD-Authentifizierung für eine bestimmte verwaltete SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="bd55f-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="bd55f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd55f-104">SYNTAX</span></span>

### <span data-ttu-id="bd55f-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd55f-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd55f-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd55f-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd55f-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd55f-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd55f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd55f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd55f-109">Das Cmdlet " **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** " ruft nur die Azure Active Directory (Azure AD)-Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bd55f-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="bd55f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd55f-110">EXAMPLES</span></span>

### <span data-ttu-id="bd55f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd55f-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="bd55f-112">Dieser Befehl ruft nur die Azure Active Directory (Azure AD)-Authentifizierungsanforderung für eine verwaltete AzureSQL-Instanz mit dem Namen ManagedInstance01 ab, die einer Ressourcengruppe namens ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bd55f-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="bd55f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd55f-113">PARAMETERS</span></span>

### <span data-ttu-id="bd55f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd55f-114">-DefaultProfile</span></span>
<span data-ttu-id="bd55f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd55f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd55f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd55f-116">-InputObject</span></span>
<span data-ttu-id="bd55f-117">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd55f-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="bd55f-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bd55f-118">-InstanceName</span></span>
<span data-ttu-id="bd55f-119">Der Name der verwalteten Azure SQL-Instanz, in der sich nur die Azure Active Directory-Authentifizierung befindet.</span><span class="sxs-lookup"><span data-stu-id="bd55f-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="bd55f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd55f-120">-ResourceGroupName</span></span>
<span data-ttu-id="bd55f-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bd55f-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd55f-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bd55f-122">-ResourceId</span></span>
<span data-ttu-id="bd55f-123">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="bd55f-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="bd55f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd55f-124">-Confirm</span></span>
<span data-ttu-id="bd55f-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd55f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd55f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd55f-126">-WhatIf</span></span>
<span data-ttu-id="bd55f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd55f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd55f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd55f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd55f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd55f-129">CommonParameters</span></span>
<span data-ttu-id="bd55f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd55f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd55f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd55f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd55f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd55f-132">INPUTS</span></span>

### <span data-ttu-id="bd55f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bd55f-133">System.String</span></span>

## <span data-ttu-id="bd55f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd55f-134">OUTPUTS</span></span>

### <span data-ttu-id="bd55f-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="bd55f-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="bd55f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd55f-136">NOTES</span></span>

## <span data-ttu-id="bd55f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd55f-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd55f-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="bd55f-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="bd55f-139">Deaktivieren-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="bd55f-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="bd55f-140">Satz-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bd55f-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="bd55f-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bd55f-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

