---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846415"
---
# <span data-ttu-id="71f86-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="71f86-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="71f86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71f86-102">SYNOPSIS</span></span>
<span data-ttu-id="71f86-103">Ruft mindestens einen virtuellen SQL-Computer ab.</span><span class="sxs-lookup"><span data-stu-id="71f86-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="71f86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71f86-104">SYNTAX</span></span>

### <span data-ttu-id="71f86-105">ResourceGroupOnly (Standard)</span><span class="sxs-lookup"><span data-stu-id="71f86-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71f86-106">Namen</span><span class="sxs-lookup"><span data-stu-id="71f86-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71f86-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="71f86-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71f86-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71f86-108">DESCRIPTION</span></span>
<span data-ttu-id="71f86-109">Das Get-AzSqlVM-Cmdlet ruft mindestens einen virtuellen SQL-Computer ab.</span><span class="sxs-lookup"><span data-stu-id="71f86-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="71f86-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71f86-110">EXAMPLES</span></span>

### <span data-ttu-id="71f86-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71f86-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="71f86-112">Dieser Befehl ruft Informationen zu allen virtuellen Azure SQL-Computern im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="71f86-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="71f86-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71f86-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="71f86-114">Dieser Befehl ruft Informationen zu allen virtuellen Azure SQL-Computern im aktuellen Abonnement ab, das der Ressourcengruppe ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="71f86-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="71f86-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="71f86-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="71f86-116">Dieser Befehl ruft Informationen zur virtuellen SQL-Maschine "VM" ab, die der Ressourcengruppe ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="71f86-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="71f86-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f86-117">PARAMETERS</span></span>

### <span data-ttu-id="71f86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f86-118">-DefaultProfile</span></span>
<span data-ttu-id="71f86-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71f86-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f86-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71f86-120">-Name</span></span>
<span data-ttu-id="71f86-121">Name des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="71f86-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="71f86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f86-122">-ResourceGroupName</span></span>
<span data-ttu-id="71f86-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71f86-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="71f86-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="71f86-124">-ResourceId</span></span>
<span data-ttu-id="71f86-125">Ressourcen-ID des SQL-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="71f86-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="71f86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f86-126">CommonParameters</span></span>
<span data-ttu-id="71f86-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f86-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71f86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f86-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71f86-129">INPUTS</span></span>

### <span data-ttu-id="71f86-130">Keine</span><span class="sxs-lookup"><span data-stu-id="71f86-130">None</span></span>

## <span data-ttu-id="71f86-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71f86-131">OUTPUTS</span></span>

### <span data-ttu-id="71f86-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="71f86-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="71f86-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="71f86-133">NOTES</span></span>

## <span data-ttu-id="71f86-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71f86-134">RELATED LINKS</span></span>
