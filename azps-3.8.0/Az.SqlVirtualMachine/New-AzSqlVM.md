---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846467"
---
# <span data-ttu-id="73086-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="73086-101">New-AzSqlVM</span></span>

## <span data-ttu-id="73086-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73086-102">SYNOPSIS</span></span>
<span data-ttu-id="73086-103">Erstellt einen neuen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="73086-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="73086-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73086-104">SYNTAX</span></span>

### <span data-ttu-id="73086-105">NameParamaterList (Standard)</span><span class="sxs-lookup"><span data-stu-id="73086-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73086-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="73086-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73086-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73086-107">DESCRIPTION</span></span>
<span data-ttu-id="73086-108">Das New-AzSqlVM-Cmdlet erstellt einen virtuellen Azure SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="73086-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="73086-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73086-109">EXAMPLES</span></span>

### <span data-ttu-id="73086-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73086-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="73086-111">Erstellt einen neuen Azure SQL-virtuellen Computer mit dem Namen VM in der Ressourcengruppe ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="73086-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="73086-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="73086-112">PARAMETERS</span></span>

### <span data-ttu-id="73086-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73086-113">-AsJob</span></span>
<span data-ttu-id="73086-114">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="73086-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="73086-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73086-115">-DefaultProfile</span></span>
<span data-ttu-id="73086-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73086-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73086-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="73086-117">-LicenseType</span></span>
<span data-ttu-id="73086-118">License Type für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="73086-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="73086-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="73086-119">-Location</span></span>
<span data-ttu-id="73086-120">Speicherort des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="73086-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="73086-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73086-121">-Name</span></span>
<span data-ttu-id="73086-122">Name des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="73086-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="73086-123">-Angebot</span><span class="sxs-lookup"><span data-stu-id="73086-123">-Offer</span></span>
<span data-ttu-id="73086-124">Angebot für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="73086-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="73086-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73086-125">-ResourceGroupName</span></span>
<span data-ttu-id="73086-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73086-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="73086-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="73086-127">-Sku</span></span>
<span data-ttu-id="73086-128">SQL Virtual Machine Edition-Typ.</span><span class="sxs-lookup"><span data-stu-id="73086-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="73086-129">-Sqlmanagetype</span><span class="sxs-lookup"><span data-stu-id="73086-129">-SqlManagementType</span></span>
<span data-ttu-id="73086-130">Verwaltungstyp für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="73086-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="73086-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="73086-131">-SqlVM</span></span>
<span data-ttu-id="73086-132">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="73086-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="73086-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="73086-133">-Tag</span></span>
<span data-ttu-id="73086-134">Die Tags, die dem virtuellen SQL-Computer zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="73086-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="73086-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73086-135">-Confirm</span></span>
<span data-ttu-id="73086-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73086-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73086-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73086-137">-WhatIf</span></span>
<span data-ttu-id="73086-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73086-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73086-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73086-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73086-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73086-140">CommonParameters</span></span>
<span data-ttu-id="73086-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73086-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73086-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73086-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73086-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73086-143">INPUTS</span></span>

### <span data-ttu-id="73086-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="73086-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="73086-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73086-145">OUTPUTS</span></span>

### <span data-ttu-id="73086-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="73086-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="73086-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="73086-147">NOTES</span></span>

## <span data-ttu-id="73086-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73086-148">RELATED LINKS</span></span>
