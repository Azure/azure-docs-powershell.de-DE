---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159652"
---
# <span data-ttu-id="d9ec5-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="d9ec5-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="d9ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ec5-103">Rufen Sie eine direkte Methode auf einem Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="d9ec5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9ec5-104">SYNTAX</span></span>

### <span data-ttu-id="d9ec5-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9ec5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9ec5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9ec5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ec5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9ec5-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ec5-109">Rufen Sie eine direkte Methode auf einem Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="d9ec5-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="d9ec5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9ec5-111">EXAMPLES</span></span>

### <span data-ttu-id="d9ec5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9ec5-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="d9ec5-113">Rufen Sie eine Gerätemethode auf.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-113">Invoke a device method.</span></span>

## <span data-ttu-id="d9ec5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ec5-114">PARAMETERS</span></span>

### <span data-ttu-id="d9ec5-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="d9ec5-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="d9ec5-116">Anzahl der Sekunden, die gewartet werden muss, bis eine Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="d9ec5-117">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-117">Default is 10.</span></span>

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

### <span data-ttu-id="d9ec5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ec5-118">-DefaultProfile</span></span>
<span data-ttu-id="d9ec5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ec5-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d9ec5-120">-DeviceId</span></span>
<span data-ttu-id="d9ec5-121">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-121">Target Device Id.</span></span>

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

### <span data-ttu-id="d9ec5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ec5-122">-InputObject</span></span>
<span data-ttu-id="d9ec5-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="d9ec5-123">IotHub object</span></span>

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

### <span data-ttu-id="d9ec5-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d9ec5-124">-IotHubName</span></span>
<span data-ttu-id="d9ec5-125">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="d9ec5-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9ec5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ec5-126">-Name</span></span>
<span data-ttu-id="d9ec5-127">Der Name der Methode, die auf diesem Gerät aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="d9ec5-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="d9ec5-128">-Payload</span></span>
<span data-ttu-id="d9ec5-129">Die Nutzlast für die methode, die auf diesem Gerät aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="d9ec5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ec5-130">-ResourceGroupName</span></span>
<span data-ttu-id="d9ec5-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d9ec5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9ec5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ec5-132">-ResourceId</span></span>
<span data-ttu-id="d9ec5-133">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d9ec5-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9ec5-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="d9ec5-134">-ResponseTimeOut</span></span>
<span data-ttu-id="d9ec5-135">Anzahl der Sekunden, die gewartet werden muss, bis ein Ergebnis von der direkten Methode empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="d9ec5-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-136">Default is 10.</span></span>

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

### <span data-ttu-id="d9ec5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9ec5-137">-Confirm</span></span>
<span data-ttu-id="d9ec5-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ec5-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9ec5-139">-WhatIf</span></span>
<span data-ttu-id="d9ec5-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ec5-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ec5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ec5-142">CommonParameters</span></span>
<span data-ttu-id="d9ec5-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ec5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ec5-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ec5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ec5-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ec5-145">INPUTS</span></span>

### <span data-ttu-id="d9ec5-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9ec5-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d9ec5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ec5-147">System.String</span></span>

## <span data-ttu-id="d9ec5-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ec5-148">OUTPUTS</span></span>

### <span data-ttu-id="d9ec5-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="d9ec5-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="d9ec5-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9ec5-150">NOTES</span></span>

## <span data-ttu-id="d9ec5-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9ec5-151">RELATED LINKS</span></span>
