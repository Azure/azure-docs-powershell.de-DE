---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: a8c748e2d37dbb4759df27b56b37719bcbb2babf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950544"
---
# <span data-ttu-id="88ac4-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ac4-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="88ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="88ac4-103">Bietet einen Azure AD-Administrator für SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="88ac4-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="88ac4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88ac4-104">SYNTAX</span></span>

### <span data-ttu-id="88ac4-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="88ac4-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac4-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac4-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88ac4-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac4-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ac4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="88ac4-109">Das **Cmdlet Set-AzSqlInstanceActiveDirectoryAdministrator** stellt einen Azure Active Directory (Azure AD)-Administrator für die verwaltete AzureSQL-Instanz im aktuellen Abonnement bereit.</span><span class="sxs-lookup"><span data-stu-id="88ac4-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="88ac4-110">Sie können immer nur einen Administrator gleichzeitig bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="88ac4-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="88ac4-111">Die folgenden Mitglieder von Azure AD können als Administrator für verwaltete SQL bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="88ac4-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="88ac4-112">Native Mitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="88ac4-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="88ac4-113">Verbundmitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="88ac4-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="88ac4-114">Azure AD-Gruppen, die als Sicherheitsgruppen erstellt wurden Importierte Mitglieder aus anderen Azure ADs werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88ac4-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="88ac4-115">Microsoft-Konten, z. B. Outlook.com, Hotmail.com oder Live.com Domänen, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88ac4-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="88ac4-116">Andere Gastkonten, z. B. in den domänen Gmail.com oder Yahoo.com, werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88ac4-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="88ac4-117">Es wird empfohlen, eine dedizierte Azure AD-Gruppe als Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="88ac4-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="88ac4-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88ac4-118">EXAMPLES</span></span>

### <span data-ttu-id="88ac4-119">Beispiel 1: Bereitstellen einer Administratorgruppe für eine verwaltete Instanz, die einer Ressourcengruppe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="88ac4-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="88ac4-120">Dieser Befehl enthält eine Azure AD-Administratorgruppe mit dem Namen DBAs für die verwaltete Instanz mit dem Namen ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="88ac4-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="88ac4-121">Dieser Server ist der Ressourcengruppe ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="88ac4-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="88ac4-122">Beispiel 2: Bereitstellen eines Administratorbenutzers mit verwalteten Instanzobjekten</span><span class="sxs-lookup"><span data-stu-id="88ac4-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="88ac4-123">Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator des verwalteten Instanzobjekts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="88ac4-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="88ac4-124">Beispiel 3: Bereitstellen eines Administrators mithilfe des Ressourcenbezeichners für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="88ac4-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="88ac4-125">Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator bereitgestellt, der den Ressourcenbezeichner für verwaltete Instanzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="88ac4-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="88ac4-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88ac4-126">PARAMETERS</span></span>

### <span data-ttu-id="88ac4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ac4-127">-DefaultProfile</span></span>
<span data-ttu-id="88ac4-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88ac4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ac4-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="88ac4-129">-DisplayName</span></span>
<span data-ttu-id="88ac4-130">Gibt den Anzeigenamen des Benutzers oder der Gruppe an, für den Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="88ac4-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="88ac4-131">Dieser Anzeigename muss im Active Directory vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="88ac4-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88ac4-132">-InputObject</span></span>
<span data-ttu-id="88ac4-133">Das zu verwendende Objekt der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="88ac4-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="88ac4-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="88ac4-134">-InstanceName</span></span>
<span data-ttu-id="88ac4-135">SQL Namen der verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="88ac4-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="88ac4-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="88ac4-136">-ObjectId</span></span>
<span data-ttu-id="88ac4-137">Gibt die Objekt-ID des Benutzers oder der Gruppe in Azure Active Directory an, für die Berechtigungen erteilt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="88ac4-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ac4-138">-ResourceGroupName</span></span>
<span data-ttu-id="88ac4-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88ac4-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="88ac4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88ac4-140">-ResourceId</span></span>
<span data-ttu-id="88ac4-141">Die Ressourcen-ID der zu verwendende Instanz</span><span class="sxs-lookup"><span data-stu-id="88ac4-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="88ac4-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88ac4-142">-Confirm</span></span>
<span data-ttu-id="88ac4-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88ac4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ac4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ac4-144">-WhatIf</span></span>
<span data-ttu-id="88ac4-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88ac4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ac4-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88ac4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ac4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ac4-147">CommonParameters</span></span>
<span data-ttu-id="88ac4-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ac4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ac4-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ac4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ac4-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88ac4-150">INPUTS</span></span>

### <span data-ttu-id="88ac4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="88ac4-151">System.String</span></span>

### <span data-ttu-id="88ac4-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="88ac4-152">System.Guid</span></span>

## <span data-ttu-id="88ac4-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88ac4-153">OUTPUTS</span></span>

### <span data-ttu-id="88ac4-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="88ac4-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="88ac4-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88ac4-155">NOTES</span></span>

## <span data-ttu-id="88ac4-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88ac4-156">RELATED LINKS</span></span>

[<span data-ttu-id="88ac4-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ac4-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="88ac4-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ac4-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
