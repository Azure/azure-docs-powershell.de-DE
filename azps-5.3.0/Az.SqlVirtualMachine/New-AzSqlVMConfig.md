---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470322"
---
# <span data-ttu-id="a55ba-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="a55ba-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="a55ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a55ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a55ba-103">Erstellt eine neue Konfiguration für einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="a55ba-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="a55ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a55ba-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a55ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a55ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a55ba-106">Das New-AzSqlVMConfig erstellt ein neues Konfigurationsobjekt für einen virtuellen Sql-Computer.</span><span class="sxs-lookup"><span data-stu-id="a55ba-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="a55ba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a55ba-107">EXAMPLES</span></span>

### <span data-ttu-id="a55ba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a55ba-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a55ba-109">Erstellt ein lokal konfigurierbares Objekt des virtuellen Sql-Computers, das verwendet werden kann, um einen virtuellen Azure SQL-Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a55ba-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="a55ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a55ba-110">PARAMETERS</span></span>

### <span data-ttu-id="a55ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55ba-111">-DefaultProfile</span></span>
<span data-ttu-id="a55ba-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a55ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a55ba-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a55ba-113">-LicenseType</span></span>
<span data-ttu-id="a55ba-114">SQL lizenztyp des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a55ba-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="a55ba-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="a55ba-115">-Offer</span></span>
<span data-ttu-id="a55ba-116">SQL angebot für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="a55ba-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="a55ba-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="a55ba-117">-Sku</span></span>
<span data-ttu-id="a55ba-118">SQL des Editionstyps des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a55ba-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="a55ba-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="a55ba-119">-SqlManagementType</span></span>
<span data-ttu-id="a55ba-120">SQL virtual machine management type.</span><span class="sxs-lookup"><span data-stu-id="a55ba-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="a55ba-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="a55ba-121">-Tag</span></span>
<span data-ttu-id="a55ba-122">Die Tags, die dem virtuellen SQL zugeordnet werden</span><span class="sxs-lookup"><span data-stu-id="a55ba-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="a55ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55ba-123">CommonParameters</span></span>
<span data-ttu-id="a55ba-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55ba-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a55ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55ba-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a55ba-126">INPUTS</span></span>

### <span data-ttu-id="a55ba-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a55ba-127">None</span></span>

## <span data-ttu-id="a55ba-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a55ba-128">OUTPUTS</span></span>

### <span data-ttu-id="a55ba-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a55ba-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a55ba-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a55ba-130">NOTES</span></span>

## <span data-ttu-id="a55ba-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a55ba-131">RELATED LINKS</span></span>
