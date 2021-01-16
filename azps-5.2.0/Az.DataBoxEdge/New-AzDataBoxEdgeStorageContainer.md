---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307843"
---
# <span data-ttu-id="b51cd-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b51cd-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="b51cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b51cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b51cd-103">Erstellt einen neuen Speichercontainer im Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="b51cd-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="b51cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b51cd-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b51cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b51cd-105">DESCRIPTION</span></span>
<span data-ttu-id="b51cd-106">Das **Cmdlet "New-AzDataBoxEdgeStorageContainer"** erstellt einen neuen Speichercontainer im Edgespeicherkonto auf einem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b51cd-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="b51cd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b51cd-107">EXAMPLES</span></span>

### <span data-ttu-id="b51cd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b51cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="b51cd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b51cd-109">PARAMETERS</span></span>

### <span data-ttu-id="b51cd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b51cd-110">-AsJob</span></span>
<span data-ttu-id="b51cd-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b51cd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b51cd-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="b51cd-112">-DataFormat</span></span>
<span data-ttu-id="b51cd-113">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="b51cd-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="b51cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51cd-114">-DefaultProfile</span></span>
<span data-ttu-id="b51cd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b51cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b51cd-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b51cd-116">-DeviceName</span></span>
<span data-ttu-id="b51cd-117">Gerätename</span><span class="sxs-lookup"><span data-stu-id="b51cd-117">Device Name</span></span>

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

### <span data-ttu-id="b51cd-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b51cd-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="b51cd-119">Bereitstellen des vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="b51cd-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="b51cd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b51cd-120">-Name</span></span>
<span data-ttu-id="b51cd-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b51cd-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="b51cd-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b51cd-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b51cd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b51cd-124">-Confirm</span></span>
<span data-ttu-id="b51cd-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b51cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b51cd-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b51cd-126">-WhatIf</span></span>
<span data-ttu-id="b51cd-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b51cd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b51cd-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b51cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b51cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51cd-129">CommonParameters</span></span>
<span data-ttu-id="b51cd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b51cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51cd-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b51cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51cd-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b51cd-132">INPUTS</span></span>

### <span data-ttu-id="b51cd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b51cd-133">System.String</span></span>

## <span data-ttu-id="b51cd-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b51cd-134">OUTPUTS</span></span>

### <span data-ttu-id="b51cd-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b51cd-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="b51cd-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b51cd-136">NOTES</span></span>

## <span data-ttu-id="b51cd-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b51cd-137">RELATED LINKS</span></span>
