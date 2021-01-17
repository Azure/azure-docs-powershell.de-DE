---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386559"
---
# <span data-ttu-id="c60b5-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="c60b5-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="c60b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c60b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c60b5-103">Aktualisieren Sie ein IoT Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="c60b5-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="c60b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c60b5-104">SYNTAX</span></span>

### <span data-ttu-id="c60b5-105">ResourceSetForStatus (Standard)</span><span class="sxs-lookup"><span data-stu-id="c60b5-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="c60b5-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="c60b5-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="c60b5-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="c60b5-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c60b5-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="c60b5-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="c60b5-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="c60b5-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60b5-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="c60b5-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60b5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c60b5-114">DESCRIPTION</span></span>
<span data-ttu-id="c60b5-115">Aktualisieren Sie ein IoT Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="c60b5-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="c60b5-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c60b5-116">EXAMPLES</span></span>

### <span data-ttu-id="c60b5-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c60b5-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="c60b5-118">Aktivieren Sie Edgefunktionen für Geräte.</span><span class="sxs-lookup"><span data-stu-id="c60b5-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="c60b5-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c60b5-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="c60b5-120">"Gerätestatus deaktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="c60b5-120">Disable device status.</span></span>

### <span data-ttu-id="c60b5-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c60b5-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="c60b5-122">Aktualisieren sie den Autorisierungstyp eines Iot Hub-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c60b5-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="c60b5-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c60b5-123">PARAMETERS</span></span>

### <span data-ttu-id="c60b5-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="c60b5-124">-AuthMethod</span></span>
<span data-ttu-id="c60b5-125">Der Autorisierungstyp, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c60b5-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="c60b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60b5-126">-DefaultProfile</span></span>
<span data-ttu-id="c60b5-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c60b5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c60b5-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c60b5-128">-DeviceId</span></span>
<span data-ttu-id="c60b5-129">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="c60b5-129">Target Device Id.</span></span>

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

### <span data-ttu-id="c60b5-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="c60b5-130">-EdgeEnabled</span></span>
<span data-ttu-id="c60b5-131">Kennzeichnung zur Aktivierung der Kante.</span><span class="sxs-lookup"><span data-stu-id="c60b5-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="c60b5-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c60b5-132">-InputObject</span></span>
<span data-ttu-id="c60b5-133">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="c60b5-133">IotHub object</span></span>

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

### <span data-ttu-id="c60b5-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c60b5-134">-IotHubName</span></span>
<span data-ttu-id="c60b5-135">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="c60b5-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c60b5-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="c60b5-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="c60b5-137">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c60b5-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="c60b5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60b5-138">-ResourceGroupName</span></span>
<span data-ttu-id="c60b5-139">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c60b5-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c60b5-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c60b5-140">-ResourceId</span></span>
<span data-ttu-id="c60b5-141">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c60b5-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c60b5-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="c60b5-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="c60b5-143">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c60b5-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="c60b5-144">-Status</span><span class="sxs-lookup"><span data-stu-id="c60b5-144">-Status</span></span>
<span data-ttu-id="c60b5-145">Legen Sie den Gerätestatus beim Erstellen des Geräts ein.</span><span class="sxs-lookup"><span data-stu-id="c60b5-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="c60b5-146">-Status 1</span><span class="sxs-lookup"><span data-stu-id="c60b5-146">-StatusReason</span></span>
<span data-ttu-id="c60b5-147">Beschreibung für den Gerätestatus.</span><span class="sxs-lookup"><span data-stu-id="c60b5-147">Description for device status.</span></span>

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

### <span data-ttu-id="c60b5-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c60b5-148">-Confirm</span></span>
<span data-ttu-id="c60b5-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c60b5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60b5-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c60b5-150">-WhatIf</span></span>
<span data-ttu-id="c60b5-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c60b5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c60b5-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c60b5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60b5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60b5-153">CommonParameters</span></span>
<span data-ttu-id="c60b5-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60b5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60b5-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c60b5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60b5-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c60b5-156">INPUTS</span></span>

### <span data-ttu-id="c60b5-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c60b5-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c60b5-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c60b5-158">System.String</span></span>

## <span data-ttu-id="c60b5-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c60b5-159">OUTPUTS</span></span>

### <span data-ttu-id="c60b5-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung</span><span class="sxs-lookup"><span data-stu-id="c60b5-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="c60b5-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c60b5-161">NOTES</span></span>

## <span data-ttu-id="c60b5-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c60b5-162">RELATED LINKS</span></span>
