---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296944"
---
# <span data-ttu-id="dd319-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="dd319-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="dd319-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd319-102">SYNOPSIS</span></span>
<span data-ttu-id="dd319-103">Nachricht "Gerät zu Wolke senden".</span><span class="sxs-lookup"><span data-stu-id="dd319-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="dd319-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd319-104">SYNTAX</span></span>

### <span data-ttu-id="dd319-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd319-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd319-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd319-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd319-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dd319-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd319-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd319-108">DESCRIPTION</span></span>
<span data-ttu-id="dd319-109">Der Befehl unterstützt das Senden von Nachrichten mit Anwendungs-und Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd319-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="dd319-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd319-110">EXAMPLES</span></span>

### <span data-ttu-id="dd319-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd319-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="dd319-112">Senden eines Geräts an eine Cloud-Nachricht mithilfe des Standard Transporttyps</span><span class="sxs-lookup"><span data-stu-id="dd319-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="dd319-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd319-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="dd319-114">Senden eines mqtt-Geräts an eine Cloud-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dd319-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="dd319-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd319-115">PARAMETERS</span></span>

### <span data-ttu-id="dd319-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd319-116">-DefaultProfile</span></span>
<span data-ttu-id="dd319-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd319-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd319-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="dd319-118">-DeviceId</span></span>
<span data-ttu-id="dd319-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="dd319-119">Target Device Id.</span></span>

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

### <span data-ttu-id="dd319-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd319-120">-InputObject</span></span>
<span data-ttu-id="dd319-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="dd319-121">IotHub object</span></span>

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

### <span data-ttu-id="dd319-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dd319-122">-IotHubName</span></span>
<span data-ttu-id="dd319-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="dd319-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dd319-124">-Nachricht</span><span class="sxs-lookup"><span data-stu-id="dd319-124">-Message</span></span>
<span data-ttu-id="dd319-125">Nachrichtentext, der an viel Hub gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd319-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="dd319-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd319-126">-PassThru</span></span>
<span data-ttu-id="dd319-127">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd319-127">Allows to return the boolean object.</span></span> <span data-ttu-id="dd319-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="dd319-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd319-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd319-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd319-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dd319-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dd319-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd319-131">-ResourceId</span></span>
<span data-ttu-id="dd319-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd319-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dd319-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="dd319-133">-TransportType</span></span>
<span data-ttu-id="dd319-134">Zu verwendender Transporttyp.</span><span class="sxs-lookup"><span data-stu-id="dd319-134">Transport type to use.</span></span>
<span data-ttu-id="dd319-135">Der Standardwert ist AMQP.</span><span class="sxs-lookup"><span data-stu-id="dd319-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd319-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd319-136">-Confirm</span></span>
<span data-ttu-id="dd319-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd319-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd319-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd319-138">-WhatIf</span></span>
<span data-ttu-id="dd319-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd319-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd319-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd319-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd319-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd319-141">CommonParameters</span></span>
<span data-ttu-id="dd319-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd319-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd319-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd319-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd319-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd319-144">INPUTS</span></span>

### <span data-ttu-id="dd319-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd319-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dd319-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd319-146">System.String</span></span>

## <span data-ttu-id="dd319-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd319-147">OUTPUTS</span></span>

### <span data-ttu-id="dd319-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd319-148">System.Boolean</span></span>

## <span data-ttu-id="dd319-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd319-149">NOTES</span></span>

## <span data-ttu-id="dd319-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd319-150">RELATED LINKS</span></span>
