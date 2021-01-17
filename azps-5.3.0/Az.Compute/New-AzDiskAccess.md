---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473079"
---
# <span data-ttu-id="04caf-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="04caf-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="04caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04caf-102">SYNOPSIS</span></span>
<span data-ttu-id="04caf-103">Erstellt eine Datenträgerzugriffsressource</span><span class="sxs-lookup"><span data-stu-id="04caf-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="04caf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04caf-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04caf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04caf-105">DESCRIPTION</span></span>
<span data-ttu-id="04caf-106">Das **Cmdlet "New-AzDiskAccess"** erstellt eine Datenträgerzugriffsressource</span><span class="sxs-lookup"><span data-stu-id="04caf-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="04caf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04caf-107">EXAMPLES</span></span>

### <span data-ttu-id="04caf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04caf-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="04caf-109">Mit diesem Befehl wird ein Datenträgerzugriff mit bestimmten Eigenschaften erstellt.</span><span class="sxs-lookup"><span data-stu-id="04caf-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="04caf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04caf-110">PARAMETERS</span></span>

### <span data-ttu-id="04caf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04caf-111">-AsJob</span></span>
<span data-ttu-id="04caf-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="04caf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04caf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04caf-113">-DefaultProfile</span></span>
<span data-ttu-id="04caf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04caf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04caf-115">-Location</span><span class="sxs-lookup"><span data-stu-id="04caf-115">-Location</span></span>
<span data-ttu-id="04caf-116">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="04caf-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04caf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="04caf-117">-Name</span></span>
<span data-ttu-id="04caf-118">Gibt den Namen eines Datenträgerzugriffs an.</span><span class="sxs-lookup"><span data-stu-id="04caf-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04caf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04caf-119">-ResourceGroupName</span></span>
<span data-ttu-id="04caf-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="04caf-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04caf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04caf-121">-Confirm</span></span>
<span data-ttu-id="04caf-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04caf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04caf-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04caf-123">-WhatIf</span></span>
<span data-ttu-id="04caf-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04caf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04caf-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04caf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04caf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04caf-126">CommonParameters</span></span>
<span data-ttu-id="04caf-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04caf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04caf-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04caf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04caf-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04caf-129">INPUTS</span></span>

### <span data-ttu-id="04caf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="04caf-130">System.String</span></span>

## <span data-ttu-id="04caf-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04caf-131">OUTPUTS</span></span>

### <span data-ttu-id="04caf-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="04caf-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="04caf-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04caf-133">NOTES</span></span>

## <span data-ttu-id="04caf-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04caf-134">RELATED LINKS</span></span>
