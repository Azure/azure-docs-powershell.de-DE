---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468504"
---
# <span data-ttu-id="13034-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="13034-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="13034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13034-102">SYNOPSIS</span></span>
<span data-ttu-id="13034-103">Ruft Informationen zu einem Azure AD-Administrator für eine verwaltete SQL ab.</span><span class="sxs-lookup"><span data-stu-id="13034-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="13034-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13034-104">SYNTAX</span></span>

### <span data-ttu-id="13034-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="13034-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13034-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13034-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13034-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13034-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13034-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13034-108">DESCRIPTION</span></span>
<span data-ttu-id="13034-109">Das **Cmdlet "Get-AzSqlInstanceActiveDirectoryAdministrator"** ruft Informationen über einen Azure Active Directory (Azure AD)-Administrator für eine verwaltete AzureSQL-Instanz im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="13034-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="13034-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13034-110">EXAMPLES</span></span>

### <span data-ttu-id="13034-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13034-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="13034-112">Dieser Befehl ruft Informationen über einen Azure -AD-Administrator für eine verwaltete Instanz namens "ManagedInstance01" ab, die einer Ressourcengruppe mit dem Namen "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="13034-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="13034-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="13034-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="13034-114">Dieser Befehl ruft Informationen über einen Azure -AD-Administrator aus einem verwalteten Instanzobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="13034-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="13034-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="13034-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="13034-116">Dieser Befehl ruft Informationen über einen Azure AD-Administrator mit dem Ressourcenbezeichner für verwaltete Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="13034-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="13034-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13034-117">PARAMETERS</span></span>

### <span data-ttu-id="13034-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13034-118">-DefaultProfile</span></span>
<span data-ttu-id="13034-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13034-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13034-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13034-120">-InputObject</span></span>
<span data-ttu-id="13034-121">Das zu verwendende verwaltete Instanzobjekt.</span><span class="sxs-lookup"><span data-stu-id="13034-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="13034-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="13034-122">-InstanceName</span></span>
<span data-ttu-id="13034-123">SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="13034-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="13034-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13034-124">-ResourceGroupName</span></span>
<span data-ttu-id="13034-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13034-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="13034-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13034-126">-ResourceId</span></span>
<span data-ttu-id="13034-127">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="13034-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="13034-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13034-128">CommonParameters</span></span>
<span data-ttu-id="13034-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13034-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13034-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13034-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13034-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13034-131">INPUTS</span></span>

### <span data-ttu-id="13034-132">System.String</span><span class="sxs-lookup"><span data-stu-id="13034-132">System.String</span></span>

## <span data-ttu-id="13034-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13034-133">OUTPUTS</span></span>

### <span data-ttu-id="13034-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="13034-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="13034-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13034-135">NOTES</span></span>

## <span data-ttu-id="13034-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13034-136">RELATED LINKS</span></span>

[<span data-ttu-id="13034-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="13034-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="13034-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="13034-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
