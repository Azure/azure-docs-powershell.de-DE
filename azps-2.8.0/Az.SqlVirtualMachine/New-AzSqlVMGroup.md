---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: e46df689b4cc6953f29f5361c4df8bc5bd878acd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826256"
---
# <span data-ttu-id="2fb3d-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="2fb3d-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="2fb3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb3d-103">Erstellt eine neue Gruppe für virtuelle SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="2fb3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb3d-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb3d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fb3d-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb3d-106">Mit dem New-AzSqlVMGroup-Cmdlet wird eine Azure SQL-Gruppe virtueller Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="2fb3d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fb3d-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb3d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fb3d-108">Example 1</span></span>
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

<span data-ttu-id="2fb3d-109">Erstellt eine neue Azure SQL-Gruppe virtueller Computer mit Testgruppen-VM in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="2fb3d-110">$Profile ist ein Objekt vom Typ Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="2fb3d-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="2fb3d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb3d-111">PARAMETERS</span></span>

### <span data-ttu-id="2fb3d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fb3d-112">-AsJob</span></span>
<span data-ttu-id="2fb3d-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2fb3d-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="2fb3d-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="2fb3d-115">Zum Erstellen eines Clusters verwendeter Name</span><span class="sxs-lookup"><span data-stu-id="2fb3d-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="2fb3d-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="2fb3d-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="2fb3d-117">Name für Betriebs Cluster</span><span class="sxs-lookup"><span data-stu-id="2fb3d-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="2fb3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb3d-118">-DefaultProfile</span></span>
<span data-ttu-id="2fb3d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb3d-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="2fb3d-120">-DomainFqdn</span></span>
<span data-ttu-id="2fb3d-121">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="2fb3d-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="2fb3d-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="2fb3d-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="2fb3d-123">Optionaler Pfad für FileShare-Zeuge</span><span class="sxs-lookup"><span data-stu-id="2fb3d-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="2fb3d-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="2fb3d-124">-Location</span></span>
<span data-ttu-id="2fb3d-125">Speicherort der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="2fb3d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2fb3d-126">-Name</span></span>
<span data-ttu-id="2fb3d-127">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="2fb3d-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="2fb3d-128">-Angebot</span><span class="sxs-lookup"><span data-stu-id="2fb3d-128">-Offer</span></span>
<span data-ttu-id="2fb3d-129">Gruppenangebot für SQL-virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="2fb3d-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="2fb3d-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="2fb3d-130">-OuPath</span></span>
<span data-ttu-id="2fb3d-131">Pfad der Organisationseinheit, in dem Knoten und Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="2fb3d-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="2fb3d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb3d-132">-ResourceGroupName</span></span>
<span data-ttu-id="2fb3d-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fb3d-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="2fb3d-134">-Sku</span></span>
<span data-ttu-id="2fb3d-135">SQL Virtual Machine Group Edition-Typ.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="2fb3d-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="2fb3d-136">-SqlServiceAccount</span></span>
<span data-ttu-id="2fb3d-137">Name, unter dem der SQL-Dienst auf allen teilnehmenden virtuellen SQL-Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="2fb3d-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="2fb3d-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2fb3d-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="2fb3d-139">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="2fb3d-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="2fb3d-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="2fb3d-140">-StorageAccountUrl</span></span>
<span data-ttu-id="2fb3d-141">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="2fb3d-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="2fb3d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fb3d-142">-Tag</span></span>
<span data-ttu-id="2fb3d-143">Die Tags, die der Gruppe der virtuellen SQL-Computer zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="2fb3d-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fb3d-144">-Confirm</span></span>
<span data-ttu-id="2fb3d-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb3d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb3d-146">-WhatIf</span></span>
<span data-ttu-id="2fb3d-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb3d-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb3d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb3d-149">CommonParameters</span></span>
<span data-ttu-id="2fb3d-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb3d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb3d-151">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fb3d-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb3d-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fb3d-152">INPUTS</span></span>

### <span data-ttu-id="2fb3d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2fb3d-153">System.String</span></span>

## <span data-ttu-id="2fb3d-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fb3d-154">OUTPUTS</span></span>

### <span data-ttu-id="2fb3d-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="2fb3d-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="2fb3d-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fb3d-156">NOTES</span></span>

## <span data-ttu-id="2fb3d-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fb3d-157">RELATED LINKS</span></span>
