---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177941"
---
# <span data-ttu-id="e629e-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="e629e-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="e629e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e629e-102">SYNOPSIS</span></span>
<span data-ttu-id="e629e-103">Generieren eines SAS-Tokens für einen Ziel-viel-Hub,-Gerät oder-Modul</span><span class="sxs-lookup"><span data-stu-id="e629e-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="e629e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e629e-104">SYNTAX</span></span>

### <span data-ttu-id="e629e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e629e-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e629e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e629e-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e629e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e629e-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e629e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e629e-108">DESCRIPTION</span></span>
<span data-ttu-id="e629e-109">Für Geräte-SAS-Token wird der Richtlinienparameter nur für den Zugriff auf die Geräteregistrierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e629e-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="e629e-110">Daher sollte die Richtlinie Lesezugriff auf die Registrierung haben.</span><span class="sxs-lookup"><span data-stu-id="e629e-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="e629e-111">Für viele Hub-Token ist die Richtlinie Teil der SAS.</span><span class="sxs-lookup"><span data-stu-id="e629e-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="e629e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e629e-112">EXAMPLES</span></span>

### <span data-ttu-id="e629e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e629e-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="e629e-114">Generieren Sie ein viel Hub-SAS-Token mithilfe der iothubowner-Richtlinie und des Primärschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e629e-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="e629e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e629e-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="e629e-116">Generieren Sie mithilfe der registryRead-Richtlinie und des sekundären Schlüssels ein viel-Hub-SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="e629e-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="e629e-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e629e-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="e629e-118">Generieren Sie ein Device SAS-Token mithilfe der iothubowner-Richtlinie für den Zugriff auf die {iothub_name}-Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="e629e-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="e629e-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e629e-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="e629e-120">Generieren Sie ein Modul-SAS-Token mithilfe der iothubowner-Richtlinie für den Zugriff auf die {iothub_name}-Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="e629e-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="e629e-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e629e-121">PARAMETERS</span></span>

### <span data-ttu-id="e629e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e629e-122">-DefaultProfile</span></span>
<span data-ttu-id="e629e-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e629e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e629e-124">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="e629e-124">-DeviceId</span></span>
<span data-ttu-id="e629e-125">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="e629e-125">Target Device Id.</span></span>

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

### <span data-ttu-id="e629e-126">-Dauer</span><span class="sxs-lookup"><span data-stu-id="e629e-126">-Duration</span></span>
<span data-ttu-id="e629e-127">Zukünftiges Ablaufdatum (in Sekunden) des zu generierenden Tokens.</span><span class="sxs-lookup"><span data-stu-id="e629e-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="e629e-128">Standard ist 3600.</span><span class="sxs-lookup"><span data-stu-id="e629e-128">Default is 3600.</span></span>

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

### <span data-ttu-id="e629e-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e629e-129">-InputObject</span></span>
<span data-ttu-id="e629e-130">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e629e-130">IotHub object</span></span>

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

### <span data-ttu-id="e629e-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e629e-131">-IotHubName</span></span>
<span data-ttu-id="e629e-132">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="e629e-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e629e-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e629e-133">-KeyName</span></span>
<span data-ttu-id="e629e-134">Zugriffstasten Name</span><span class="sxs-lookup"><span data-stu-id="e629e-134">Access key name.</span></span>

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

### <span data-ttu-id="e629e-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e629e-135">-KeyType</span></span>
<span data-ttu-id="e629e-136">Zugriffs Tastentyp.</span><span class="sxs-lookup"><span data-stu-id="e629e-136">Access key type.</span></span>

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

### <span data-ttu-id="e629e-137">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="e629e-137">-ModuleId</span></span>
<span data-ttu-id="e629e-138">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="e629e-138">Target Module Id.</span></span>

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

### <span data-ttu-id="e629e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e629e-139">-ResourceGroupName</span></span>
<span data-ttu-id="e629e-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e629e-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e629e-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e629e-141">-ResourceId</span></span>
<span data-ttu-id="e629e-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e629e-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e629e-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e629e-143">-Confirm</span></span>
<span data-ttu-id="e629e-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e629e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e629e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e629e-145">-WhatIf</span></span>
<span data-ttu-id="e629e-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e629e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e629e-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e629e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e629e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e629e-148">CommonParameters</span></span>
<span data-ttu-id="e629e-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e629e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e629e-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e629e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e629e-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e629e-151">INPUTS</span></span>

### <span data-ttu-id="e629e-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e629e-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e629e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e629e-153">System.String</span></span>

## <span data-ttu-id="e629e-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e629e-154">OUTPUTS</span></span>

### <span data-ttu-id="e629e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e629e-155">System.String</span></span>

## <span data-ttu-id="e629e-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e629e-156">NOTES</span></span>

## <span data-ttu-id="e629e-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e629e-157">RELATED LINKS</span></span>
