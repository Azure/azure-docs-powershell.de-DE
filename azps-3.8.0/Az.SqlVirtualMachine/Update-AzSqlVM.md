---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: ce700b90194e1cd0fcdf05162696ae980d24ad01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004393"
---
# <span data-ttu-id="014b0-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="014b0-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="014b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="014b0-102">SYNOPSIS</span></span>
<span data-ttu-id="014b0-103">Aktualisiert einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="014b0-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="014b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="014b0-104">SYNTAX</span></span>

### <span data-ttu-id="014b0-105">NameParamaterList (Standard)</span><span class="sxs-lookup"><span data-stu-id="014b0-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014b0-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="014b0-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014b0-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="014b0-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014b0-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="014b0-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014b0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="014b0-109">DESCRIPTION</span></span>
<span data-ttu-id="014b0-110">Das Update-AzSqlVM-Cmdlet aktualisiert einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="014b0-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="014b0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="014b0-111">EXAMPLES</span></span>

### <span data-ttu-id="014b0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="014b0-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="014b0-113">Aktualisiert die Tags einer virtuellen SQL-Maschine.</span><span class="sxs-lookup"><span data-stu-id="014b0-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="014b0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="014b0-114">PARAMETERS</span></span>

### <span data-ttu-id="014b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="014b0-115">-AsJob</span></span>
<span data-ttu-id="014b0-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="014b0-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="014b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014b0-117">-DefaultProfile</span></span>
<span data-ttu-id="014b0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="014b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="014b0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="014b0-119">-InputObject</span></span>
<span data-ttu-id="014b0-120">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="014b0-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="014b0-121">-LicenseType</span></span>
<span data-ttu-id="014b0-122">License Type für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="014b0-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="014b0-123">-Name</span></span>
<span data-ttu-id="014b0-124">Name des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="014b0-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-125">-Angebot</span><span class="sxs-lookup"><span data-stu-id="014b0-125">-Offer</span></span>
<span data-ttu-id="014b0-126">Angebot für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="014b0-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="014b0-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="014b0-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="014b0-129">-ResourceId</span></span>
<span data-ttu-id="014b0-130">Ressourcen-ID des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="014b0-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="014b0-131">-Sku</span></span>
<span data-ttu-id="014b0-132">SQL Virtual Machine Edition-Typ.</span><span class="sxs-lookup"><span data-stu-id="014b0-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-133">-Sqlmanagetype</span><span class="sxs-lookup"><span data-stu-id="014b0-133">-SqlManagementType</span></span>
<span data-ttu-id="014b0-134">Verwaltungstyp für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="014b0-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="014b0-135">-Tag</span></span>
<span data-ttu-id="014b0-136">Die Tags, die dem virtuellen SQL-Computer zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="014b0-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014b0-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="014b0-137">-Confirm</span></span>
<span data-ttu-id="014b0-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="014b0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014b0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014b0-139">-WhatIf</span></span>
<span data-ttu-id="014b0-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="014b0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014b0-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="014b0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014b0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014b0-142">CommonParameters</span></span>
<span data-ttu-id="014b0-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="014b0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014b0-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="014b0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014b0-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="014b0-145">INPUTS</span></span>

### <span data-ttu-id="014b0-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="014b0-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="014b0-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="014b0-147">OUTPUTS</span></span>

### <span data-ttu-id="014b0-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="014b0-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="014b0-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="014b0-149">NOTES</span></span>

## <span data-ttu-id="014b0-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="014b0-150">RELATED LINKS</span></span>
