---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846416"
---
# <span data-ttu-id="35ace-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="35ace-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="35ace-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35ace-102">SYNOPSIS</span></span>
<span data-ttu-id="35ace-103">Ruft mindestens eine SQL Virtual Machine-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="35ace-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="35ace-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35ace-104">SYNTAX</span></span>

### <span data-ttu-id="35ace-105">ResourceGroupOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="35ace-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35ace-106">Namen</span><span class="sxs-lookup"><span data-stu-id="35ace-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35ace-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="35ace-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35ace-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35ace-108">DESCRIPTION</span></span>
<span data-ttu-id="35ace-109">Das Get-AzSqlVMGroup-Cmdlet ruft mindestens eine SQL Virtual Machine-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="35ace-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="35ace-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35ace-110">EXAMPLES</span></span>

### <span data-ttu-id="35ace-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35ace-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="35ace-112">Dieser Befehl ruft Informationen zu allen Azure SQL-virtuellen Computergruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="35ace-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="35ace-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35ace-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="35ace-114">Dieser Befehl ruft Informationen zu allen Azure SQL-virtuellen Computergruppen im aktuellen Abonnement ab, das der Ressourcengruppe ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="35ace-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="35ace-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="35ace-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="35ace-116">Dieser Befehl ruft Informationen zur Gruppe "Testgruppe" des SQL-virtuellen Computers ab, die der Ressourcengruppe ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="35ace-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="35ace-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="35ace-117">PARAMETERS</span></span>

### <span data-ttu-id="35ace-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ace-118">-DefaultProfile</span></span>
<span data-ttu-id="35ace-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35ace-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ace-120">-Name</span><span class="sxs-lookup"><span data-stu-id="35ace-120">-Name</span></span>
<span data-ttu-id="35ace-121">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="35ace-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="35ace-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ace-122">-ResourceGroupName</span></span>
<span data-ttu-id="35ace-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35ace-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="35ace-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="35ace-124">-ResourceId</span></span>
<span data-ttu-id="35ace-125">Ressourcen-ID der SQL-virtuellen Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="35ace-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="35ace-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ace-126">CommonParameters</span></span>
<span data-ttu-id="35ace-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ace-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ace-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35ace-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ace-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35ace-129">INPUTS</span></span>

### <span data-ttu-id="35ace-130">System. String</span><span class="sxs-lookup"><span data-stu-id="35ace-130">System.String</span></span>

## <span data-ttu-id="35ace-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35ace-131">OUTPUTS</span></span>

### <span data-ttu-id="35ace-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="35ace-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="35ace-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="35ace-133">NOTES</span></span>

## <span data-ttu-id="35ace-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35ace-134">RELATED LINKS</span></span>
