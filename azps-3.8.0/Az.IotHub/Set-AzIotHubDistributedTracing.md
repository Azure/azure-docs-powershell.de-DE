---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996114"
---
# <span data-ttu-id="2209a-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="2209a-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="2209a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2209a-102">SYNOPSIS</span></span>
<span data-ttu-id="2209a-103">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="2209a-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="2209a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2209a-104">SYNTAX</span></span>

### <span data-ttu-id="2209a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2209a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2209a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2209a-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2209a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2209a-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2209a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2209a-108">DESCRIPTION</span></span>
<span data-ttu-id="2209a-109">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="2209a-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="2209a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2209a-110">EXAMPLES</span></span>

### <span data-ttu-id="2209a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2209a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="2209a-112">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="2209a-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="2209a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2209a-113">PARAMETERS</span></span>

### <span data-ttu-id="2209a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2209a-114">-DefaultProfile</span></span>
<span data-ttu-id="2209a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2209a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2209a-116">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="2209a-116">-DeviceId</span></span>
<span data-ttu-id="2209a-117">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="2209a-117">Target Device Id.</span></span>

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

### <span data-ttu-id="2209a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2209a-118">-InputObject</span></span>
<span data-ttu-id="2209a-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2209a-119">IotHub object</span></span>

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

### <span data-ttu-id="2209a-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2209a-120">-IotHubName</span></span>
<span data-ttu-id="2209a-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="2209a-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2209a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2209a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2209a-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2209a-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2209a-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2209a-124">-ResourceId</span></span>
<span data-ttu-id="2209a-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2209a-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2209a-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="2209a-126">-SamplingMode</span></span>
<span data-ttu-id="2209a-127">Aktiviert und deaktiviert die Sampling-Funktion für die verteilte Ablaufverfolgung.</span><span class="sxs-lookup"><span data-stu-id="2209a-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="2209a-128">-SamplingRate</span></span>
<span data-ttu-id="2209a-129">Steuert die Anzahl der Nachrichten, die zum Hinzufügen des Ablauf Verfolgungs Kontexts abgetastet wurden.</span><span class="sxs-lookup"><span data-stu-id="2209a-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="2209a-130">Dieser Wert ist ein Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="2209a-130">This value is a percentage.</span></span>
<span data-ttu-id="2209a-131">Nur Werte von 0 bis 100 (einschließlich) sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="2209a-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2209a-132">-Confirm</span></span>
<span data-ttu-id="2209a-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2209a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2209a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2209a-134">-WhatIf</span></span>
<span data-ttu-id="2209a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2209a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2209a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2209a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2209a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2209a-137">CommonParameters</span></span>
<span data-ttu-id="2209a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2209a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2209a-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2209a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2209a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2209a-140">INPUTS</span></span>

### <span data-ttu-id="2209a-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2209a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2209a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2209a-142">System.String</span></span>

## <span data-ttu-id="2209a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2209a-143">OUTPUTS</span></span>

### <span data-ttu-id="2209a-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="2209a-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="2209a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2209a-145">NOTES</span></span>

## <span data-ttu-id="2209a-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2209a-146">RELATED LINKS</span></span>
