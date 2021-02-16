---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150484"
---
# <span data-ttu-id="8d61c-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="8d61c-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="8d61c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d61c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d61c-103">Ruft eine oder mehrere Sql Virtual Machine-Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="8d61c-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8d61c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d61c-104">SYNTAX</span></span>

### <span data-ttu-id="8d61c-105">ResourceGroupOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d61c-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d61c-106">Name</span><span class="sxs-lookup"><span data-stu-id="8d61c-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d61c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d61c-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d61c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d61c-108">DESCRIPTION</span></span>
<span data-ttu-id="8d61c-109">Das Get-AzSqlVMGroup cmdlet ruft eine oder mehrere Sql Virtual Machine-Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="8d61c-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8d61c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d61c-110">EXAMPLES</span></span>

### <span data-ttu-id="8d61c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d61c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="8d61c-112">Dieser Befehl ruft Informationen zu allen Azure SQL virtuellen Computergruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8d61c-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="8d61c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8d61c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8d61c-114">Dieser Befehl ruft Informationen zu allen Azure SQL virtuellen Computergruppen im aktuellen Abonnement ab, das der Ressourcengruppe "ResourceGroup01" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8d61c-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8d61c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8d61c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8d61c-116">Dieser Befehl ruft Informationen über die SQL Gruppe "Test"" des virtuellen Computers ab, die der Ressourcengruppe "ResourceGroup01" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8d61c-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8d61c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d61c-117">PARAMETERS</span></span>

### <span data-ttu-id="8d61c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d61c-118">-DefaultProfile</span></span>
<span data-ttu-id="8d61c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d61c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d61c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8d61c-120">-Name</span></span>
<span data-ttu-id="8d61c-121">SQL gruppenname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8d61c-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="8d61c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d61c-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d61c-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d61c-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="8d61c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d61c-124">-ResourceId</span></span>
<span data-ttu-id="8d61c-125">SQL ressourcen-ID der Gruppe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8d61c-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="8d61c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d61c-126">CommonParameters</span></span>
<span data-ttu-id="8d61c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d61c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d61c-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d61c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d61c-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d61c-129">INPUTS</span></span>

### <span data-ttu-id="8d61c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8d61c-130">System.String</span></span>

## <span data-ttu-id="8d61c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d61c-131">OUTPUTS</span></span>

### <span data-ttu-id="8d61c-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="8d61c-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8d61c-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d61c-133">NOTES</span></span>

## <span data-ttu-id="8d61c-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d61c-134">RELATED LINKS</span></span>
