---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470324"
---
# <span data-ttu-id="0af65-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="0af65-101">New-AzSqlVM</span></span>

## <span data-ttu-id="0af65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af65-102">SYNOPSIS</span></span>
<span data-ttu-id="0af65-103">Erstellt einen neuen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="0af65-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="0af65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0af65-104">SYNTAX</span></span>

### <span data-ttu-id="0af65-105">NameParamaterList (Standard)</span><span class="sxs-lookup"><span data-stu-id="0af65-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af65-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="0af65-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af65-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0af65-107">DESCRIPTION</span></span>
<span data-ttu-id="0af65-108">Das New-AzSqlVM erstellt einen virtuellen Azure SQL Computer.</span><span class="sxs-lookup"><span data-stu-id="0af65-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="0af65-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0af65-109">EXAMPLES</span></span>

### <span data-ttu-id="0af65-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0af65-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="0af65-111">Erstellt einen neuen virtuellen Azure SQL Computer mit "name vm" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0af65-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="0af65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0af65-112">PARAMETERS</span></span>

### <span data-ttu-id="0af65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0af65-113">-AsJob</span></span>
<span data-ttu-id="0af65-114">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="0af65-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0af65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af65-115">-DefaultProfile</span></span>
<span data-ttu-id="0af65-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0af65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af65-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0af65-117">-LicenseType</span></span>
<span data-ttu-id="0af65-118">SQL lizenztyp des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0af65-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0af65-119">-Location</span></span>
<span data-ttu-id="0af65-120">SQL position des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0af65-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="0af65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0af65-121">-Name</span></span>
<span data-ttu-id="0af65-122">SQL namen des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0af65-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="0af65-123">-Offer</span></span>
<span data-ttu-id="0af65-124">SQL angebot für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="0af65-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af65-125">-ResourceGroupName</span></span>
<span data-ttu-id="0af65-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0af65-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0af65-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="0af65-127">-Sku</span></span>
<span data-ttu-id="0af65-128">SQL des Editionstyps des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="0af65-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="0af65-129">-SqlManagementType</span></span>
<span data-ttu-id="0af65-130">SQL des Managementtyps virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="0af65-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="0af65-131">-SqlVM</span></span>
<span data-ttu-id="0af65-132">SQL virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="0af65-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0af65-133">-Tag</span></span>
<span data-ttu-id="0af65-134">Die Tags, die dem virtuellen SQL zugeordnet werden</span><span class="sxs-lookup"><span data-stu-id="0af65-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af65-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0af65-135">-Confirm</span></span>
<span data-ttu-id="0af65-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0af65-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af65-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0af65-137">-WhatIf</span></span>
<span data-ttu-id="0af65-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0af65-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0af65-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0af65-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af65-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af65-140">CommonParameters</span></span>
<span data-ttu-id="0af65-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af65-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af65-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0af65-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af65-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0af65-143">INPUTS</span></span>

### <span data-ttu-id="0af65-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="0af65-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="0af65-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0af65-145">OUTPUTS</span></span>

### <span data-ttu-id="0af65-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="0af65-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="0af65-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0af65-147">NOTES</span></span>

## <span data-ttu-id="0af65-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0af65-148">RELATED LINKS</span></span>
