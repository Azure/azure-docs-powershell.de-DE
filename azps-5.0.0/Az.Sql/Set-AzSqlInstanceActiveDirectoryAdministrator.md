---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175391"
---
# <span data-ttu-id="21066-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21066-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="21066-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21066-102">SYNOPSIS</span></span>
<span data-ttu-id="21066-103">Stellt eine Azure AD-Administrator für SQL verwaltete Instanz dar.</span><span class="sxs-lookup"><span data-stu-id="21066-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="21066-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21066-104">SYNTAX</span></span>

### <span data-ttu-id="21066-105">UseResourceGroupAndInstanceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21066-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21066-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21066-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21066-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21066-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21066-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21066-108">DESCRIPTION</span></span>
<span data-ttu-id="21066-109">Das Cmdlet " **Satz-AzSqlInstanceActiveDirectoryAdministrator" stellt** einen Azure Active Directory (Azure AD)-Administrator für AzureSQL verwaltete Instanz im aktuellen Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="21066-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="21066-110">Sie können jeweils nur einen Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="21066-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="21066-111">Die folgenden Mitglieder von Azure AD können als Administrator für die SQL-verwaltete Instanz bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="21066-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="21066-112">Native Member von Azure AD</span><span class="sxs-lookup"><span data-stu-id="21066-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="21066-113">Verbundmitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="21066-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="21066-114">Azure AD Groups, die als Sicherheitsgruppen erstellt wurden, die Mitglieder aus anderen Azure ADS importiert haben, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21066-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="21066-115">Microsoft-Konten, wie Sie in den Outlook.com-, hotmail.com-oder Live.com-Domänen vorliegen, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21066-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="21066-116">Andere Gastkonten, beispielsweise die in der gmail.com-oder Yahoo.com-Domäne, werden nicht als Administratoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21066-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="21066-117">Wir empfehlen, dass Sie eine dedizierte Azure Ad-Gruppe als Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="21066-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="21066-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21066-118">EXAMPLES</span></span>

### <span data-ttu-id="21066-119">Beispiel 1: Bereitstelleneiner Administratorgruppe für eine verwaltete Instanz, die der Ressourcengruppe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="21066-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="21066-120">Dieser Befehl stellt eine Azure AD-Administratorgruppe namens DBAs für die verwaltete Instanz mit dem Namen ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="21066-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="21066-121">Dieser Server ist dem Ressourcengruppen-ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="21066-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="21066-122">Beispiel 2: Bereitstellen eines Administratorbenutzers mithilfe eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="21066-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="21066-123">Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator vom verwalteten Instanzen Objekt abgewickelt.</span><span class="sxs-lookup"><span data-stu-id="21066-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="21066-124">Beispiel 3: Bereitstellen eines Administrators mit Ressourcenbezeichner für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="21066-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="21066-125">Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator mithilfe der Ressourcen-ID für verwaltete Instanzen angegeben.</span><span class="sxs-lookup"><span data-stu-id="21066-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="21066-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="21066-126">PARAMETERS</span></span>

### <span data-ttu-id="21066-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21066-127">-DefaultProfile</span></span>
<span data-ttu-id="21066-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21066-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21066-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21066-129">-DisplayName</span></span>
<span data-ttu-id="21066-130">Gibt den Anzeigenamen des Benutzers oder der Gruppe an, dem Sie Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="21066-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="21066-131">Dieser Anzeigename muss in dem Active Directory vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="21066-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="21066-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21066-132">-InputObject</span></span>
<span data-ttu-id="21066-133">Das zu verwendende verwaltete Instanzen Objekt.</span><span class="sxs-lookup"><span data-stu-id="21066-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="21066-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="21066-134">-InstanceName</span></span>
<span data-ttu-id="21066-135">Name der verwalteten SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="21066-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="21066-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="21066-136">-ObjectId</span></span>
<span data-ttu-id="21066-137">Gibt die Objekt-ID des Benutzers oder der Gruppe in Azure Active Directory an, für den Berechtigungen erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21066-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="21066-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21066-138">-ResourceGroupName</span></span>
<span data-ttu-id="21066-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21066-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="21066-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="21066-140">-ResourceId</span></span>
<span data-ttu-id="21066-141">Die Ressourcen-ID der zu verwendenden Instanz</span><span class="sxs-lookup"><span data-stu-id="21066-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="21066-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21066-142">-Confirm</span></span>
<span data-ttu-id="21066-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21066-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21066-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21066-144">-WhatIf</span></span>
<span data-ttu-id="21066-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21066-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21066-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21066-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21066-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21066-147">CommonParameters</span></span>
<span data-ttu-id="21066-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21066-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21066-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21066-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21066-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21066-150">INPUTS</span></span>

### <span data-ttu-id="21066-151">System. String</span><span class="sxs-lookup"><span data-stu-id="21066-151">System.String</span></span>

### <span data-ttu-id="21066-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="21066-152">System.Guid</span></span>

## <span data-ttu-id="21066-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21066-153">OUTPUTS</span></span>

### <span data-ttu-id="21066-154">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="21066-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="21066-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="21066-155">NOTES</span></span>

## <span data-ttu-id="21066-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21066-156">RELATED LINKS</span></span>

[<span data-ttu-id="21066-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21066-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="21066-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21066-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
