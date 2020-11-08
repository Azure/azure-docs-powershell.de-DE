---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166605"
---
# <span data-ttu-id="354aa-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="354aa-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="354aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="354aa-102">SYNOPSIS</span></span>
<span data-ttu-id="354aa-103">Erstellen Sie ein Modul auf einem Ziel-viel-Gerät in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="354aa-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="354aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="354aa-104">SYNTAX</span></span>

### <span data-ttu-id="354aa-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="354aa-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="354aa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="354aa-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="354aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="354aa-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="354aa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="354aa-108">DESCRIPTION</span></span>
<span data-ttu-id="354aa-109">Erstellen Sie ein Modul auf einem Ziel-viel-Gerät mit einem anderen Autorisierungs in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="354aa-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="354aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="354aa-110">EXAMPLES</span></span>

### <span data-ttu-id="354aa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="354aa-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

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

<span data-ttu-id="354aa-112">Erstellen Sie ein Modul auf einem Ziel-viel-Gerät mit Standard Autorisierung (freigegebener privater Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="354aa-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="354aa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="354aa-113">PARAMETERS</span></span>

### <span data-ttu-id="354aa-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="354aa-114">-AuthMethod</span></span>
<span data-ttu-id="354aa-115">Der Autorisierungs, mit dem eine Entität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="354aa-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="354aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354aa-116">-DefaultProfile</span></span>
<span data-ttu-id="354aa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="354aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354aa-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="354aa-118">-DeviceId</span></span>
<span data-ttu-id="354aa-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="354aa-119">Target Device Id.</span></span>

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

### <span data-ttu-id="354aa-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="354aa-120">-InputObject</span></span>
<span data-ttu-id="354aa-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="354aa-121">IotHub object</span></span>

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

### <span data-ttu-id="354aa-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="354aa-122">-IotHubName</span></span>
<span data-ttu-id="354aa-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="354aa-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="354aa-124">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="354aa-124">-ModuleId</span></span>
<span data-ttu-id="354aa-125">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="354aa-125">Target Module Id.</span></span>

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

### <span data-ttu-id="354aa-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="354aa-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="354aa-127">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für den Primärschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="354aa-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="354aa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354aa-128">-ResourceGroupName</span></span>
<span data-ttu-id="354aa-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="354aa-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="354aa-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="354aa-130">-ResourceId</span></span>
<span data-ttu-id="354aa-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="354aa-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="354aa-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="354aa-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="354aa-133">Eindeutiger selbstsignierter Zertifikat-Fingerabdruck, der für sekundären Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="354aa-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="354aa-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="354aa-134">-Confirm</span></span>
<span data-ttu-id="354aa-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="354aa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="354aa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354aa-136">-WhatIf</span></span>
<span data-ttu-id="354aa-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="354aa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354aa-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="354aa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="354aa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354aa-139">CommonParameters</span></span>
<span data-ttu-id="354aa-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354aa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354aa-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354aa-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354aa-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="354aa-142">INPUTS</span></span>

### <span data-ttu-id="354aa-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="354aa-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="354aa-144">System. String</span><span class="sxs-lookup"><span data-stu-id="354aa-144">System.String</span></span>

## <span data-ttu-id="354aa-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="354aa-145">OUTPUTS</span></span>

### <span data-ttu-id="354aa-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="354aa-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="354aa-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="354aa-147">NOTES</span></span>

## <span data-ttu-id="354aa-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="354aa-148">RELATED LINKS</span></span>