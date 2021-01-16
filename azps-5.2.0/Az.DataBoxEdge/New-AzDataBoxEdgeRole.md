---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293692"
---
# <span data-ttu-id="5d5b7-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5d5b7-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="5d5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5b7-103">Erstellt eine neue Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="5d5b7-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="5d5b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d5b7-104">SYNTAX</span></span>

### <span data-ttu-id="5d5b7-105">ConnectionStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d5b7-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5b7-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d5b7-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d5b7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d5b7-107">DESCRIPTION</span></span>
<span data-ttu-id="5d5b7-108">Das **Cmdlet "New-AzDataBoxEdgeRole"** erstellt eine neue Rolle für ein Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="5d5b7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d5b7-109">EXAMPLES</span></span>

### <span data-ttu-id="5d5b7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d5b7-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="5d5b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d5b7-111">PARAMETERS</span></span>

### <span data-ttu-id="5d5b7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d5b7-112">-AsJob</span></span>
<span data-ttu-id="5d5b7-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5d5b7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d5b7-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5d5b7-114">-ConnectionString</span></span>
<span data-ttu-id="5d5b7-115">So stellen Sie Verbindungszeichenfolgen zur Verfügung</span><span class="sxs-lookup"><span data-stu-id="5d5b7-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5b7-116">-DefaultProfile</span></span>
<span data-ttu-id="5d5b7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5b7-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5d5b7-118">-DeviceName</span></span>
<span data-ttu-id="5d5b7-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="5d5b7-119">Device Name</span></span>

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

### <span data-ttu-id="5d5b7-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="5d5b7-120">-DeviceProperty</span></span>
<span data-ttu-id="5d5b7-121">So stellen Sie Geräteeigenschaften zur Verfügung</span><span class="sxs-lookup"><span data-stu-id="5d5b7-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5d5b7-122">-EncryptionKey</span></span>
<span data-ttu-id="5d5b7-123">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="5d5b7-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="5d5b7-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="5d5b7-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="5d5b7-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5d5b7-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="5d5b7-127">Geben Sie die Verbindungszeichenfolge des IOT-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="5d5b7-128">-IotDeviceId</span></span>
<span data-ttu-id="5d5b7-129">Geräte-ID des Iot-Geräts</span><span class="sxs-lookup"><span data-stu-id="5d5b7-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="5d5b7-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="5d5b7-131">Zugriffstaste des Iot -Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="5d5b7-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5d5b7-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="5d5b7-133">Geben Sie die Verbindungszeichenfolge des Edgegeräts an.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="5d5b7-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="5d5b7-135">ID des Iot Edge Device</span><span class="sxs-lookup"><span data-stu-id="5d5b7-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="5d5b7-136">-IotHostHub</span></span>
<span data-ttu-id="5d5b7-137">Adresse von Hosthub</span><span class="sxs-lookup"><span data-stu-id="5d5b7-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5d5b7-138">-Name</span></span>
<span data-ttu-id="5d5b7-139">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="5d5b7-139">Resource Name</span></span>

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

### <span data-ttu-id="5d5b7-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="5d5b7-140">-Platform</span></span>
<span data-ttu-id="5d5b7-141">Stellen Sie die Plattform für Linux zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="5d5b7-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5b7-142">-ResourceGroupName</span></span>
<span data-ttu-id="5d5b7-143">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5d5b7-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b7-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="5d5b7-144">-RoleStatus</span></span>
<span data-ttu-id="5d5b7-145">Bereitstellen des Status "Aktivieren/Deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="5d5b7-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="5d5b7-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d5b7-146">-Confirm</span></span>
<span data-ttu-id="5d5b7-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5b7-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d5b7-148">-WhatIf</span></span>
<span data-ttu-id="5d5b7-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d5b7-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5b7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5b7-151">CommonParameters</span></span>
<span data-ttu-id="5d5b7-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5b7-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d5b7-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5b7-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d5b7-154">INPUTS</span></span>

### <span data-ttu-id="5d5b7-155">Keine</span><span class="sxs-lookup"><span data-stu-id="5d5b7-155">None</span></span>

## <span data-ttu-id="5d5b7-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d5b7-156">OUTPUTS</span></span>

### <span data-ttu-id="5d5b7-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5d5b7-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5d5b7-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d5b7-158">NOTES</span></span>

## <span data-ttu-id="5d5b7-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d5b7-159">RELATED LINKS</span></span>
