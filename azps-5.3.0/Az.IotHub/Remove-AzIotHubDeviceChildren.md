---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386699"
---
# <span data-ttu-id="afbec-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="afbec-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="afbec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbec-102">SYNOPSIS</span></span>
<span data-ttu-id="afbec-103">Entfernen Sie Nicht-Edge-Geräte als untere Geräte von einem bestimmten Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="afbec-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="afbec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afbec-104">SYNTAX</span></span>

### <span data-ttu-id="afbec-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afbec-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afbec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afbec-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afbec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afbec-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afbec-108">DESCRIPTION</span></span>
<span data-ttu-id="afbec-109">Entfernen Sie alle oder erwähnten Geräte, die keine Edgegeräte sind, als von Ihnen angegebene Edgegeräte.</span><span class="sxs-lookup"><span data-stu-id="afbec-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="afbec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afbec-110">EXAMPLES</span></span>

### <span data-ttu-id="afbec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afbec-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="afbec-112">Entfernen erwähnter Geräte als untere Geräte des angegebenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="afbec-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="afbec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="afbec-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="afbec-114">Entfernen Sie alle Nicht-Edge-Geräte als von Ihnen angegebene Edgegeräte.</span><span class="sxs-lookup"><span data-stu-id="afbec-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="afbec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afbec-115">PARAMETERS</span></span>

### <span data-ttu-id="afbec-116">-Children</span><span class="sxs-lookup"><span data-stu-id="afbec-116">-Children</span></span>
<span data-ttu-id="afbec-117">Die Liste untergeordneter Geräte (durch Kommas getrennt) schließt nur Geräte ein, die keine Edgegeräte sind.</span><span class="sxs-lookup"><span data-stu-id="afbec-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="afbec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbec-118">-DefaultProfile</span></span>
<span data-ttu-id="afbec-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afbec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afbec-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="afbec-120">-DeviceId</span></span>
<span data-ttu-id="afbec-121">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="afbec-121">Id of edge device.</span></span>

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

### <span data-ttu-id="afbec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afbec-122">-InputObject</span></span>
<span data-ttu-id="afbec-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="afbec-123">IotHub object</span></span>

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

### <span data-ttu-id="afbec-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="afbec-124">-IotHubName</span></span>
<span data-ttu-id="afbec-125">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="afbec-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="afbec-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afbec-126">-PassThru</span></span>
<span data-ttu-id="afbec-127">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="afbec-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="afbec-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="afbec-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afbec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afbec-129">-ResourceGroupName</span></span>
<span data-ttu-id="afbec-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="afbec-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="afbec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afbec-131">-ResourceId</span></span>
<span data-ttu-id="afbec-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="afbec-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="afbec-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afbec-133">-Confirm</span></span>
<span data-ttu-id="afbec-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afbec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afbec-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="afbec-135">-WhatIf</span></span>
<span data-ttu-id="afbec-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afbec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afbec-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afbec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afbec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbec-138">CommonParameters</span></span>
<span data-ttu-id="afbec-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbec-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbec-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afbec-141">INPUTS</span></span>

### <span data-ttu-id="afbec-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="afbec-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="afbec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="afbec-143">System.String</span></span>

## <span data-ttu-id="afbec-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afbec-144">OUTPUTS</span></span>

### <span data-ttu-id="afbec-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afbec-145">System.Boolean</span></span>

## <span data-ttu-id="afbec-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afbec-146">NOTES</span></span>

## <span data-ttu-id="afbec-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afbec-147">RELATED LINKS</span></span>
