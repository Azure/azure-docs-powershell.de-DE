---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293681"
---
# <span data-ttu-id="d941e-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d941e-101">New-AzIotHub</span></span>

## <span data-ttu-id="d941e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d941e-102">SYNOPSIS</span></span>
<span data-ttu-id="d941e-103">Erstellt einen neuen IotHub.</span><span class="sxs-lookup"><span data-stu-id="d941e-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="d941e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d941e-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d941e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d941e-105">DESCRIPTION</span></span>
<span data-ttu-id="d941e-106">Erstellt einen neuen IotHub.</span><span class="sxs-lookup"><span data-stu-id="d941e-106">Creates a new IotHub.</span></span>
<span data-ttu-id="d941e-107">Sie können IotHub mit den Standardeigenschaften erstellen oder die Eingabeeigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="d941e-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="d941e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d941e-108">EXAMPLES</span></span>

### <span data-ttu-id="d941e-109">Beispiel 1 Erstellen eines neuen IotHub mit Standardeigenschaften</span><span class="sxs-lookup"><span data-stu-id="d941e-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="d941e-110">Erstellt einen neuen IotHub mit dem Namen "myiothub" der SKU "S1", Kapazität 1 und Standort "northeurope", der in den Tags enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d941e-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="d941e-111">Beispiel 2 Erstellen eines neuen IotHub mit dem MaxDeliveryCount der CloudToDevice-Warteschlange, die auf 20 festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="d941e-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="d941e-112">Erstellt einen neuen IotHub mit dem Namen "myiothub" der SKU "S1", Kapazität 1 und Standort "northeurope" mit erweiterten Eingabeeigenschaften, die durch $properties.</span><span class="sxs-lookup"><span data-stu-id="d941e-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="d941e-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="d941e-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="d941e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d941e-114">PARAMETERS</span></span>

### <span data-ttu-id="d941e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d941e-115">-DefaultProfile</span></span>
<span data-ttu-id="d941e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d941e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d941e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d941e-117">-Location</span></span>
<span data-ttu-id="d941e-118">Speicherort, an dem der IoT-Hub erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d941e-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="d941e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d941e-119">-Name</span></span>
<span data-ttu-id="d941e-120">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="d941e-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="d941e-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="d941e-121">-Properties</span></span>
<span data-ttu-id="d941e-122">Eigenschaften des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="d941e-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="d941e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d941e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d941e-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d941e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d941e-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d941e-125">-SkuName</span></span>
<span data-ttu-id="d941e-126">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="d941e-126">Name of the sku</span></span>

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

### <span data-ttu-id="d941e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d941e-127">-Tag</span></span>
<span data-ttu-id="d941e-128">IoT-Hubinstanztags.</span><span class="sxs-lookup"><span data-stu-id="d941e-128">IoT hub instance tags.</span></span> <span data-ttu-id="d941e-129">Eigenschaftentasche in Schlüssel-Wert-Paaren in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d941e-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="d941e-130">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="d941e-130">-Units</span></span>
<span data-ttu-id="d941e-131">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="d941e-131">Number of units</span></span>

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

### <span data-ttu-id="d941e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d941e-132">-Confirm</span></span>
<span data-ttu-id="d941e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d941e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d941e-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d941e-134">-WhatIf</span></span>
<span data-ttu-id="d941e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d941e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d941e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d941e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d941e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d941e-137">CommonParameters</span></span>
<span data-ttu-id="d941e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d941e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d941e-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d941e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d941e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d941e-140">INPUTS</span></span>

### <span data-ttu-id="d941e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d941e-141">System.String</span></span>

## <span data-ttu-id="d941e-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d941e-142">OUTPUTS</span></span>

### <span data-ttu-id="d941e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d941e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d941e-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d941e-144">NOTES</span></span>

## <span data-ttu-id="d941e-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d941e-145">RELATED LINKS</span></span>
