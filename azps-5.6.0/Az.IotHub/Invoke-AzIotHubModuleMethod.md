---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: ea2362fc779ada8faf62c863ccffb9e58e078b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936795"
---
# <span data-ttu-id="081fd-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="081fd-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="081fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="081fd-102">SYNOPSIS</span></span>
<span data-ttu-id="081fd-103">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="081fd-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="081fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="081fd-104">SYNTAX</span></span>

### <span data-ttu-id="081fd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="081fd-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="081fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="081fd-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="081fd-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="081fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="081fd-108">DESCRIPTION</span></span>
<span data-ttu-id="081fd-109">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="081fd-109">Invoke an Edge module method.</span></span> <span data-ttu-id="081fd-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="081fd-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="081fd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="081fd-111">EXAMPLES</span></span>

### <span data-ttu-id="081fd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="081fd-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="081fd-113">Rufen Sie eine Edgemodulmethode auf.</span><span class="sxs-lookup"><span data-stu-id="081fd-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="081fd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="081fd-114">PARAMETERS</span></span>

### <span data-ttu-id="081fd-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="081fd-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="081fd-116">Die Anzahl der Sekunden, die gewartet werden müssen, bis eine Verbindung erfolgreich hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="081fd-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="081fd-117">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="081fd-117">Default is 10.</span></span>

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

### <span data-ttu-id="081fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081fd-118">-DefaultProfile</span></span>
<span data-ttu-id="081fd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="081fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081fd-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="081fd-120">-DeviceId</span></span>
<span data-ttu-id="081fd-121">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="081fd-121">Target Device Id.</span></span>

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

### <span data-ttu-id="081fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="081fd-122">-InputObject</span></span>
<span data-ttu-id="081fd-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="081fd-123">IotHub object</span></span>

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

### <span data-ttu-id="081fd-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="081fd-124">-IotHubName</span></span>
<span data-ttu-id="081fd-125">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="081fd-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="081fd-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="081fd-126">-ModuleId</span></span>
<span data-ttu-id="081fd-127">Die Modul-ID des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="081fd-127">Target device's module id.</span></span>

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

### <span data-ttu-id="081fd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="081fd-128">-Name</span></span>
<span data-ttu-id="081fd-129">Der Name der Methode, die auf diesem Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="081fd-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="081fd-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="081fd-130">-Payload</span></span>
<span data-ttu-id="081fd-131">Die Nutzlast für die Methode, die auf diesem Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="081fd-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="081fd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="081fd-132">-ResourceGroupName</span></span>
<span data-ttu-id="081fd-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="081fd-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="081fd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="081fd-134">-ResourceId</span></span>
<span data-ttu-id="081fd-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="081fd-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="081fd-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="081fd-136">-ResponseTimeOut</span></span>
<span data-ttu-id="081fd-137">Anzahl der Sekunden, die gewartet werden müssen, bis ein Ergebnis von der direkten Methode empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="081fd-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="081fd-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="081fd-138">Default is 10.</span></span>

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

### <span data-ttu-id="081fd-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="081fd-139">-Confirm</span></span>
<span data-ttu-id="081fd-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="081fd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="081fd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081fd-141">-WhatIf</span></span>
<span data-ttu-id="081fd-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="081fd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="081fd-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="081fd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="081fd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081fd-144">CommonParameters</span></span>
<span data-ttu-id="081fd-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081fd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081fd-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081fd-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081fd-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="081fd-147">INPUTS</span></span>

### <span data-ttu-id="081fd-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="081fd-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="081fd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="081fd-149">System.String</span></span>

## <span data-ttu-id="081fd-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="081fd-150">OUTPUTS</span></span>

### <span data-ttu-id="081fd-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="081fd-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="081fd-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="081fd-152">NOTES</span></span>

## <span data-ttu-id="081fd-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="081fd-153">RELATED LINKS</span></span>
