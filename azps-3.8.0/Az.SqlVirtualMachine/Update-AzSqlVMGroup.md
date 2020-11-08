---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995774"
---
# <span data-ttu-id="efe93-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="efe93-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="efe93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efe93-102">SYNOPSIS</span></span>
<span data-ttu-id="efe93-103">Aktualisiert eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="efe93-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="efe93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efe93-104">SYNTAX</span></span>

### <span data-ttu-id="efe93-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="efe93-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efe93-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="efe93-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe93-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="efe93-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe93-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efe93-108">DESCRIPTION</span></span>
<span data-ttu-id="efe93-109">Das Update-AzSqlVMGroup-Cmdlet aktualisiert eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="efe93-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="efe93-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efe93-110">EXAMPLES</span></span>

### <span data-ttu-id="efe93-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efe93-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="efe93-112">Aktualisiert die Tags einer virtuellen SQL-Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="efe93-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="efe93-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="efe93-113">PARAMETERS</span></span>

### <span data-ttu-id="efe93-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efe93-114">-AsJob</span></span>
<span data-ttu-id="efe93-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="efe93-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="efe93-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="efe93-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="efe93-117">Zum Erstellen eines Clusters verwendeter Name</span><span class="sxs-lookup"><span data-stu-id="efe93-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="efe93-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="efe93-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="efe93-119">Name für Betriebs Cluster</span><span class="sxs-lookup"><span data-stu-id="efe93-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="efe93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe93-120">-DefaultProfile</span></span>
<span data-ttu-id="efe93-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efe93-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efe93-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="efe93-122">-DomainFqdn</span></span>
<span data-ttu-id="efe93-123">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="efe93-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="efe93-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="efe93-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="efe93-125">Optionaler Pfad für FileShare-Zeuge</span><span class="sxs-lookup"><span data-stu-id="efe93-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="efe93-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="efe93-126">-InputObject</span></span>
<span data-ttu-id="efe93-127">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="efe93-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="efe93-128">-Name</span><span class="sxs-lookup"><span data-stu-id="efe93-128">-Name</span></span>
<span data-ttu-id="efe93-129">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="efe93-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="efe93-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="efe93-130">-OuPath</span></span>
<span data-ttu-id="efe93-131">Pfad der Organisationseinheit, in dem Knoten und Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="efe93-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="efe93-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe93-132">-ResourceGroupName</span></span>
<span data-ttu-id="efe93-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="efe93-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="efe93-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="efe93-134">-ResourceId</span></span>
<span data-ttu-id="efe93-135">Ressourcen-ID der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="efe93-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="efe93-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="efe93-136">-SqlServiceAccount</span></span>
<span data-ttu-id="efe93-137">Name, unter dem der SQL-Dienst auf allen teilnehmenden virtuellen SQL-Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="efe93-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="efe93-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="efe93-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="efe93-139">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="efe93-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="efe93-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="efe93-140">-StorageAccountUrl</span></span>
<span data-ttu-id="efe93-141">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="efe93-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="efe93-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="efe93-142">-Tag</span></span>
<span data-ttu-id="efe93-143">Die Tags, die der Gruppe der virtuellen SQL-Computer zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="efe93-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="efe93-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efe93-144">-Confirm</span></span>
<span data-ttu-id="efe93-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efe93-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe93-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe93-146">-WhatIf</span></span>
<span data-ttu-id="efe93-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efe93-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe93-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efe93-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe93-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe93-149">CommonParameters</span></span>
<span data-ttu-id="efe93-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe93-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe93-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efe93-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe93-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efe93-152">INPUTS</span></span>

### <span data-ttu-id="efe93-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="efe93-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="efe93-154">System. String</span><span class="sxs-lookup"><span data-stu-id="efe93-154">System.String</span></span>

## <span data-ttu-id="efe93-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efe93-155">OUTPUTS</span></span>

### <span data-ttu-id="efe93-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="efe93-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="efe93-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="efe93-157">NOTES</span></span>

## <span data-ttu-id="efe93-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efe93-158">RELATED LINKS</span></span>
