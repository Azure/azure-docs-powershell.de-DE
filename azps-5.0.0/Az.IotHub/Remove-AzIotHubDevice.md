---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175534"
---
# <span data-ttu-id="942e8-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="942e8-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="942e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="942e8-102">SYNOPSIS</span></span>
<span data-ttu-id="942e8-103">Löschen Sie ein viel Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="942e8-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="942e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="942e8-104">SYNTAX</span></span>

### <span data-ttu-id="942e8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="942e8-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942e8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="942e8-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942e8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="942e8-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942e8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="942e8-108">DESCRIPTION</span></span>
<span data-ttu-id="942e8-109">Löschen Sie alle Geräte oder ein bestimmtes Gerät von einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="942e8-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="942e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="942e8-110">EXAMPLES</span></span>

### <span data-ttu-id="942e8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="942e8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="942e8-112">Löschen Sie alle viel Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="942e8-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="942e8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="942e8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="942e8-114">Löschen Sie ein viel Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="942e8-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="942e8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="942e8-115">PARAMETERS</span></span>

### <span data-ttu-id="942e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942e8-116">-DefaultProfile</span></span>
<span data-ttu-id="942e8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="942e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942e8-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="942e8-118">-DeviceId</span></span>
<span data-ttu-id="942e8-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="942e8-119">Target Device Id.</span></span>

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

### <span data-ttu-id="942e8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="942e8-120">-InputObject</span></span>
<span data-ttu-id="942e8-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="942e8-121">IotHub object</span></span>

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

### <span data-ttu-id="942e8-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="942e8-122">-IotHubName</span></span>
<span data-ttu-id="942e8-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="942e8-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="942e8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="942e8-124">-PassThru</span></span>
<span data-ttu-id="942e8-125">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="942e8-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="942e8-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="942e8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="942e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="942e8-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="942e8-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="942e8-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="942e8-129">-ResourceId</span></span>
<span data-ttu-id="942e8-130">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="942e8-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="942e8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="942e8-131">-Confirm</span></span>
<span data-ttu-id="942e8-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="942e8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942e8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942e8-133">-WhatIf</span></span>
<span data-ttu-id="942e8-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="942e8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942e8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="942e8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942e8-136">CommonParameters</span></span>
<span data-ttu-id="942e8-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="942e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942e8-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="942e8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942e8-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="942e8-139">INPUTS</span></span>

### <span data-ttu-id="942e8-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="942e8-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="942e8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="942e8-141">System.String</span></span>

## <span data-ttu-id="942e8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="942e8-142">OUTPUTS</span></span>

### <span data-ttu-id="942e8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="942e8-143">System.Boolean</span></span>

## <span data-ttu-id="942e8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="942e8-144">NOTES</span></span>

## <span data-ttu-id="942e8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="942e8-145">RELATED LINKS</span></span>
