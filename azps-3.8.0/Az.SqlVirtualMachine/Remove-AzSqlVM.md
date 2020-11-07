---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846400"
---
# <span data-ttu-id="611a6-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="611a6-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="611a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="611a6-102">SYNOPSIS</span></span>
<span data-ttu-id="611a6-103">Löscht einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="611a6-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="611a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="611a6-104">SYNTAX</span></span>

### <span data-ttu-id="611a6-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="611a6-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="611a6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="611a6-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="611a6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="611a6-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="611a6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="611a6-108">DESCRIPTION</span></span>
<span data-ttu-id="611a6-109">Das Remove-AzSqlVM-Cmdlet löscht einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="611a6-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="611a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="611a6-110">EXAMPLES</span></span>

### <span data-ttu-id="611a6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="611a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="611a6-112">Löscht den virtuellen Azure SQL-Computer "VM" in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="611a6-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="611a6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="611a6-113">PARAMETERS</span></span>

### <span data-ttu-id="611a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="611a6-114">-AsJob</span></span>
<span data-ttu-id="611a6-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="611a6-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="611a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611a6-116">-DefaultProfile</span></span>
<span data-ttu-id="611a6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="611a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="611a6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="611a6-118">-InputObject</span></span>
<span data-ttu-id="611a6-119">SQL-Objekt für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="611a6-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="611a6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="611a6-120">-Name</span></span>
<span data-ttu-id="611a6-121">Name des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="611a6-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611a6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="611a6-122">-PassThru</span></span>
<span data-ttu-id="611a6-123">Gibt an, ob die gelöschte Ressource am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="611a6-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="611a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="611a6-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="611a6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="611a6-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="611a6-126">-ResourceId</span></span>
<span data-ttu-id="611a6-127">Ressourcen-ID des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="611a6-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611a6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="611a6-128">-Confirm</span></span>
<span data-ttu-id="611a6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="611a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="611a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="611a6-130">-WhatIf</span></span>
<span data-ttu-id="611a6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="611a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="611a6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="611a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="611a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611a6-133">CommonParameters</span></span>
<span data-ttu-id="611a6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="611a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611a6-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="611a6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611a6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="611a6-136">INPUTS</span></span>

### <span data-ttu-id="611a6-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="611a6-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="611a6-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="611a6-138">OUTPUTS</span></span>

### <span data-ttu-id="611a6-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="611a6-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="611a6-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="611a6-140">NOTES</span></span>

## <span data-ttu-id="611a6-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="611a6-141">RELATED LINKS</span></span>
