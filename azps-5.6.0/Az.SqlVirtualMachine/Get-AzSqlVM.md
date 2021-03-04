---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b3678b52f55e09fdcad8c1d116cd349b2cc5ab45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939288"
---
# <span data-ttu-id="b1201-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="b1201-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="b1201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1201-102">SYNOPSIS</span></span>
<span data-ttu-id="b1201-103">Ruft einen oder mehrere virtuelle Sql-Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b1201-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="b1201-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1201-104">SYNTAX</span></span>

### <span data-ttu-id="b1201-105">ResourceGroupOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1201-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1201-106">Name</span><span class="sxs-lookup"><span data-stu-id="b1201-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1201-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1201-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1201-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1201-108">DESCRIPTION</span></span>
<span data-ttu-id="b1201-109">Das Get-AzSqlVM-Cmdlet ruft einen oder mehrere virtuelle Sql-Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b1201-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="b1201-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1201-110">EXAMPLES</span></span>

### <span data-ttu-id="b1201-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1201-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="b1201-112">Dieser Befehl ruft Informationen zu allen virtuellen Azure-SQL im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b1201-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="b1201-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b1201-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="b1201-114">Dieser Befehl ruft Informationen zu allen virtuellen Azure SQL im aktuellen Abonnement ab, das der Ressourcengruppe ResourceGroup01 zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b1201-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b1201-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b1201-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="b1201-116">Dieser Befehl ruft Informationen zum virtuellen Computer "vm" SQL ab, der der Ressourcengruppe ResourceGroup01 zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b1201-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b1201-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b1201-117">PARAMETERS</span></span>

### <span data-ttu-id="b1201-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1201-118">-DefaultProfile</span></span>
<span data-ttu-id="b1201-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1201-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1201-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b1201-120">-Name</span></span>
<span data-ttu-id="b1201-121">SQL namen des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b1201-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="b1201-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1201-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1201-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1201-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1201-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1201-124">-ResourceId</span></span>
<span data-ttu-id="b1201-125">SQL ressourcen-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b1201-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="b1201-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1201-126">CommonParameters</span></span>
<span data-ttu-id="b1201-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1201-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1201-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1201-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1201-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1201-129">INPUTS</span></span>

### <span data-ttu-id="b1201-130">Keine</span><span class="sxs-lookup"><span data-stu-id="b1201-130">None</span></span>

## <span data-ttu-id="b1201-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1201-131">OUTPUTS</span></span>

### <span data-ttu-id="b1201-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b1201-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b1201-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b1201-133">NOTES</span></span>

## <span data-ttu-id="b1201-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b1201-134">RELATED LINKS</span></span>
