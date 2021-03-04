---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 15a8f9aa8ed3c0746b402b29967999d395794fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946555"
---
# <span data-ttu-id="e7168-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e7168-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="e7168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7168-102">SYNOPSIS</span></span>
<span data-ttu-id="e7168-103">Löschen Sie ein IoT Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e7168-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="e7168-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7168-104">SYNTAX</span></span>

### <span data-ttu-id="e7168-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7168-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7168-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e7168-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7168-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e7168-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7168-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7168-108">DESCRIPTION</span></span>
<span data-ttu-id="e7168-109">Löschen Sie alle Geräte oder ein bestimmtes Gerät aus einem Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="e7168-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="e7168-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7168-110">EXAMPLES</span></span>

### <span data-ttu-id="e7168-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7168-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="e7168-112">Löschen Sie alle Iot Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="e7168-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="e7168-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e7168-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="e7168-114">Löschen Sie ein Iot Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e7168-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="e7168-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7168-115">PARAMETERS</span></span>

### <span data-ttu-id="e7168-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7168-116">-DefaultProfile</span></span>
<span data-ttu-id="e7168-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7168-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7168-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e7168-118">-DeviceId</span></span>
<span data-ttu-id="e7168-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="e7168-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7168-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7168-120">-InputObject</span></span>
<span data-ttu-id="e7168-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e7168-121">IotHub object</span></span>

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

### <span data-ttu-id="e7168-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e7168-122">-IotHubName</span></span>
<span data-ttu-id="e7168-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="e7168-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e7168-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7168-124">-PassThru</span></span>
<span data-ttu-id="e7168-125">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7168-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="e7168-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e7168-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7168-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7168-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7168-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e7168-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e7168-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7168-129">-ResourceId</span></span>
<span data-ttu-id="e7168-130">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e7168-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e7168-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7168-131">-Confirm</span></span>
<span data-ttu-id="e7168-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7168-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7168-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7168-133">-WhatIf</span></span>
<span data-ttu-id="e7168-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7168-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7168-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7168-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7168-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7168-136">CommonParameters</span></span>
<span data-ttu-id="e7168-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7168-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7168-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7168-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7168-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7168-139">INPUTS</span></span>

### <span data-ttu-id="e7168-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e7168-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e7168-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e7168-141">System.String</span></span>

## <span data-ttu-id="e7168-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7168-142">OUTPUTS</span></span>

### <span data-ttu-id="e7168-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7168-143">System.Boolean</span></span>

## <span data-ttu-id="e7168-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7168-144">NOTES</span></span>

## <span data-ttu-id="e7168-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7168-145">RELATED LINKS</span></span>
