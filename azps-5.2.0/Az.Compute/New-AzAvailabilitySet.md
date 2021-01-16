---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368834"
---
# <span data-ttu-id="72b8f-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72b8f-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="72b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="72b8f-103">Erstellt einen Azure-Verfügbarkeitssatz.</span><span class="sxs-lookup"><span data-stu-id="72b8f-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="72b8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72b8f-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72b8f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="72b8f-106">Das **Cmdlet "New-AzAvailabilitySet"** erstellt einen Azure-Verfügbarkeitssatz.</span><span class="sxs-lookup"><span data-stu-id="72b8f-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="72b8f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="72b8f-108">Beispiel 1: Erstellen eines Verfügbarkeitssets</span><span class="sxs-lookup"><span data-stu-id="72b8f-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="72b8f-109">Mit diesem Befehl wird ein Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" erstellt.</span><span class="sxs-lookup"><span data-stu-id="72b8f-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="72b8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="72b8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72b8f-111">-AsJob</span></span>
<span data-ttu-id="72b8f-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="72b8f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="72b8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b8f-113">-DefaultProfile</span></span>
<span data-ttu-id="72b8f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72b8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72b8f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="72b8f-115">-Location</span></span>
<span data-ttu-id="72b8f-116">Gibt den Speicherort für den Verfügbarkeitssatz an.</span><span class="sxs-lookup"><span data-stu-id="72b8f-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="72b8f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="72b8f-117">-Name</span></span>
<span data-ttu-id="72b8f-118">Gibt einen Namen für den Verfügbarkeitssatz an.</span><span class="sxs-lookup"><span data-stu-id="72b8f-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8f-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="72b8f-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="72b8f-120">Gibt die Anzahl der Plattformfehlerdomänen an.</span><span class="sxs-lookup"><span data-stu-id="72b8f-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8f-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="72b8f-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="72b8f-122">Gibt die Anzahl der Domänen der Plattformaktualisierung an.</span><span class="sxs-lookup"><span data-stu-id="72b8f-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8f-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="72b8f-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="72b8f-124">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die mit diesem Verfügbarkeitssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72b8f-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="72b8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="72b8f-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72b8f-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="72b8f-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="72b8f-127">-Sku</span></span>
<span data-ttu-id="72b8f-128">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="72b8f-128">The Name of Sku.</span></span>
<span data-ttu-id="72b8f-129">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="72b8f-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72b8f-130">Ausgerichtet: Für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="72b8f-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="72b8f-131">Klassisch: Für nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="72b8f-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="72b8f-132">-Tag</span></span>
<span data-ttu-id="72b8f-133">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="72b8f-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="72b8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b8f-134">CommonParameters</span></span>
<span data-ttu-id="72b8f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b8f-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72b8f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b8f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72b8f-137">INPUTS</span></span>

### <span data-ttu-id="72b8f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="72b8f-138">System.String</span></span>

### <span data-ttu-id="72b8f-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="72b8f-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="72b8f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72b8f-140">OUTPUTS</span></span>

### <span data-ttu-id="72b8f-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72b8f-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="72b8f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72b8f-142">NOTES</span></span>

## <span data-ttu-id="72b8f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72b8f-143">RELATED LINKS</span></span>

[<span data-ttu-id="72b8f-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72b8f-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="72b8f-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72b8f-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


