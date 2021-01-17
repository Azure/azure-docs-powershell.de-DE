---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364929"
---
# <span data-ttu-id="e2faa-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e2faa-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="e2faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2faa-102">SYNOPSIS</span></span>
<span data-ttu-id="e2faa-103">Erstellt eine Datenträgerzugriffsressource</span><span class="sxs-lookup"><span data-stu-id="e2faa-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="e2faa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2faa-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2faa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2faa-105">DESCRIPTION</span></span>
<span data-ttu-id="e2faa-106">Das **Cmdlet "New-AzDiskAccess"** erstellt eine Datenträgerzugriffsressource</span><span class="sxs-lookup"><span data-stu-id="e2faa-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="e2faa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2faa-107">EXAMPLES</span></span>

### <span data-ttu-id="e2faa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2faa-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="e2faa-109">Mit diesem Befehl wird ein Datenträgerzugriff mit bestimmten Eigenschaften erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2faa-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="e2faa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2faa-110">PARAMETERS</span></span>

### <span data-ttu-id="e2faa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2faa-111">-AsJob</span></span>
<span data-ttu-id="e2faa-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e2faa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2faa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2faa-113">-DefaultProfile</span></span>
<span data-ttu-id="e2faa-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2faa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2faa-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e2faa-115">-Location</span></span>
<span data-ttu-id="e2faa-116">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="e2faa-116">Specifies the location.</span></span>

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

### <span data-ttu-id="e2faa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e2faa-117">-Name</span></span>
<span data-ttu-id="e2faa-118">Gibt den Namen eines Datenträgerzugriffs an.</span><span class="sxs-lookup"><span data-stu-id="e2faa-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="e2faa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2faa-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2faa-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e2faa-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e2faa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2faa-121">-Confirm</span></span>
<span data-ttu-id="e2faa-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2faa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2faa-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e2faa-123">-WhatIf</span></span>
<span data-ttu-id="e2faa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2faa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2faa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2faa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2faa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2faa-126">CommonParameters</span></span>
<span data-ttu-id="e2faa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2faa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2faa-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2faa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2faa-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2faa-129">INPUTS</span></span>

### <span data-ttu-id="e2faa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e2faa-130">System.String</span></span>

## <span data-ttu-id="e2faa-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2faa-131">OUTPUTS</span></span>

### <span data-ttu-id="e2faa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e2faa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="e2faa-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e2faa-133">NOTES</span></span>

## <span data-ttu-id="e2faa-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e2faa-134">RELATED LINKS</span></span>
