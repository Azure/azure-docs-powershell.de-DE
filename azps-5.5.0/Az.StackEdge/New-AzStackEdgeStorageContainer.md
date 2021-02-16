---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155089"
---
# <span data-ttu-id="58c2d-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58c2d-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="58c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="58c2d-103">Erstellt einen neuen Speichercontainer im Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="58c2d-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="58c2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c2d-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c2d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="58c2d-106">Das **Cmdlet "New-AzStackEdgeStorageContainer"** erstellt einen neuen Speichercontainer im Edgespeicherkonto auf einem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="58c2d-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="58c2d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="58c2d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58c2d-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="58c2d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58c2d-109">PARAMETERS</span></span>

### <span data-ttu-id="58c2d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58c2d-110">-AsJob</span></span>
<span data-ttu-id="58c2d-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58c2d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58c2d-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="58c2d-112">-DataFormat</span></span>
<span data-ttu-id="58c2d-113">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="58c2d-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c2d-114">-DefaultProfile</span></span>
<span data-ttu-id="58c2d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c2d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c2d-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="58c2d-116">-DeviceName</span></span>
<span data-ttu-id="58c2d-117">Gerätename</span><span class="sxs-lookup"><span data-stu-id="58c2d-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c2d-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58c2d-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="58c2d-119">Bereitstellen des vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="58c2d-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c2d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="58c2d-120">-Name</span></span>
<span data-ttu-id="58c2d-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="58c2d-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="58c2d-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="58c2d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="58c2d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58c2d-124">-Confirm</span></span>
<span data-ttu-id="58c2d-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58c2d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c2d-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58c2d-126">-WhatIf</span></span>
<span data-ttu-id="58c2d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58c2d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58c2d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58c2d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c2d-129">CommonParameters</span></span>
<span data-ttu-id="58c2d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c2d-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58c2d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c2d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58c2d-132">INPUTS</span></span>

### <span data-ttu-id="58c2d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="58c2d-133">System.String</span></span>

## <span data-ttu-id="58c2d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58c2d-134">OUTPUTS</span></span>

### <span data-ttu-id="58c2d-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58c2d-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="58c2d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58c2d-136">NOTES</span></span>

## <span data-ttu-id="58c2d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58c2d-137">RELATED LINKS</span></span>
