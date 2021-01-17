---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470629"
---
# <span data-ttu-id="36a18-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="36a18-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="36a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a18-102">SYNOPSIS</span></span>
<span data-ttu-id="36a18-103">Konfiguriert ein neues Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="36a18-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="36a18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36a18-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a18-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36a18-105">DESCRIPTION</span></span>
<span data-ttu-id="36a18-106">Das **Cmdlet "New-AzDataBoxEdgeDevice"** konfiguriert ein neues Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="36a18-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="36a18-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36a18-107">EXAMPLES</span></span>

### <span data-ttu-id="36a18-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36a18-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="36a18-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a18-109">PARAMETERS</span></span>

### <span data-ttu-id="36a18-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36a18-110">-AsJob</span></span>
<span data-ttu-id="36a18-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="36a18-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36a18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a18-112">-DefaultProfile</span></span>
<span data-ttu-id="36a18-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a18-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a18-114">-Location</span><span class="sxs-lookup"><span data-stu-id="36a18-114">-Location</span></span>
<span data-ttu-id="36a18-115">Position des Geräts</span><span class="sxs-lookup"><span data-stu-id="36a18-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a18-116">-Name</span><span class="sxs-lookup"><span data-stu-id="36a18-116">-Name</span></span>
<span data-ttu-id="36a18-117">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="36a18-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a18-118">-ResourceGroupName</span></span>
<span data-ttu-id="36a18-119">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="36a18-119">Resource Group Name</span></span>

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

### <span data-ttu-id="36a18-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="36a18-120">-Sku</span></span>
<span data-ttu-id="36a18-121">Verfügbare SKU sind Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="36a18-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a18-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36a18-122">-Confirm</span></span>
<span data-ttu-id="36a18-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36a18-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a18-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36a18-124">-WhatIf</span></span>
<span data-ttu-id="36a18-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36a18-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36a18-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36a18-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a18-127">CommonParameters</span></span>
<span data-ttu-id="36a18-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a18-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36a18-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a18-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36a18-130">INPUTS</span></span>

### <span data-ttu-id="36a18-131">Keine</span><span class="sxs-lookup"><span data-stu-id="36a18-131">None</span></span>

## <span data-ttu-id="36a18-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36a18-132">OUTPUTS</span></span>

### <span data-ttu-id="36a18-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="36a18-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="36a18-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36a18-134">NOTES</span></span>

## <span data-ttu-id="36a18-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36a18-135">RELATED LINKS</span></span>
