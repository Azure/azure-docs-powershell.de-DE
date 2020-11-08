---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174799"
---
# <span data-ttu-id="5d5ff-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5d5ff-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="5d5ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5ff-103">Konfiguriert ein neues Edge-Gerät für Datenfelder</span><span class="sxs-lookup"><span data-stu-id="5d5ff-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="5d5ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d5ff-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="5d5ff-106">Das Cmdlet " **New-AzDataBoxEdgeDevice** " konfiguriert ein neues Edge-Gerät für Datenfelder</span><span class="sxs-lookup"><span data-stu-id="5d5ff-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="5d5ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="5d5ff-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d5ff-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="5d5ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d5ff-109">PARAMETERS</span></span>

### <span data-ttu-id="5d5ff-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d5ff-110">-AsJob</span></span>
<span data-ttu-id="5d5ff-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5d5ff-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d5ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5ff-112">-DefaultProfile</span></span>
<span data-ttu-id="5d5ff-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d5ff-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5ff-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="5d5ff-114">-Location</span></span>
<span data-ttu-id="5d5ff-115">Standort des Geräts</span><span class="sxs-lookup"><span data-stu-id="5d5ff-115">Location of the device</span></span>

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

### <span data-ttu-id="5d5ff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5d5ff-116">-Name</span></span>
<span data-ttu-id="5d5ff-117">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="5d5ff-117">Resource Name</span></span>

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

### <span data-ttu-id="5d5ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d5ff-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5d5ff-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5d5ff-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d5ff-120">-Sku</span></span>
<span data-ttu-id="5d5ff-121">Verfügbare SKUs sind Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="5d5ff-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="5d5ff-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d5ff-122">-Confirm</span></span>
<span data-ttu-id="5d5ff-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d5ff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5ff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5ff-124">-WhatIf</span></span>
<span data-ttu-id="5d5ff-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d5ff-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d5ff-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d5ff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5ff-127">CommonParameters</span></span>
<span data-ttu-id="5d5ff-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5ff-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d5ff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5ff-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d5ff-130">INPUTS</span></span>

### <span data-ttu-id="5d5ff-131">Keine</span><span class="sxs-lookup"><span data-stu-id="5d5ff-131">None</span></span>

## <span data-ttu-id="5d5ff-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d5ff-132">OUTPUTS</span></span>

### <span data-ttu-id="5d5ff-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5d5ff-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="5d5ff-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d5ff-134">NOTES</span></span>

## <span data-ttu-id="5d5ff-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d5ff-135">RELATED LINKS</span></span>
