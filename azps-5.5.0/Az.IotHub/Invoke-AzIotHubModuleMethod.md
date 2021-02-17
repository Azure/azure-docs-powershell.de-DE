---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147804"
---
# <span data-ttu-id="cadda-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="cadda-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="cadda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadda-102">SYNOPSIS</span></span>
<span data-ttu-id="cadda-103">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="cadda-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="cadda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cadda-104">SYNTAX</span></span>

### <span data-ttu-id="cadda-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cadda-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cadda-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cadda-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cadda-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cadda-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadda-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cadda-108">DESCRIPTION</span></span>
<span data-ttu-id="cadda-109">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="cadda-109">Invoke an Edge module method.</span></span> <span data-ttu-id="cadda-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="cadda-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="cadda-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cadda-111">EXAMPLES</span></span>

### <span data-ttu-id="cadda-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cadda-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="cadda-113">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="cadda-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="cadda-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cadda-114">PARAMETERS</span></span>

### <span data-ttu-id="cadda-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="cadda-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="cadda-116">Anzahl der Sekunden, die gewartet werden muss, bis eine Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cadda-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="cadda-117">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="cadda-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadda-118">-DefaultProfile</span></span>
<span data-ttu-id="cadda-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cadda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cadda-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cadda-120">-DeviceId</span></span>
<span data-ttu-id="cadda-121">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="cadda-121">Target Device Id.</span></span>

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

### <span data-ttu-id="cadda-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cadda-122">-InputObject</span></span>
<span data-ttu-id="cadda-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="cadda-123">IotHub object</span></span>

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

### <span data-ttu-id="cadda-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cadda-124">-IotHubName</span></span>
<span data-ttu-id="cadda-125">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="cadda-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cadda-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="cadda-126">-ModuleId</span></span>
<span data-ttu-id="cadda-127">Die Modul-ID des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="cadda-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadda-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cadda-128">-Name</span></span>
<span data-ttu-id="cadda-129">Der Name der Methode, die in diesem Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cadda-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="cadda-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="cadda-130">-Payload</span></span>
<span data-ttu-id="cadda-131">Die Nutzlast für die methode, die in diesem Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cadda-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="cadda-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadda-132">-ResourceGroupName</span></span>
<span data-ttu-id="cadda-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cadda-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cadda-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cadda-134">-ResourceId</span></span>
<span data-ttu-id="cadda-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="cadda-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cadda-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="cadda-136">-ResponseTimeOut</span></span>
<span data-ttu-id="cadda-137">Anzahl der Sekunden, die gewartet werden muss, bis ein Ergebnis von der direkten Methode empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="cadda-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="cadda-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="cadda-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadda-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cadda-139">-Confirm</span></span>
<span data-ttu-id="cadda-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cadda-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadda-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cadda-141">-WhatIf</span></span>
<span data-ttu-id="cadda-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cadda-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadda-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cadda-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadda-144">CommonParameters</span></span>
<span data-ttu-id="cadda-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadda-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadda-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadda-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cadda-147">INPUTS</span></span>

### <span data-ttu-id="cadda-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cadda-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cadda-149">System.String</span><span class="sxs-lookup"><span data-stu-id="cadda-149">System.String</span></span>

## <span data-ttu-id="cadda-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cadda-150">OUTPUTS</span></span>

### <span data-ttu-id="cadda-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="cadda-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="cadda-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cadda-152">NOTES</span></span>

## <span data-ttu-id="cadda-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cadda-153">RELATED LINKS</span></span>
