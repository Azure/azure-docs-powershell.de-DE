---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: a2ee91815553b1de6ae21eb2afb344e010058deb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826259"
---
# <span data-ttu-id="a5caf-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="a5caf-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="a5caf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5caf-102">SYNOPSIS</span></span>
<span data-ttu-id="a5caf-103">Erstellt eine neue Konfiguration für einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="a5caf-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="a5caf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5caf-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5caf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5caf-105">DESCRIPTION</span></span>
<span data-ttu-id="a5caf-106">Das New-AzSqlVMConfig-Cmdlet erstellt ein neues Configuration-Objekt für einen virtuellen SQL-Computer.</span><span class="sxs-lookup"><span data-stu-id="a5caf-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="a5caf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5caf-107">EXAMPLES</span></span>

### <span data-ttu-id="a5caf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5caf-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a5caf-109">Erstellt ein lokales konfigurierbares Objekt des SQL Virtual Machine, das zum Erstellen eines virtuellen Azure SQL-Computers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5caf-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="a5caf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5caf-110">PARAMETERS</span></span>

### <span data-ttu-id="a5caf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5caf-111">-DefaultProfile</span></span>
<span data-ttu-id="a5caf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5caf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5caf-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a5caf-113">-LicenseType</span></span>
<span data-ttu-id="a5caf-114">License Type für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="a5caf-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="a5caf-115">-Angebot</span><span class="sxs-lookup"><span data-stu-id="a5caf-115">-Offer</span></span>
<span data-ttu-id="a5caf-116">Angebot für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="a5caf-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="a5caf-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5caf-117">-Sku</span></span>
<span data-ttu-id="a5caf-118">SQL Virtual Machine Edition-Typ.</span><span class="sxs-lookup"><span data-stu-id="a5caf-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="a5caf-119">-Sqlmanagetype</span><span class="sxs-lookup"><span data-stu-id="a5caf-119">-SqlManagementType</span></span>
<span data-ttu-id="a5caf-120">Verwaltungstyp für SQL-Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="a5caf-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="a5caf-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5caf-121">-Tag</span></span>
<span data-ttu-id="a5caf-122">Die Tags, die dem virtuellen SQL-Computer zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a5caf-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="a5caf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5caf-123">CommonParameters</span></span>
<span data-ttu-id="a5caf-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5caf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5caf-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5caf-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5caf-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5caf-126">INPUTS</span></span>

### <span data-ttu-id="a5caf-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a5caf-127">None</span></span>

## <span data-ttu-id="a5caf-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5caf-128">OUTPUTS</span></span>

### <span data-ttu-id="a5caf-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a5caf-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a5caf-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5caf-130">NOTES</span></span>

## <span data-ttu-id="a5caf-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5caf-131">RELATED LINKS</span></span>
