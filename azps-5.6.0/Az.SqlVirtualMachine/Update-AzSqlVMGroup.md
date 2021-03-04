---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 04a75ec50f985bb1cea0266c077946adbdab4f65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943291"
---
# <span data-ttu-id="4282d-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="4282d-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="4282d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4282d-102">SYNOPSIS</span></span>
<span data-ttu-id="4282d-103">Aktualisiert eine Sql Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4282d-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="4282d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4282d-104">SYNTAX</span></span>

### <span data-ttu-id="4282d-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="4282d-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4282d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4282d-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4282d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4282d-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4282d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4282d-108">DESCRIPTION</span></span>
<span data-ttu-id="4282d-109">Das Update-AzSqlVMGroup cmdlet aktualisiert eine Sql Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4282d-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="4282d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4282d-110">EXAMPLES</span></span>

### <span data-ttu-id="4282d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4282d-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="4282d-112">Aktualisiert die Tags einer Gruppe virtueller Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="4282d-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="4282d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4282d-113">PARAMETERS</span></span>

### <span data-ttu-id="4282d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4282d-114">-AsJob</span></span>
<span data-ttu-id="4282d-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4282d-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4282d-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="4282d-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="4282d-117">Name, der zum Erstellen von Clustern verwendet wird</span><span class="sxs-lookup"><span data-stu-id="4282d-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="4282d-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="4282d-119">Name, der für den Betrieb von Clustern verwendet wird</span><span class="sxs-lookup"><span data-stu-id="4282d-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4282d-120">-DefaultProfile</span></span>
<span data-ttu-id="4282d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4282d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4282d-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="4282d-122">-DomainFqdn</span></span>
<span data-ttu-id="4282d-123">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="4282d-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="4282d-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="4282d-125">Optionaler Pfad für fileshare witness</span><span class="sxs-lookup"><span data-stu-id="4282d-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4282d-126">-InputObject</span></span>
<span data-ttu-id="4282d-127">SQL virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="4282d-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4282d-128">-Name</span></span>
<span data-ttu-id="4282d-129">SQL namen der Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="4282d-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="4282d-130">-OuPath</span></span>
<span data-ttu-id="4282d-131">Pfad der Organisationseinheit, in dem die Knoten und der Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="4282d-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4282d-132">-ResourceGroupName</span></span>
<span data-ttu-id="4282d-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4282d-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4282d-134">-ResourceId</span></span>
<span data-ttu-id="4282d-135">SQL der Ressourcen-ID der Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="4282d-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="4282d-136">-SqlServiceAccount</span></span>
<span data-ttu-id="4282d-137">Name, unter dem SQL dienst auf allen teilnehmenden SQL virtuellen Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="4282d-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4282d-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="4282d-139">Primärschlüssel des Speicherkontos für Zeuge</span><span class="sxs-lookup"><span data-stu-id="4282d-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="4282d-140">-StorageAccountUrl</span></span>
<span data-ttu-id="4282d-141">Primärschlüssel des Speicherkontos für Zeuge</span><span class="sxs-lookup"><span data-stu-id="4282d-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="4282d-142">-Tag</span></span>
<span data-ttu-id="4282d-143">Die Tags, die der Gruppe SQL virtuellen Computer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4282d-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282d-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4282d-144">-Confirm</span></span>
<span data-ttu-id="4282d-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4282d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4282d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4282d-146">-WhatIf</span></span>
<span data-ttu-id="4282d-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4282d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4282d-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4282d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4282d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4282d-149">CommonParameters</span></span>
<span data-ttu-id="4282d-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4282d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4282d-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4282d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4282d-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4282d-152">INPUTS</span></span>

### <span data-ttu-id="4282d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="4282d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="4282d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4282d-154">System.String</span></span>

## <span data-ttu-id="4282d-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4282d-155">OUTPUTS</span></span>

### <span data-ttu-id="4282d-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="4282d-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="4282d-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4282d-157">NOTES</span></span>

## <span data-ttu-id="4282d-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4282d-158">RELATED LINKS</span></span>
