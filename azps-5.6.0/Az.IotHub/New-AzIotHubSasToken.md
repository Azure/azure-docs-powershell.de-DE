---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931136"
---
# <span data-ttu-id="ca1ac-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="ca1ac-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="ca1ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1ac-103">Generieren Sie ein SAS-Token für einen IoT-Hub, ein Gerät oder modul.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="ca1ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca1ac-104">SYNTAX</span></span>

### <span data-ttu-id="ca1ac-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca1ac-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca1ac-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca1ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca1ac-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca1ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca1ac-108">DESCRIPTION</span></span>
<span data-ttu-id="ca1ac-109">Bei Geräte-SAS-Token wird der Richtlinienparameter nur für den Zugriff auf die Geräteregistrierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="ca1ac-110">Daher sollte die Richtlinie Lesezugriff auf die Registrierung haben.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="ca1ac-111">Für IoT Hub-Token ist die Richtlinie Teil der SAS.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="ca1ac-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca1ac-112">EXAMPLES</span></span>

### <span data-ttu-id="ca1ac-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca1ac-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ca1ac-114">Generieren Sie ein IoT Hub SAS-Token mit der iothubowner-Richtlinie und dem Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="ca1ac-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca1ac-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="ca1ac-116">Generieren Sie ein IoT Hub SAS-Token mit der registryRead-Richtlinie und dem sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="ca1ac-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ca1ac-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="ca1ac-118">Generieren Sie ein Geräte-SAS-Token mithilfe der iothubowner-Richtlinie für den Zugriff auf die {iothub_name}-Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="ca1ac-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ca1ac-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="ca1ac-120">Generieren Sie ein Modul-SAS-Token mithilfe der iothubowner-Richtlinie, um auf die {iothub_name}-Geräteregistrierung zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="ca1ac-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ca1ac-121">PARAMETERS</span></span>

### <span data-ttu-id="ca1ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1ac-122">-DefaultProfile</span></span>
<span data-ttu-id="ca1ac-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1ac-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ca1ac-124">-DeviceId</span></span>
<span data-ttu-id="ca1ac-125">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-125">Target Device Id.</span></span>

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

### <span data-ttu-id="ca1ac-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="ca1ac-126">-Duration</span></span>
<span data-ttu-id="ca1ac-127">Zukünftiger Ablauf (in Sekunden) des zu generierenden Tokens.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="ca1ac-128">Der Standardwert ist 3600.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-128">Default is 3600.</span></span>

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

### <span data-ttu-id="ca1ac-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1ac-129">-InputObject</span></span>
<span data-ttu-id="ca1ac-130">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="ca1ac-130">IotHub object</span></span>

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

### <span data-ttu-id="ca1ac-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-131">-IotHubName</span></span>
<span data-ttu-id="ca1ac-132">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="ca1ac-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ca1ac-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-133">-KeyName</span></span>
<span data-ttu-id="ca1ac-134">Name des Zugriffsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-134">Access key name.</span></span>

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

### <span data-ttu-id="ca1ac-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ca1ac-135">-KeyType</span></span>
<span data-ttu-id="ca1ac-136">Zugriffstastentyp.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="ca1ac-137">-ModuleId</span></span>
<span data-ttu-id="ca1ac-138">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-138">Target Module Id.</span></span>

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

### <span data-ttu-id="ca1ac-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-139">-ResourceGroupName</span></span>
<span data-ttu-id="ca1ac-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ca1ac-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca1ac-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca1ac-141">-ResourceId</span></span>
<span data-ttu-id="ca1ac-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ca1ac-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ca1ac-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca1ac-143">-Confirm</span></span>
<span data-ttu-id="ca1ac-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1ac-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1ac-145">-WhatIf</span></span>
<span data-ttu-id="ca1ac-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1ac-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1ac-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1ac-148">CommonParameters</span></span>
<span data-ttu-id="ca1ac-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1ac-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca1ac-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1ac-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca1ac-151">INPUTS</span></span>

### <span data-ttu-id="ca1ac-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ca1ac-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ca1ac-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ca1ac-153">System.String</span></span>

## <span data-ttu-id="ca1ac-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca1ac-154">OUTPUTS</span></span>

### <span data-ttu-id="ca1ac-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ca1ac-155">System.String</span></span>

## <span data-ttu-id="ca1ac-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ca1ac-156">NOTES</span></span>

## <span data-ttu-id="ca1ac-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ca1ac-157">RELATED LINKS</span></span>
