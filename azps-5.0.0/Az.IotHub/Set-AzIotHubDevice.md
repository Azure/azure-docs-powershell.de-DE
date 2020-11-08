---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180455"
---
# <span data-ttu-id="2d98d-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2d98d-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="2d98d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d98d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d98d-103">Aktualisieren Sie ein viel Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="2d98d-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="2d98d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d98d-104">SYNTAX</span></span>

### <span data-ttu-id="2d98d-105">ResourceSetForStatus (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d98d-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="2d98d-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="2d98d-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2d98d-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="2d98d-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d98d-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2d98d-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="2d98d-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="2d98d-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d98d-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2d98d-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d98d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d98d-114">DESCRIPTION</span></span>
<span data-ttu-id="2d98d-115">Aktualisieren Sie ein viel Hub-Gerät.</span><span class="sxs-lookup"><span data-stu-id="2d98d-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="2d98d-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d98d-116">EXAMPLES</span></span>

### <span data-ttu-id="2d98d-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d98d-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="2d98d-118">Aktivieren der edgefunktionen für Geräte.</span><span class="sxs-lookup"><span data-stu-id="2d98d-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="2d98d-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2d98d-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="2d98d-120">Gerätestatus deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2d98d-120">Disable device status.</span></span>

### <span data-ttu-id="2d98d-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2d98d-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="2d98d-122">Aktualisieren des Autorisierungs Typs eines viel Hub-Geräts</span><span class="sxs-lookup"><span data-stu-id="2d98d-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="2d98d-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d98d-123">PARAMETERS</span></span>

### <span data-ttu-id="2d98d-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="2d98d-124">-AuthMethod</span></span>
<span data-ttu-id="2d98d-125">Der Autorisierungs, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d98d-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="2d98d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d98d-126">-DefaultProfile</span></span>
<span data-ttu-id="2d98d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d98d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d98d-128">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="2d98d-128">-DeviceId</span></span>
<span data-ttu-id="2d98d-129">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="2d98d-129">Target Device Id.</span></span>

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

### <span data-ttu-id="2d98d-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2d98d-130">-EdgeEnabled</span></span>
<span data-ttu-id="2d98d-131">Kennzeichen, das die Kanten Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="2d98d-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="2d98d-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d98d-132">-InputObject</span></span>
<span data-ttu-id="2d98d-133">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2d98d-133">IotHub object</span></span>

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

### <span data-ttu-id="2d98d-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2d98d-134">-IotHubName</span></span>
<span data-ttu-id="2d98d-135">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="2d98d-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2d98d-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="2d98d-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="2d98d-137">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für den Primärschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d98d-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="2d98d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d98d-138">-ResourceGroupName</span></span>
<span data-ttu-id="2d98d-139">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2d98d-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d98d-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d98d-140">-ResourceId</span></span>
<span data-ttu-id="2d98d-141">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2d98d-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2d98d-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="2d98d-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="2d98d-143">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für sekundären Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d98d-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="2d98d-144">-Status</span><span class="sxs-lookup"><span data-stu-id="2d98d-144">-Status</span></span>
<span data-ttu-id="2d98d-145">Einrichten des Gerätestatus bei der Erstellung</span><span class="sxs-lookup"><span data-stu-id="2d98d-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="2d98d-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="2d98d-146">-StatusReason</span></span>
<span data-ttu-id="2d98d-147">Beschreibung für den Gerätestatus</span><span class="sxs-lookup"><span data-stu-id="2d98d-147">Description for device status.</span></span>

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

### <span data-ttu-id="2d98d-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d98d-148">-Confirm</span></span>
<span data-ttu-id="2d98d-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d98d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d98d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d98d-150">-WhatIf</span></span>
<span data-ttu-id="2d98d-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d98d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d98d-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d98d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d98d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d98d-153">CommonParameters</span></span>
<span data-ttu-id="2d98d-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d98d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d98d-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d98d-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d98d-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d98d-156">INPUTS</span></span>

### <span data-ttu-id="2d98d-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2d98d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2d98d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2d98d-158">System.String</span></span>

## <span data-ttu-id="2d98d-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d98d-159">OUTPUTS</span></span>

### <span data-ttu-id="2d98d-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="2d98d-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="2d98d-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d98d-161">NOTES</span></span>

## <span data-ttu-id="2d98d-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d98d-162">RELATED LINKS</span></span>
