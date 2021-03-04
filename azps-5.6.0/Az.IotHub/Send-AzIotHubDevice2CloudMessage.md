---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 41c4f5f4852f499f45b5c765263bdf356dbf90ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939547"
---
# <span data-ttu-id="efcab-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="efcab-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="efcab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcab-102">SYNOPSIS</span></span>
<span data-ttu-id="efcab-103">Senden einer Geräte-in-Cloud-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="efcab-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="efcab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efcab-104">SYNTAX</span></span>

### <span data-ttu-id="efcab-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="efcab-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efcab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="efcab-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efcab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="efcab-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efcab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efcab-108">DESCRIPTION</span></span>
<span data-ttu-id="efcab-109">Der Befehl unterstützt das Senden von Nachrichten mit Anwendungs- und Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="efcab-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="efcab-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efcab-110">EXAMPLES</span></span>

### <span data-ttu-id="efcab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efcab-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="efcab-112">Senden von Geräten in die Cloud mithilfe des Standardtransporttyps</span><span class="sxs-lookup"><span data-stu-id="efcab-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="efcab-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="efcab-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="efcab-114">Senden eines mqtt-Geräts an eine Cloudnachricht.</span><span class="sxs-lookup"><span data-stu-id="efcab-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="efcab-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efcab-115">PARAMETERS</span></span>

### <span data-ttu-id="efcab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcab-116">-DefaultProfile</span></span>
<span data-ttu-id="efcab-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efcab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efcab-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="efcab-118">-DeviceId</span></span>
<span data-ttu-id="efcab-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="efcab-119">Target Device Id.</span></span>

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

### <span data-ttu-id="efcab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efcab-120">-InputObject</span></span>
<span data-ttu-id="efcab-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="efcab-121">IotHub object</span></span>

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

### <span data-ttu-id="efcab-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="efcab-122">-IotHubName</span></span>
<span data-ttu-id="efcab-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="efcab-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="efcab-124">-Nachricht</span><span class="sxs-lookup"><span data-stu-id="efcab-124">-Message</span></span>
<span data-ttu-id="efcab-125">Nachrichtentext, der an IoT Hub gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efcab-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="efcab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efcab-126">-PassThru</span></span>
<span data-ttu-id="efcab-127">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="efcab-127">Allows to return the boolean object.</span></span> <span data-ttu-id="efcab-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="efcab-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efcab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcab-129">-ResourceGroupName</span></span>
<span data-ttu-id="efcab-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="efcab-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="efcab-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efcab-131">-ResourceId</span></span>
<span data-ttu-id="efcab-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="efcab-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="efcab-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="efcab-133">-TransportType</span></span>
<span data-ttu-id="efcab-134">Zu verwendende Transportart.</span><span class="sxs-lookup"><span data-stu-id="efcab-134">Transport type to use.</span></span>
<span data-ttu-id="efcab-135">Standard ist Amqp.</span><span class="sxs-lookup"><span data-stu-id="efcab-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="efcab-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efcab-136">-Confirm</span></span>
<span data-ttu-id="efcab-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efcab-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efcab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efcab-138">-WhatIf</span></span>
<span data-ttu-id="efcab-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efcab-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efcab-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efcab-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efcab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcab-141">CommonParameters</span></span>
<span data-ttu-id="efcab-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efcab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcab-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcab-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcab-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efcab-144">INPUTS</span></span>

### <span data-ttu-id="efcab-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="efcab-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="efcab-146">System.String</span><span class="sxs-lookup"><span data-stu-id="efcab-146">System.String</span></span>

## <span data-ttu-id="efcab-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efcab-147">OUTPUTS</span></span>

### <span data-ttu-id="efcab-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efcab-148">System.Boolean</span></span>

## <span data-ttu-id="efcab-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="efcab-149">NOTES</span></span>

## <span data-ttu-id="efcab-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="efcab-150">RELATED LINKS</span></span>
