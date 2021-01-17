---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361765"
---
# <span data-ttu-id="ed9ea-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="ed9ea-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="ed9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9ea-103">Aktualisieren Sie ein Modul auf einem Ziel-IoT-Gerät in einem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="ed9ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed9ea-104">SYNTAX</span></span>

### <span data-ttu-id="ed9ea-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed9ea-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed9ea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed9ea-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed9ea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed9ea-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed9ea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed9ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ed9ea-109">Aktualisieren Sie ein Modul auf einem Ziel-IoT-Gerät in einem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="ed9ea-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed9ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ed9ea-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed9ea-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="ed9ea-112">Aktualisieren sie den Autorisierungstyp eines Iot-Gerätemoduls.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="ed9ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed9ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ed9ea-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="ed9ea-114">-AuthMethod</span></span>
<span data-ttu-id="ed9ea-115">Der Autorisierungstyp, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="ed9ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9ea-116">-DefaultProfile</span></span>
<span data-ttu-id="ed9ea-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9ea-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ed9ea-118">-DeviceId</span></span>
<span data-ttu-id="ed9ea-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-119">Target Device Id.</span></span>

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

### <span data-ttu-id="ed9ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed9ea-120">-InputObject</span></span>
<span data-ttu-id="ed9ea-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="ed9ea-121">IotHub object</span></span>

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

### <span data-ttu-id="ed9ea-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ed9ea-122">-IotHubName</span></span>
<span data-ttu-id="ed9ea-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="ed9ea-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed9ea-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="ed9ea-124">-ModuleId</span></span>
<span data-ttu-id="ed9ea-125">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-125">Target Module Id.</span></span>

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

### <span data-ttu-id="ed9ea-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ed9ea-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="ed9ea-127">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="ed9ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed9ea-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ed9ea-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed9ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed9ea-130">-ResourceId</span></span>
<span data-ttu-id="ed9ea-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ed9ea-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ed9ea-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ed9ea-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="ed9ea-133">Expliziter selbst signierter Fingerabdruck des Zertifikats zur Verwendung für den sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9ea-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed9ea-134">-Confirm</span></span>
<span data-ttu-id="ed9ea-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9ea-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed9ea-136">-WhatIf</span></span>
<span data-ttu-id="ed9ea-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9ea-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9ea-139">CommonParameters</span></span>
<span data-ttu-id="ed9ea-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9ea-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9ea-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9ea-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed9ea-142">INPUTS</span></span>

### <span data-ttu-id="ed9ea-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed9ea-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed9ea-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ed9ea-144">System.String</span></span>

## <span data-ttu-id="ed9ea-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed9ea-145">OUTPUTS</span></span>

### <span data-ttu-id="ed9ea-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="ed9ea-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="ed9ea-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed9ea-147">NOTES</span></span>

## <span data-ttu-id="ed9ea-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed9ea-148">RELATED LINKS</span></span>