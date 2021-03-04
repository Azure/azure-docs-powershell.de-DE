---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: bc9c881a69ee2365dcb9ff805c1c14fe3f1bbf79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931648"
---
# <span data-ttu-id="ce2b8-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ce2b8-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="ce2b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2b8-103">Erstellt eine neue Sql Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="ce2b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce2b8-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce2b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce2b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2b8-106">Das New-AzSqlVMGroup-Cmdlet erstellt eine Azure SQL Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="ce2b8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce2b8-107">EXAMPLES</span></span>

### <span data-ttu-id="ce2b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce2b8-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ce2b8-109">Erstellt eine neue Azure SQL Gruppe virtueller Computer mit der Testgruppe vm in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="ce2b8-110">$profile ist ein Objekt vom Typ Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="ce2b8-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ce2b8-111">PARAMETERS</span></span>

### <span data-ttu-id="ce2b8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce2b8-112">-AsJob</span></span>
<span data-ttu-id="ce2b8-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ce2b8-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="ce2b8-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="ce2b8-115">Name, der zum Erstellen von Clustern verwendet wird</span><span class="sxs-lookup"><span data-stu-id="ce2b8-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="ce2b8-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="ce2b8-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="ce2b8-117">Name, der für den Betrieb von Clustern verwendet wird</span><span class="sxs-lookup"><span data-stu-id="ce2b8-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2b8-118">-DefaultProfile</span></span>
<span data-ttu-id="ce2b8-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce2b8-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="ce2b8-120">-DomainFqdn</span></span>
<span data-ttu-id="ce2b8-121">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="ce2b8-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="ce2b8-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="ce2b8-123">Optionaler Pfad für fileshare witness</span><span class="sxs-lookup"><span data-stu-id="ce2b8-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="ce2b8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ce2b8-124">-Location</span></span>
<span data-ttu-id="ce2b8-125">SQL des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ce2b8-126">-Name</span></span>
<span data-ttu-id="ce2b8-127">SQL namen der Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-128">-Angebot</span><span class="sxs-lookup"><span data-stu-id="ce2b8-128">-Offer</span></span>
<span data-ttu-id="ce2b8-129">SQL virtuellen Computergruppenangebot.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="ce2b8-130">-OuPath</span></span>
<span data-ttu-id="ce2b8-131">Pfad der Organisationseinheit, in dem die Knoten und der Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="ce2b8-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="ce2b8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2b8-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce2b8-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="ce2b8-134">-Sku</span></span>
<span data-ttu-id="ce2b8-135">SQL des Gruppeneditionstyps des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ce2b8-136">-SqlServiceAccount</span></span>
<span data-ttu-id="ce2b8-137">Name, unter dem SQL dienst auf allen teilnehmenden SQL virtuellen Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="ce2b8-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ce2b8-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="ce2b8-139">Primärschlüssel des Speicherkontos für Zeuge</span><span class="sxs-lookup"><span data-stu-id="ce2b8-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ce2b8-140">-StorageAccountUrl</span></span>
<span data-ttu-id="ce2b8-141">Primärschlüssel des Speicherkontos für Zeuge</span><span class="sxs-lookup"><span data-stu-id="ce2b8-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce2b8-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce2b8-142">-Tag</span></span>
<span data-ttu-id="ce2b8-143">Die Tags, die der Gruppe SQL virtuellen Computer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="ce2b8-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce2b8-144">-Confirm</span></span>
<span data-ttu-id="ce2b8-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce2b8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce2b8-146">-WhatIf</span></span>
<span data-ttu-id="ce2b8-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce2b8-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce2b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2b8-149">CommonParameters</span></span>
<span data-ttu-id="ce2b8-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce2b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2b8-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce2b8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2b8-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce2b8-152">INPUTS</span></span>

### <span data-ttu-id="ce2b8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ce2b8-153">System.String</span></span>

## <span data-ttu-id="ce2b8-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce2b8-154">OUTPUTS</span></span>

### <span data-ttu-id="ce2b8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ce2b8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ce2b8-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ce2b8-156">NOTES</span></span>

## <span data-ttu-id="ce2b8-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ce2b8-157">RELATED LINKS</span></span>
