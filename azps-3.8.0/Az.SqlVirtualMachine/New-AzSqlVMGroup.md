---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846403"
---
# <span data-ttu-id="20d35-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="20d35-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="20d35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20d35-102">SYNOPSIS</span></span>
<span data-ttu-id="20d35-103">Erstellt eine neue Gruppe für virtuelle SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="20d35-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="20d35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20d35-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20d35-105">DESCRIPTION</span></span>
<span data-ttu-id="20d35-106">Mit dem New-AzSqlVMGroup-Cmdlet wird eine Azure SQL-Gruppe virtueller Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="20d35-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="20d35-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20d35-107">EXAMPLES</span></span>

### <span data-ttu-id="20d35-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20d35-108">Example 1</span></span>
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

<span data-ttu-id="20d35-109">Erstellt eine neue Azure SQL-Gruppe virtueller Computer mit Testgruppen-VM in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="20d35-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="20d35-110">$Profile ist ein Objekt vom Typ Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="20d35-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="20d35-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="20d35-111">PARAMETERS</span></span>

### <span data-ttu-id="20d35-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20d35-112">-AsJob</span></span>
<span data-ttu-id="20d35-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="20d35-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="20d35-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="20d35-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="20d35-115">Zum Erstellen eines Clusters verwendeter Name</span><span class="sxs-lookup"><span data-stu-id="20d35-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="20d35-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="20d35-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="20d35-117">Name für Betriebs Cluster</span><span class="sxs-lookup"><span data-stu-id="20d35-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="20d35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d35-118">-DefaultProfile</span></span>
<span data-ttu-id="20d35-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20d35-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d35-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="20d35-120">-DomainFqdn</span></span>
<span data-ttu-id="20d35-121">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="20d35-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="20d35-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="20d35-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="20d35-123">Optionaler Pfad für FileShare-Zeuge</span><span class="sxs-lookup"><span data-stu-id="20d35-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="20d35-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="20d35-124">-Location</span></span>
<span data-ttu-id="20d35-125">Speicherort der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="20d35-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="20d35-126">-Name</span><span class="sxs-lookup"><span data-stu-id="20d35-126">-Name</span></span>
<span data-ttu-id="20d35-127">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="20d35-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="20d35-128">-Angebot</span><span class="sxs-lookup"><span data-stu-id="20d35-128">-Offer</span></span>
<span data-ttu-id="20d35-129">Gruppenangebot für SQL-virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="20d35-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="20d35-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="20d35-130">-OuPath</span></span>
<span data-ttu-id="20d35-131">Pfad der Organisationseinheit, in dem Knoten und Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="20d35-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="20d35-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d35-132">-ResourceGroupName</span></span>
<span data-ttu-id="20d35-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20d35-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="20d35-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="20d35-134">-Sku</span></span>
<span data-ttu-id="20d35-135">SQL Virtual Machine Group Edition-Typ.</span><span class="sxs-lookup"><span data-stu-id="20d35-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="20d35-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="20d35-136">-SqlServiceAccount</span></span>
<span data-ttu-id="20d35-137">Name, unter dem der SQL-Dienst auf allen teilnehmenden virtuellen SQL-Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="20d35-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="20d35-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="20d35-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="20d35-139">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="20d35-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="20d35-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="20d35-140">-StorageAccountUrl</span></span>
<span data-ttu-id="20d35-141">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="20d35-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="20d35-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="20d35-142">-Tag</span></span>
<span data-ttu-id="20d35-143">Die Tags, die der Gruppe der virtuellen SQL-Computer zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20d35-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="20d35-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20d35-144">-Confirm</span></span>
<span data-ttu-id="20d35-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20d35-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d35-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d35-146">-WhatIf</span></span>
<span data-ttu-id="20d35-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20d35-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d35-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20d35-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d35-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d35-149">CommonParameters</span></span>
<span data-ttu-id="20d35-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d35-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d35-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20d35-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d35-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20d35-152">INPUTS</span></span>

### <span data-ttu-id="20d35-153">System. String</span><span class="sxs-lookup"><span data-stu-id="20d35-153">System.String</span></span>

## <span data-ttu-id="20d35-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20d35-154">OUTPUTS</span></span>

### <span data-ttu-id="20d35-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="20d35-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="20d35-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="20d35-156">NOTES</span></span>

## <span data-ttu-id="20d35-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20d35-157">RELATED LINKS</span></span>
