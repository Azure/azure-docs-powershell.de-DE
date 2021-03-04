---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949120"
---
# <span data-ttu-id="f0609-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="f0609-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="f0609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0609-102">SYNOPSIS</span></span>
<span data-ttu-id="f0609-103">Entfernen Sie Nicht-Edge-Geräte als untere Geräte vom angegebenen Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="f0609-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="f0609-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0609-104">SYNTAX</span></span>

### <span data-ttu-id="f0609-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0609-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0609-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0609-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0609-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f0609-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0609-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0609-108">DESCRIPTION</span></span>
<span data-ttu-id="f0609-109">Entfernen Sie alle oder erwähnten Nicht-Edge-Geräte als untere edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f0609-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="f0609-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0609-110">EXAMPLES</span></span>

### <span data-ttu-id="f0609-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0609-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="f0609-112">Entfernen Sie die erwähnten Geräte als Untergeräte des angegebenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f0609-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="f0609-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f0609-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="f0609-114">Entfernen Sie alle Nicht-Edge-Geräte als untere edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f0609-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="f0609-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0609-115">PARAMETERS</span></span>

### <span data-ttu-id="f0609-116">-Kinder</span><span class="sxs-lookup"><span data-stu-id="f0609-116">-Children</span></span>
<span data-ttu-id="f0609-117">Die Liste der untergeordneten Geräte (durch Kommas getrennt) umfasst nur Nicht-Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="f0609-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0609-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0609-118">-DefaultProfile</span></span>
<span data-ttu-id="f0609-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0609-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0609-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f0609-120">-DeviceId</span></span>
<span data-ttu-id="f0609-121">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="f0609-121">Id of edge device.</span></span>

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

### <span data-ttu-id="f0609-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0609-122">-InputObject</span></span>
<span data-ttu-id="f0609-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f0609-123">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0609-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f0609-124">-IotHubName</span></span>
<span data-ttu-id="f0609-125">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="f0609-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0609-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0609-126">-PassThru</span></span>
<span data-ttu-id="f0609-127">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="f0609-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="f0609-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f0609-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0609-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0609-129">-ResourceGroupName</span></span>
<span data-ttu-id="f0609-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f0609-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0609-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0609-131">-ResourceId</span></span>
<span data-ttu-id="f0609-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f0609-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0609-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0609-133">-Confirm</span></span>
<span data-ttu-id="f0609-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0609-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0609-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0609-135">-WhatIf</span></span>
<span data-ttu-id="f0609-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0609-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0609-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0609-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0609-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0609-138">CommonParameters</span></span>
<span data-ttu-id="f0609-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0609-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0609-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0609-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0609-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0609-141">INPUTS</span></span>

### <span data-ttu-id="f0609-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f0609-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f0609-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f0609-143">System.String</span></span>

## <span data-ttu-id="f0609-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0609-144">OUTPUTS</span></span>

### <span data-ttu-id="f0609-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0609-145">System.Boolean</span></span>

## <span data-ttu-id="f0609-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0609-146">NOTES</span></span>

## <span data-ttu-id="f0609-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0609-147">RELATED LINKS</span></span>
