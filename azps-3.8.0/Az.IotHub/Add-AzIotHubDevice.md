---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004547"
---
# <span data-ttu-id="ecdf9-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ecdf9-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="ecdf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdf9-103">Erstellen Sie ein Gerät in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="ecdf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecdf9-104">SYNTAX</span></span>

### <span data-ttu-id="ecdf9-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecdf9-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecdf9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecdf9-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecdf9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ecdf9-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecdf9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecdf9-108">DESCRIPTION</span></span>
<span data-ttu-id="ecdf9-109">Erstellen Sie ein Gerät mit einem anderen Autorisierungs in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="ecdf9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecdf9-110">EXAMPLES</span></span>

### <span data-ttu-id="ecdf9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecdf9-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="ecdf9-112">Erstellen eines Edge-fähigen viel Geräts mit Standard Autorisierung (freigegebener privater Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="ecdf9-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="ecdf9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ecdf9-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="ecdf9-114">Erstellen Sie ein viel Gerät mit einer Root-CA-Autorisierung mit deaktiviertem Status und Grund.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="ecdf9-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ecdf9-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="ecdf9-116">Erstellen Sie ein Edge-fähiges viel-Gerät, und fügen Sie ihm untergeordnete Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="ecdf9-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ecdf9-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="ecdf9-118">Erstellen Sie ein viel Gerät, und legen Sie das übergeordnete Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="ecdf9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecdf9-119">PARAMETERS</span></span>

### <span data-ttu-id="ecdf9-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="ecdf9-120">-AuthMethod</span></span>
<span data-ttu-id="ecdf9-121">Der Autorisierungs, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="ecdf9-122">-Kinder</span><span class="sxs-lookup"><span data-stu-id="ecdf9-122">-Children</span></span>
<span data-ttu-id="ecdf9-123">Liste der untergeordneten Geräte hinzufügen (durch Kommas getrennt) enthält nur nicht-Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="ecdf9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdf9-124">-DefaultProfile</span></span>
<span data-ttu-id="ecdf9-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecdf9-126">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="ecdf9-126">-DeviceId</span></span>
<span data-ttu-id="ecdf9-127">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-127">Target Device Id.</span></span>

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

### <span data-ttu-id="ecdf9-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ecdf9-128">-EdgeEnabled</span></span>
<span data-ttu-id="ecdf9-129">Kennzeichen, das die Kanten Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="ecdf9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ecdf9-130">-Force</span></span>
<span data-ttu-id="ecdf9-131">Überschreibt das übergeordnete Gerät des nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="ecdf9-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ecdf9-132">-InputObject</span></span>
<span data-ttu-id="ecdf9-133">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="ecdf9-133">IotHub object</span></span>

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

### <span data-ttu-id="ecdf9-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ecdf9-134">-IotHubName</span></span>
<span data-ttu-id="ecdf9-135">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="ecdf9-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ecdf9-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ecdf9-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="ecdf9-137">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für den Primärschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="ecdf9-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="ecdf9-138">-ParentDeviceId</span></span>
<span data-ttu-id="ecdf9-139">Die ID des Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-139">Id of edge device.</span></span>

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

### <span data-ttu-id="ecdf9-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdf9-140">-ResourceGroupName</span></span>
<span data-ttu-id="ecdf9-141">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ecdf9-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ecdf9-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ecdf9-142">-ResourceId</span></span>
<span data-ttu-id="ecdf9-143">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ecdf9-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ecdf9-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ecdf9-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="ecdf9-145">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für sekundären Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="ecdf9-146">-Status</span><span class="sxs-lookup"><span data-stu-id="ecdf9-146">-Status</span></span>
<span data-ttu-id="ecdf9-147">Einrichten des Gerätestatus bei der Erstellung</span><span class="sxs-lookup"><span data-stu-id="ecdf9-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="ecdf9-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="ecdf9-148">-StatusReason</span></span>
<span data-ttu-id="ecdf9-149">Beschreibung für den Gerätestatus</span><span class="sxs-lookup"><span data-stu-id="ecdf9-149">Description for device status.</span></span>

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

### <span data-ttu-id="ecdf9-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecdf9-150">-Confirm</span></span>
<span data-ttu-id="ecdf9-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecdf9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdf9-152">-WhatIf</span></span>
<span data-ttu-id="ecdf9-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdf9-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecdf9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdf9-155">CommonParameters</span></span>
<span data-ttu-id="ecdf9-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdf9-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdf9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdf9-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecdf9-158">INPUTS</span></span>

### <span data-ttu-id="ecdf9-159">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ecdf9-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ecdf9-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ecdf9-160">System.String</span></span>

## <span data-ttu-id="ecdf9-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecdf9-161">OUTPUTS</span></span>

### <span data-ttu-id="ecdf9-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ecdf9-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ecdf9-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecdf9-163">NOTES</span></span>

## <span data-ttu-id="ecdf9-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecdf9-164">RELATED LINKS</span></span>
