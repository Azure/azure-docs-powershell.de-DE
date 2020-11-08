---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174046"
---
# <span data-ttu-id="9ec31-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="9ec31-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="9ec31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ec31-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec31-103">Aktualisiert eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9ec31-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="9ec31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ec31-104">SYNTAX</span></span>

### <span data-ttu-id="9ec31-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ec31-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec31-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9ec31-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec31-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec31-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec31-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec31-108">DESCRIPTION</span></span>
<span data-ttu-id="9ec31-109">Das Update-AzSqlVMGroup-Cmdlet aktualisiert eine SQL Virtual Machine-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9ec31-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="9ec31-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ec31-110">EXAMPLES</span></span>

### <span data-ttu-id="9ec31-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ec31-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="9ec31-112">Aktualisiert die Tags einer virtuellen SQL-Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="9ec31-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="9ec31-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec31-113">PARAMETERS</span></span>

### <span data-ttu-id="9ec31-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ec31-114">-AsJob</span></span>
<span data-ttu-id="9ec31-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="9ec31-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9ec31-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="9ec31-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="9ec31-117">Zum Erstellen eines Clusters verwendeter Name</span><span class="sxs-lookup"><span data-stu-id="9ec31-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="9ec31-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="9ec31-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="9ec31-119">Name für Betriebs Cluster</span><span class="sxs-lookup"><span data-stu-id="9ec31-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="9ec31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec31-120">-DefaultProfile</span></span>
<span data-ttu-id="9ec31-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ec31-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ec31-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="9ec31-122">-DomainFqdn</span></span>
<span data-ttu-id="9ec31-123">Vollqualifizierter Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="9ec31-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="9ec31-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="9ec31-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="9ec31-125">Optionaler Pfad für FileShare-Zeuge</span><span class="sxs-lookup"><span data-stu-id="9ec31-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="9ec31-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ec31-126">-InputObject</span></span>
<span data-ttu-id="9ec31-127">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="9ec31-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="9ec31-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9ec31-128">-Name</span></span>
<span data-ttu-id="9ec31-129">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="9ec31-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="9ec31-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="9ec31-130">-OuPath</span></span>
<span data-ttu-id="9ec31-131">Pfad der Organisationseinheit, in dem Knoten und Cluster vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="9ec31-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="9ec31-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec31-132">-ResourceGroupName</span></span>
<span data-ttu-id="9ec31-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ec31-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ec31-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9ec31-134">-ResourceId</span></span>
<span data-ttu-id="9ec31-135">Ressourcen-ID der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="9ec31-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="9ec31-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="9ec31-136">-SqlServiceAccount</span></span>
<span data-ttu-id="9ec31-137">Name, unter dem der SQL-Dienst auf allen teilnehmenden virtuellen SQL-Computern im Cluster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="9ec31-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="9ec31-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9ec31-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="9ec31-139">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9ec31-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="9ec31-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="9ec31-140">-StorageAccountUrl</span></span>
<span data-ttu-id="9ec31-141">Primärschlüssel des Zeugen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9ec31-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="9ec31-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ec31-142">-Tag</span></span>
<span data-ttu-id="9ec31-143">Die Tags, die der Gruppe der virtuellen SQL-Computer zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9ec31-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="9ec31-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ec31-144">-Confirm</span></span>
<span data-ttu-id="9ec31-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ec31-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec31-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec31-146">-WhatIf</span></span>
<span data-ttu-id="9ec31-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec31-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec31-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec31-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec31-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec31-149">CommonParameters</span></span>
<span data-ttu-id="9ec31-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec31-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec31-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ec31-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec31-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ec31-152">INPUTS</span></span>

### <span data-ttu-id="9ec31-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="9ec31-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="9ec31-154">System. String</span><span class="sxs-lookup"><span data-stu-id="9ec31-154">System.String</span></span>

## <span data-ttu-id="9ec31-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ec31-155">OUTPUTS</span></span>

### <span data-ttu-id="9ec31-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="9ec31-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="9ec31-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ec31-157">NOTES</span></span>

## <span data-ttu-id="9ec31-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ec31-158">RELATED LINKS</span></span>
