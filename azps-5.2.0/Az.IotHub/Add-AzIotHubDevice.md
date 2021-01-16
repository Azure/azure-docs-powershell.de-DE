---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299360"
---
# <span data-ttu-id="7f3ed-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7f3ed-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="7f3ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3ed-103">Erstellen Sie ein Gerät in einem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="7f3ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f3ed-104">SYNTAX</span></span>

### <span data-ttu-id="7f3ed-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f3ed-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3ed-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f3ed-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f3ed-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7f3ed-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f3ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f3ed-108">DESCRIPTION</span></span>
<span data-ttu-id="7f3ed-109">Erstellen Sie in einem IoT Hub ein Gerät mit einem anderen Autorisierungstyp.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="7f3ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f3ed-110">EXAMPLES</span></span>

### <span data-ttu-id="7f3ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f3ed-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="7f3ed-112">Erstellen Sie ein edgefähiges IoT-Gerät mit Standardautorisierung (geteilter privater Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="7f3ed-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="7f3ed-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f3ed-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="7f3ed-114">Erstellen Sie ein Gerät mit Stammzertifizierungsstelle mit deaktivierten Status und Grund.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="7f3ed-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7f3ed-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="7f3ed-116">Erstellen Sie ein edgefähiges IoT-Gerät, und fügen Sie diesem untergeordnete Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="7f3ed-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7f3ed-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="7f3ed-118">Erstellen Sie ein IoT-Gerät, und legen Sie dessen übergeordnetes Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="7f3ed-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f3ed-119">PARAMETERS</span></span>

### <span data-ttu-id="7f3ed-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="7f3ed-120">-AuthMethod</span></span>
<span data-ttu-id="7f3ed-121">Der Autorisierungstyp, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ed-122">-Children</span><span class="sxs-lookup"><span data-stu-id="7f3ed-122">-Children</span></span>
<span data-ttu-id="7f3ed-123">Die Liste der untergeordneten Geräte (durch Kommas getrennt) enthält nur Geräte, die keine Edgegeräte sind.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="7f3ed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3ed-124">-DefaultProfile</span></span>
<span data-ttu-id="7f3ed-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3ed-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7f3ed-126">-DeviceId</span></span>
<span data-ttu-id="7f3ed-127">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-127">Target Device Id.</span></span>

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

### <span data-ttu-id="7f3ed-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7f3ed-128">-EdgeEnabled</span></span>
<span data-ttu-id="7f3ed-129">Kennzeichnung zur Aktivierung von Rand.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7f3ed-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7f3ed-130">-Force</span></span>
<span data-ttu-id="7f3ed-131">Überschreibt das übergeordnete Gerät des Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="7f3ed-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f3ed-132">-InputObject</span></span>
<span data-ttu-id="7f3ed-133">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="7f3ed-133">IotHub object</span></span>

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

### <span data-ttu-id="7f3ed-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7f3ed-134">-IotHubName</span></span>
<span data-ttu-id="7f3ed-135">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="7f3ed-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7f3ed-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f3ed-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="7f3ed-137">Expliziter selbst signierter Zertifikatdrückdruck zur Verwendung für den Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="7f3ed-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="7f3ed-138">-ParentDeviceId</span></span>
<span data-ttu-id="7f3ed-139">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-139">Id of edge device.</span></span>

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

### <span data-ttu-id="7f3ed-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3ed-140">-ResourceGroupName</span></span>
<span data-ttu-id="7f3ed-141">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f3ed-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7f3ed-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f3ed-142">-ResourceId</span></span>
<span data-ttu-id="7f3ed-143">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7f3ed-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7f3ed-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f3ed-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="7f3ed-145">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="7f3ed-146">-Status</span><span class="sxs-lookup"><span data-stu-id="7f3ed-146">-Status</span></span>
<span data-ttu-id="7f3ed-147">Legen Sie den Gerätestatus beim Erstellen des Geräts ein.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ed-148">-Status 1</span><span class="sxs-lookup"><span data-stu-id="7f3ed-148">-StatusReason</span></span>
<span data-ttu-id="7f3ed-149">Beschreibung für den Gerätestatus.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-149">Description for device status.</span></span>

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

### <span data-ttu-id="7f3ed-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f3ed-150">-Confirm</span></span>
<span data-ttu-id="7f3ed-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3ed-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f3ed-152">-WhatIf</span></span>
<span data-ttu-id="7f3ed-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f3ed-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f3ed-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3ed-155">CommonParameters</span></span>
<span data-ttu-id="7f3ed-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3ed-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3ed-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3ed-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3ed-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f3ed-158">INPUTS</span></span>

### <span data-ttu-id="7f3ed-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7f3ed-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7f3ed-160">System.String</span><span class="sxs-lookup"><span data-stu-id="7f3ed-160">System.String</span></span>

## <span data-ttu-id="7f3ed-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f3ed-161">OUTPUTS</span></span>

### <span data-ttu-id="7f3ed-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung</span><span class="sxs-lookup"><span data-stu-id="7f3ed-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="7f3ed-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f3ed-163">NOTES</span></span>

## <span data-ttu-id="7f3ed-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f3ed-164">RELATED LINKS</span></span>
