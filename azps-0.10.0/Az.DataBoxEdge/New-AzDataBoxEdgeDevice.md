---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 353d4ca1e5f5eebd1cda1ec22d801a73db239963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844091"
---
# <span data-ttu-id="21719-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="21719-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="21719-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21719-102">SYNOPSIS</span></span>
<span data-ttu-id="21719-103">Konfiguriert ein neues Edge-Gerät für Datenfelder</span><span class="sxs-lookup"><span data-stu-id="21719-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="21719-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21719-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21719-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21719-105">DESCRIPTION</span></span>
<span data-ttu-id="21719-106">Das Cmdlet " **New-AzDataBoxEdgeDevice** " konfiguriert ein neues Edge-Gerät für Datenfelder</span><span class="sxs-lookup"><span data-stu-id="21719-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="21719-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21719-107">EXAMPLES</span></span>

### <span data-ttu-id="21719-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21719-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="21719-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="21719-109">PARAMETERS</span></span>

### <span data-ttu-id="21719-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21719-110">-AsJob</span></span>
<span data-ttu-id="21719-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="21719-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21719-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21719-112">-DefaultProfile</span></span>
<span data-ttu-id="21719-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21719-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21719-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="21719-114">-Location</span></span>
<span data-ttu-id="21719-115">Standort des Geräts</span><span class="sxs-lookup"><span data-stu-id="21719-115">Location of the device</span></span>

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

### <span data-ttu-id="21719-116">-Name</span><span class="sxs-lookup"><span data-stu-id="21719-116">-Name</span></span>
<span data-ttu-id="21719-117">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="21719-117">Resource Name</span></span>

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

### <span data-ttu-id="21719-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21719-118">-ResourceGroupName</span></span>
<span data-ttu-id="21719-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="21719-119">Resource Group Name</span></span>

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

### <span data-ttu-id="21719-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="21719-120">-Sku</span></span>
<span data-ttu-id="21719-121">Verfügbare SKUs sind Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="21719-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="21719-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21719-122">-Confirm</span></span>
<span data-ttu-id="21719-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21719-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21719-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21719-124">-WhatIf</span></span>
<span data-ttu-id="21719-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21719-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21719-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21719-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21719-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21719-127">CommonParameters</span></span>
<span data-ttu-id="21719-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21719-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21719-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21719-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21719-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21719-130">INPUTS</span></span>

### <span data-ttu-id="21719-131">Keine</span><span class="sxs-lookup"><span data-stu-id="21719-131">None</span></span>

## <span data-ttu-id="21719-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21719-132">OUTPUTS</span></span>

### <span data-ttu-id="21719-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="21719-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="21719-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="21719-134">NOTES</span></span>

## <span data-ttu-id="21719-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21719-135">RELATED LINKS</span></span>
