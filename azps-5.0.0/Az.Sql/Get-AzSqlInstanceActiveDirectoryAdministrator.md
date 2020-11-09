---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296638"
---
# <span data-ttu-id="a7f46-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7f46-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a7f46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7f46-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f46-103">Ruft Informationen zu einem Azure AD-Administrator für SQL-verwaltete Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="a7f46-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="a7f46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f46-104">SYNTAX</span></span>

### <span data-ttu-id="a7f46-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7f46-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7f46-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7f46-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7f46-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7f46-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7f46-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7f46-108">DESCRIPTION</span></span>
<span data-ttu-id="a7f46-109">Das Cmdlet " **Get-AzSqlInstanceActiveDirectoryAdministrator** " Ruft Informationen zu einem Azure Active Directory (Azure AD)-Administrator für eine AzureSQL-verwaltete Instanz im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a7f46-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="a7f46-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7f46-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f46-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7f46-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7f46-112">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator für eine verwaltete Instanz mit dem Namen ManagedInstance01 ab, die einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7f46-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="a7f46-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a7f46-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7f46-114">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator aus einem verwalteten Instanzen Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="a7f46-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="a7f46-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a7f46-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7f46-116">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator mithilfe der Ressourcen-ID für verwaltete Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="a7f46-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="a7f46-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f46-117">PARAMETERS</span></span>

### <span data-ttu-id="a7f46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f46-118">-DefaultProfile</span></span>
<span data-ttu-id="a7f46-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7f46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f46-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7f46-120">-InputObject</span></span>
<span data-ttu-id="a7f46-121">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7f46-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="a7f46-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a7f46-122">-InstanceName</span></span>
<span data-ttu-id="a7f46-123">Name der verwalteten SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="a7f46-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="a7f46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f46-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7f46-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7f46-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7f46-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a7f46-126">-ResourceId</span></span>
<span data-ttu-id="a7f46-127">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="a7f46-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a7f46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f46-128">CommonParameters</span></span>
<span data-ttu-id="a7f46-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f46-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7f46-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f46-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7f46-131">INPUTS</span></span>

### <span data-ttu-id="a7f46-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f46-132">System.String</span></span>

## <span data-ttu-id="a7f46-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7f46-133">OUTPUTS</span></span>

### <span data-ttu-id="a7f46-134">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a7f46-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a7f46-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7f46-135">NOTES</span></span>

## <span data-ttu-id="a7f46-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7f46-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7f46-137">Satz-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7f46-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="a7f46-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7f46-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
