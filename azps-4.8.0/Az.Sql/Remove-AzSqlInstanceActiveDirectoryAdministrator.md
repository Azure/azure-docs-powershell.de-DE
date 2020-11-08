---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174110"
---
# <span data-ttu-id="c2937-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c2937-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c2937-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2937-102">SYNOPSIS</span></span>
<span data-ttu-id="c2937-103">Entfernt eine Azure AD-Administrator für SQL-verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="c2937-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="c2937-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2937-104">SYNTAX</span></span>

### <span data-ttu-id="c2937-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2937-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2937-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2937-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2937-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2937-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2937-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2937-108">DESCRIPTION</span></span>
<span data-ttu-id="c2937-109">Das Cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** entfernt einen Azure Active Directory (Azure AD)-Administrator für AzureSQL verwaltete Instanz im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2937-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="c2937-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2937-110">EXAMPLES</span></span>

### <span data-ttu-id="c2937-111">Beispiel 1: Entfernen eines Administrators</span><span class="sxs-lookup"><span data-stu-id="c2937-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="c2937-112">Mit diesem Befehl wird der Azure AD-Administrator für die verwaltete Instanz mit dem Namen ManagedInstanceName01, die der Ressourcengruppe ResourceGroup01 zugeordnet ist, entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2937-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c2937-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2937-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="c2937-114">Mit diesem Befehl wird der Azure AD-Administrator aus dem Objekt der verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2937-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="c2937-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c2937-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="c2937-116">Mit diesem Befehl wird der Azure AD-Administrator mithilfe der Ressourcenkennung für verwaltete Instanzen entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2937-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="c2937-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2937-117">PARAMETERS</span></span>

### <span data-ttu-id="c2937-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2937-118">-DefaultProfile</span></span>
<span data-ttu-id="c2937-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2937-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2937-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c2937-120">-Force</span></span>
<span data-ttu-id="c2937-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="c2937-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c2937-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2937-122">-InputObject</span></span>
<span data-ttu-id="c2937-123">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2937-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="c2937-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2937-124">-InstanceName</span></span>
<span data-ttu-id="c2937-125">Name der verwalteten SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="c2937-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="c2937-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2937-126">-PassThru</span></span>
<span data-ttu-id="c2937-127">Definiert, ob der entfernte AD-Administrator zurückgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="c2937-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="c2937-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2937-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2937-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2937-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2937-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2937-130">-ResourceId</span></span>
<span data-ttu-id="c2937-131">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="c2937-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="c2937-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2937-132">-Confirm</span></span>
<span data-ttu-id="c2937-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2937-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2937-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2937-134">-WhatIf</span></span>
<span data-ttu-id="c2937-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2937-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2937-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2937-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2937-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2937-137">CommonParameters</span></span>
<span data-ttu-id="c2937-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2937-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2937-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2937-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2937-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2937-140">INPUTS</span></span>

### <span data-ttu-id="c2937-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2937-141">System.String</span></span>

## <span data-ttu-id="c2937-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2937-142">OUTPUTS</span></span>

### <span data-ttu-id="c2937-143">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c2937-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c2937-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2937-144">NOTES</span></span>

## <span data-ttu-id="c2937-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2937-145">RELATED LINKS</span></span>

[<span data-ttu-id="c2937-146">Satz-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c2937-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="c2937-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c2937-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
