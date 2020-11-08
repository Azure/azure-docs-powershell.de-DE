---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003603"
---
# <span data-ttu-id="9358c-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9358c-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="9358c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9358c-102">SYNOPSIS</span></span>
<span data-ttu-id="9358c-103">Erstellt eine neue Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="9358c-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="9358c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9358c-104">SYNTAX</span></span>

### <span data-ttu-id="9358c-105">ConnectionStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9358c-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9358c-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="9358c-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9358c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9358c-107">DESCRIPTION</span></span>
<span data-ttu-id="9358c-108">Das Cmdlet **New-AzDataBoxEdgeRole** erstellt eine neue Rolle für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="9358c-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="9358c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9358c-109">EXAMPLES</span></span>

### <span data-ttu-id="9358c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9358c-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="9358c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9358c-111">PARAMETERS</span></span>

### <span data-ttu-id="9358c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9358c-112">-AsJob</span></span>
<span data-ttu-id="9358c-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9358c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9358c-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9358c-114">-ConnectionString</span></span>
<span data-ttu-id="9358c-115">So stellen Sie Verbindungszeichenfolgen bereit</span><span class="sxs-lookup"><span data-stu-id="9358c-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="9358c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9358c-116">-DefaultProfile</span></span>
<span data-ttu-id="9358c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9358c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9358c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9358c-118">-DeviceName</span></span>
<span data-ttu-id="9358c-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="9358c-119">Device Name</span></span>

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

### <span data-ttu-id="9358c-120">-Deviceproperty</span><span class="sxs-lookup"><span data-stu-id="9358c-120">-DeviceProperty</span></span>
<span data-ttu-id="9358c-121">So stellen Sie Geräteeigenschaften bereit</span><span class="sxs-lookup"><span data-stu-id="9358c-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="9358c-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9358c-122">-EncryptionKey</span></span>
<span data-ttu-id="9358c-123">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="9358c-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9358c-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="9358c-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="9358c-125">Gerätezugriffs Taste "viel"</span><span class="sxs-lookup"><span data-stu-id="9358c-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="9358c-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="9358c-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="9358c-127">Bitte geben Sie die Verbindungszeichenfolge des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="9358c-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="9358c-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="9358c-128">-IotDeviceId</span></span>
<span data-ttu-id="9358c-129">Geräte-ID des viel-Geräts</span><span class="sxs-lookup"><span data-stu-id="9358c-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="9358c-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="9358c-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="9358c-131">Zugriffstaste des viel Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="9358c-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="9358c-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="9358c-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="9358c-133">Bitte geben Sie die Verbindungszeichenfolge des Edge-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="9358c-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="9358c-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="9358c-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="9358c-135">ID des viel Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="9358c-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="9358c-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="9358c-136">-IotHostHub</span></span>
<span data-ttu-id="9358c-137">Hosthub-Adresse</span><span class="sxs-lookup"><span data-stu-id="9358c-137">Hosthub address</span></span>

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

### <span data-ttu-id="9358c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9358c-138">-Name</span></span>
<span data-ttu-id="9358c-139">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="9358c-139">Resource Name</span></span>

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

### <span data-ttu-id="9358c-140">-Plattform</span><span class="sxs-lookup"><span data-stu-id="9358c-140">-Platform</span></span>
<span data-ttu-id="9358c-141">Bereitstellen der Plattform für Ex: Linux</span><span class="sxs-lookup"><span data-stu-id="9358c-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="9358c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9358c-142">-ResourceGroupName</span></span>
<span data-ttu-id="9358c-143">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9358c-143">Resource Group Name</span></span>

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

### <span data-ttu-id="9358c-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="9358c-144">-RoleStatus</span></span>
<span data-ttu-id="9358c-145">Bereitstellen des Status aktivieren/deaktivieren</span><span class="sxs-lookup"><span data-stu-id="9358c-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="9358c-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9358c-146">-Confirm</span></span>
<span data-ttu-id="9358c-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9358c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9358c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9358c-148">-WhatIf</span></span>
<span data-ttu-id="9358c-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9358c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9358c-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9358c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9358c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9358c-151">CommonParameters</span></span>
<span data-ttu-id="9358c-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9358c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9358c-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9358c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9358c-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9358c-154">INPUTS</span></span>

### <span data-ttu-id="9358c-155">Keine</span><span class="sxs-lookup"><span data-stu-id="9358c-155">None</span></span>

## <span data-ttu-id="9358c-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9358c-156">OUTPUTS</span></span>

### <span data-ttu-id="9358c-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9358c-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="9358c-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="9358c-158">NOTES</span></span>

## <span data-ttu-id="9358c-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9358c-159">RELATED LINKS</span></span>
