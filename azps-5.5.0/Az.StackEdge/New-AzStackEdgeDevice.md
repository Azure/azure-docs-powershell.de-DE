---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145513"
---
# <span data-ttu-id="1a027-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1a027-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="1a027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a027-102">SYNOPSIS</span></span>
<span data-ttu-id="1a027-103">Konfiguriert ein neues Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1a027-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="1a027-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a027-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a027-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a027-105">DESCRIPTION</span></span>
<span data-ttu-id="1a027-106">Das **Cmdlet "New-AzStackEdgeDevice"** konfiguriert ein neues Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1a027-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="1a027-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a027-107">EXAMPLES</span></span>

### <span data-ttu-id="1a027-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a027-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="1a027-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a027-109">PARAMETERS</span></span>

### <span data-ttu-id="1a027-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a027-110">-AsJob</span></span>
<span data-ttu-id="1a027-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a027-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a027-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a027-112">-DefaultProfile</span></span>
<span data-ttu-id="1a027-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a027-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a027-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1a027-114">-Location</span></span>
<span data-ttu-id="1a027-115">Position des Geräts</span><span class="sxs-lookup"><span data-stu-id="1a027-115">Location of the device</span></span>

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

### <span data-ttu-id="1a027-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1a027-116">-Name</span></span>
<span data-ttu-id="1a027-117">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="1a027-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a027-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a027-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a027-119">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="1a027-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1a027-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="1a027-120">-Sku</span></span>
<span data-ttu-id="1a027-121">Verfügbare SKU sind Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="1a027-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="1a027-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a027-122">-Confirm</span></span>
<span data-ttu-id="1a027-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a027-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a027-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a027-124">-WhatIf</span></span>
<span data-ttu-id="1a027-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a027-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a027-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a027-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a027-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a027-127">CommonParameters</span></span>
<span data-ttu-id="1a027-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a027-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a027-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a027-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a027-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a027-130">INPUTS</span></span>

### <span data-ttu-id="1a027-131">Keine</span><span class="sxs-lookup"><span data-stu-id="1a027-131">None</span></span>

## <span data-ttu-id="1a027-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a027-132">OUTPUTS</span></span>

### <span data-ttu-id="1a027-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1a027-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="1a027-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a027-134">NOTES</span></span>

## <span data-ttu-id="1a027-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a027-135">RELATED LINKS</span></span>
