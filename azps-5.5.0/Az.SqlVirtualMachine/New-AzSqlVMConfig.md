---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173772"
---
# <span data-ttu-id="c76d9-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="c76d9-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="c76d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c76d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c76d9-103">Erstellt eine neue Konfiguration für einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="c76d9-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="c76d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c76d9-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c76d9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c76d9-105">DESCRIPTION</span></span>
<span data-ttu-id="c76d9-106">Das New-AzSqlVMConfig erstellt ein neues Konfigurationsobjekt für einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="c76d9-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="c76d9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c76d9-107">EXAMPLES</span></span>

### <span data-ttu-id="c76d9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c76d9-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="c76d9-109">Erstellt ein lokal konfigurierbares Objekt des virtuellen Sql-Computers, das verwendet werden kann, um einen virtuellen Azure SQL-Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c76d9-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="c76d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c76d9-110">PARAMETERS</span></span>

### <span data-ttu-id="c76d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76d9-111">-DefaultProfile</span></span>
<span data-ttu-id="c76d9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c76d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c76d9-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c76d9-113">-LicenseType</span></span>
<span data-ttu-id="c76d9-114">SQL lizenztyp des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c76d9-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="c76d9-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="c76d9-115">-Offer</span></span>
<span data-ttu-id="c76d9-116">SQL angebot für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="c76d9-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="c76d9-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="c76d9-117">-Sku</span></span>
<span data-ttu-id="c76d9-118">SQL des Editionstyps des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c76d9-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="c76d9-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="c76d9-119">-SqlManagementType</span></span>
<span data-ttu-id="c76d9-120">SQL des Managementtyps virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="c76d9-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="c76d9-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c76d9-121">-Tag</span></span>
<span data-ttu-id="c76d9-122">Die Tags, die dem virtuellen SQL zugeordnet werden</span><span class="sxs-lookup"><span data-stu-id="c76d9-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="c76d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76d9-123">CommonParameters</span></span>
<span data-ttu-id="c76d9-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76d9-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c76d9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76d9-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c76d9-126">INPUTS</span></span>

### <span data-ttu-id="c76d9-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c76d9-127">None</span></span>

## <span data-ttu-id="c76d9-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c76d9-128">OUTPUTS</span></span>

### <span data-ttu-id="c76d9-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="c76d9-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="c76d9-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c76d9-130">NOTES</span></span>

## <span data-ttu-id="c76d9-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c76d9-131">RELATED LINKS</span></span>
