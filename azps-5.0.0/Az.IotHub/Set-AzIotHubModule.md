---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180447"
---
# <span data-ttu-id="3b407-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3b407-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="3b407-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b407-102">SYNOPSIS</span></span>
<span data-ttu-id="3b407-103">Aktualisieren Sie ein Modul auf einem Ziel-viel-Gerät in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="3b407-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="3b407-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b407-104">SYNTAX</span></span>

### <span data-ttu-id="3b407-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b407-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b407-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3b407-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b407-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3b407-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b407-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b407-108">DESCRIPTION</span></span>
<span data-ttu-id="3b407-109">Aktualisieren Sie ein Modul auf einem Ziel-viel-Gerät in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="3b407-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="3b407-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b407-110">EXAMPLES</span></span>

### <span data-ttu-id="3b407-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b407-111">Example 1</span></span>
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

<span data-ttu-id="3b407-112">Aktualisieren des Autorisierungs Typs eines viel Geräte Moduls.</span><span class="sxs-lookup"><span data-stu-id="3b407-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="3b407-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b407-113">PARAMETERS</span></span>

### <span data-ttu-id="3b407-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="3b407-114">-AuthMethod</span></span>
<span data-ttu-id="3b407-115">Der Autorisierungs, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b407-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="3b407-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b407-116">-DefaultProfile</span></span>
<span data-ttu-id="3b407-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b407-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b407-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="3b407-118">-DeviceId</span></span>
<span data-ttu-id="3b407-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="3b407-119">Target Device Id.</span></span>

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

### <span data-ttu-id="3b407-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b407-120">-InputObject</span></span>
<span data-ttu-id="3b407-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="3b407-121">IotHub object</span></span>

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

### <span data-ttu-id="3b407-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3b407-122">-IotHubName</span></span>
<span data-ttu-id="3b407-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="3b407-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3b407-124">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="3b407-124">-ModuleId</span></span>
<span data-ttu-id="3b407-125">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="3b407-125">Target Module Id.</span></span>

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

### <span data-ttu-id="3b407-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b407-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="3b407-127">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für den Primärschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b407-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="3b407-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b407-128">-ResourceGroupName</span></span>
<span data-ttu-id="3b407-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3b407-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3b407-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b407-130">-ResourceId</span></span>
<span data-ttu-id="3b407-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3b407-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3b407-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b407-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="3b407-133">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für sekundären Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b407-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="3b407-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b407-134">-Confirm</span></span>
<span data-ttu-id="3b407-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b407-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b407-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b407-136">-WhatIf</span></span>
<span data-ttu-id="3b407-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b407-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b407-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b407-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b407-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b407-139">CommonParameters</span></span>
<span data-ttu-id="3b407-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b407-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b407-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b407-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b407-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b407-142">INPUTS</span></span>

### <span data-ttu-id="3b407-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3b407-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3b407-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3b407-144">System.String</span></span>

## <span data-ttu-id="3b407-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b407-145">OUTPUTS</span></span>

### <span data-ttu-id="3b407-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="3b407-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="3b407-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b407-147">NOTES</span></span>

## <span data-ttu-id="3b407-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b407-148">RELATED LINKS</span></span>