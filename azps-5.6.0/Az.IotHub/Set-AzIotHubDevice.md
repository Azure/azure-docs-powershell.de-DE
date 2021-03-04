---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: c164286e71b198ab19dd1928d6ee495014295306
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920547"
---
# <span data-ttu-id="16f13-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="16f13-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="16f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16f13-102">SYNOPSIS</span></span>
<span data-ttu-id="16f13-103">Aktualisieren sie ein IoT Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="16f13-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="16f13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16f13-104">SYNTAX</span></span>

### <span data-ttu-id="16f13-105">ResourceSetForStatus (Standard)</span><span class="sxs-lookup"><span data-stu-id="16f13-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="16f13-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="16f13-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="16f13-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="16f13-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16f13-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="16f13-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="16f13-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="16f13-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f13-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="16f13-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f13-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16f13-114">DESCRIPTION</span></span>
<span data-ttu-id="16f13-115">Aktualisieren sie ein IoT Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="16f13-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="16f13-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16f13-116">EXAMPLES</span></span>

### <span data-ttu-id="16f13-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16f13-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="16f13-118">Aktivieren Sie die Edgefunktionen für Geräte.</span><span class="sxs-lookup"><span data-stu-id="16f13-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="16f13-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16f13-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="16f13-120">Deaktivieren Sie den Gerätestatus.</span><span class="sxs-lookup"><span data-stu-id="16f13-120">Disable device status.</span></span>

### <span data-ttu-id="16f13-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="16f13-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="16f13-122">Aktualisieren des Autorisierungstyps eines Iot Hub-Geräts</span><span class="sxs-lookup"><span data-stu-id="16f13-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="16f13-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16f13-123">PARAMETERS</span></span>

### <span data-ttu-id="16f13-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="16f13-124">-AuthMethod</span></span>
<span data-ttu-id="16f13-125">Der Autorisierungstyp, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16f13-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f13-126">-DefaultProfile</span></span>
<span data-ttu-id="16f13-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16f13-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f13-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="16f13-128">-DeviceId</span></span>
<span data-ttu-id="16f13-129">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="16f13-129">Target Device Id.</span></span>

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

### <span data-ttu-id="16f13-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="16f13-130">-EdgeEnabled</span></span>
<span data-ttu-id="16f13-131">Kennzeichnen, das die Edge-Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="16f13-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16f13-132">-InputObject</span></span>
<span data-ttu-id="16f13-133">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="16f13-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="16f13-134">-IotHubName</span></span>
<span data-ttu-id="16f13-135">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="16f13-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="16f13-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="16f13-137">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="16f13-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f13-138">-ResourceGroupName</span></span>
<span data-ttu-id="16f13-139">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="16f13-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16f13-140">-ResourceId</span></span>
<span data-ttu-id="16f13-141">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="16f13-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="16f13-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="16f13-143">Expliziter selbst signierter Zertifikat-Fingerabdruck zur Verwendung für sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="16f13-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-144">-Status</span><span class="sxs-lookup"><span data-stu-id="16f13-144">-Status</span></span>
<span data-ttu-id="16f13-145">Legen Sie den Gerätestatus bei der Erstellung ein.</span><span class="sxs-lookup"><span data-stu-id="16f13-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="16f13-146">-StatusReason</span></span>
<span data-ttu-id="16f13-147">Beschreibung für den Gerätestatus.</span><span class="sxs-lookup"><span data-stu-id="16f13-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f13-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16f13-148">-Confirm</span></span>
<span data-ttu-id="16f13-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16f13-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f13-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f13-150">-WhatIf</span></span>
<span data-ttu-id="16f13-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16f13-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f13-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16f13-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f13-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f13-153">CommonParameters</span></span>
<span data-ttu-id="16f13-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f13-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f13-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f13-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f13-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16f13-156">INPUTS</span></span>

### <span data-ttu-id="16f13-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="16f13-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="16f13-158">System.String</span><span class="sxs-lookup"><span data-stu-id="16f13-158">System.String</span></span>

## <span data-ttu-id="16f13-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16f13-159">OUTPUTS</span></span>

### <span data-ttu-id="16f13-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="16f13-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="16f13-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="16f13-161">NOTES</span></span>

## <span data-ttu-id="16f13-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="16f13-162">RELATED LINKS</span></span>
