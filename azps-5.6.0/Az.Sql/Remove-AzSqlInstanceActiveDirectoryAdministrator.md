---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 16a2250941ba0e28d40648ed2cd69fee7ffefc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920187"
---
# <span data-ttu-id="afc17-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="afc17-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="afc17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc17-102">SYNOPSIS</span></span>
<span data-ttu-id="afc17-103">Entfernt einen Azure AD-Administrator für SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="afc17-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="afc17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afc17-104">SYNTAX</span></span>

### <span data-ttu-id="afc17-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afc17-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc17-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc17-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc17-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc17-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc17-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afc17-108">DESCRIPTION</span></span>
<span data-ttu-id="afc17-109">Das **Cmdlet Remove-AzSqlInstanceActiveDirectoryAdministrator** entfernt einen Azure Active Directory (Azure AD)-Administrator für verwaltete AzureSQL-Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afc17-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="afc17-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afc17-110">EXAMPLES</span></span>

### <span data-ttu-id="afc17-111">Beispiel 1: Entfernen eines Administrators</span><span class="sxs-lookup"><span data-stu-id="afc17-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="afc17-112">Mit diesem Befehl wird der Azure AD-Administrator für die verwaltete Instanz mit dem Namen ManagedInstanceName01 entfernt, die der Ressourcengruppe ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="afc17-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="afc17-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="afc17-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="afc17-114">Mit diesem Befehl wird der Azure AD-Administrator aus dem Objekt der verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="afc17-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="afc17-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="afc17-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="afc17-116">Mit diesem Befehl wird der Azure AD-Administrator mit dem Ressourcenbezeichner für verwaltete Instanzen entfernt.</span><span class="sxs-lookup"><span data-stu-id="afc17-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="afc17-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afc17-117">PARAMETERS</span></span>

### <span data-ttu-id="afc17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc17-118">-DefaultProfile</span></span>
<span data-ttu-id="afc17-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afc17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc17-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="afc17-120">-Force</span></span>
<span data-ttu-id="afc17-121">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="afc17-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc17-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afc17-122">-InputObject</span></span>
<span data-ttu-id="afc17-123">Das zu verwendende Objekt der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="afc17-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="afc17-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="afc17-124">-InstanceName</span></span>
<span data-ttu-id="afc17-125">SQL Namen der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="afc17-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="afc17-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afc17-126">-PassThru</span></span>
<span data-ttu-id="afc17-127">Definiert, ob der entfernte AD-Administrator zurückgeben soll</span><span class="sxs-lookup"><span data-stu-id="afc17-127">Defines whether to return the removed AD administrator</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc17-128">-ResourceGroupName</span></span>
<span data-ttu-id="afc17-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="afc17-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="afc17-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc17-130">-ResourceId</span></span>
<span data-ttu-id="afc17-131">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="afc17-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="afc17-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afc17-132">-Confirm</span></span>
<span data-ttu-id="afc17-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afc17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc17-134">-WhatIf</span></span>
<span data-ttu-id="afc17-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afc17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc17-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afc17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc17-137">CommonParameters</span></span>
<span data-ttu-id="afc17-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc17-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afc17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc17-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afc17-140">INPUTS</span></span>

### <span data-ttu-id="afc17-141">System.String</span><span class="sxs-lookup"><span data-stu-id="afc17-141">System.String</span></span>

## <span data-ttu-id="afc17-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afc17-142">OUTPUTS</span></span>

### <span data-ttu-id="afc17-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="afc17-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="afc17-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afc17-144">NOTES</span></span>

## <span data-ttu-id="afc17-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afc17-145">RELATED LINKS</span></span>

[<span data-ttu-id="afc17-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="afc17-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="afc17-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="afc17-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
