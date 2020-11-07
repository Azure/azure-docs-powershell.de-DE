---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: f3ee19d5389958741e8258db8b807acce7494ff8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650964"
---
# <span data-ttu-id="fa7fe-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="fa7fe-101">New-AzIotHub</span></span>

## <span data-ttu-id="fa7fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7fe-103">Erstellt eine neue IotHub.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="fa7fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa7fe-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="fa7fe-106">Erstellt eine neue IotHub.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-106">Creates a new IotHub.</span></span>
<span data-ttu-id="fa7fe-107">Sie können die IotHub entweder mit den Standardeigenschaften erstellen oder die Eingabeeigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="fa7fe-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa7fe-108">EXAMPLES</span></span>

### <span data-ttu-id="fa7fe-109">Beispiel 1 Erstellen eines neuen IotHub mit Standardeigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa7fe-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="fa7fe-110">Erstellt eine neue IotHub mit dem Namen "myiothub" der SKU "S1", Capacity 1 und Location "northeurope".</span><span class="sxs-lookup"><span data-stu-id="fa7fe-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="fa7fe-111">Beispiel 2 Erstellen eines neuen IotHub, wobei die MaxDeliveryCount der CloudToDevice-Warteschlange auf 20 gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="fa7fe-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="fa7fe-112">Erstellt eine neue IotHub mit dem Namen "myiothub" der SKU "S1", Capacity 1 und Location "northeurope" mit erweiterten Eingabeeigenschaften, die durch $Properties dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="fa7fe-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. psCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $Properties = New-Object Microsoft. Azure. Commands. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-Einheiten 1-Standort "northeurope"-Eigenschaften $Properties</span><span class="sxs-lookup"><span data-stu-id="fa7fe-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="fa7fe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa7fe-114">PARAMETERS</span></span>

### <span data-ttu-id="fa7fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7fe-115">-DefaultProfile</span></span>
<span data-ttu-id="fa7fe-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fa7fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa7fe-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="fa7fe-117">-Location</span></span>
<span data-ttu-id="fa7fe-118">Ort, an dem der viel-Hub erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="fa7fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fa7fe-119">-Name</span></span>
<span data-ttu-id="fa7fe-120">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="fa7fe-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-121">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa7fe-121">-Properties</span></span>
<span data-ttu-id="fa7fe-122">Eigenschaften des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa7fe-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fa7fe-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fa7fe-125">-SkuName</span></span>
<span data-ttu-id="fa7fe-126">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="fa7fe-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-127">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="fa7fe-127">-Units</span></span>
<span data-ttu-id="fa7fe-128">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="fa7fe-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa7fe-129">-Confirm</span></span>
<span data-ttu-id="fa7fe-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7fe-131">-WhatIf</span></span>
<span data-ttu-id="fa7fe-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7fe-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7fe-134">CommonParameters</span></span>
<span data-ttu-id="fa7fe-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7fe-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa7fe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7fe-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa7fe-137">INPUTS</span></span>

### <span data-ttu-id="fa7fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fa7fe-138">System.String</span></span>

## <span data-ttu-id="fa7fe-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa7fe-139">OUTPUTS</span></span>

### <span data-ttu-id="fa7fe-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fa7fe-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="fa7fe-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa7fe-141">NOTES</span></span>

## <span data-ttu-id="fa7fe-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa7fe-142">RELATED LINKS</span></span>
