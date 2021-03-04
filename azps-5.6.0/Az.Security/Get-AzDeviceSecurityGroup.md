---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 52fae225184b83675f21af941fa125576252ffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950059"
---
# <span data-ttu-id="37c5d-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="37c5d-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="37c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="37c5d-103">Gerätesicherheitsgruppe erhalten (IoT Hub-Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="37c5d-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="37c5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37c5d-104">SYNTAX</span></span>

### <span data-ttu-id="37c5d-105">ResourceIdScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="37c5d-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37c5d-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="37c5d-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37c5d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37c5d-107">DESCRIPTION</span></span>
<span data-ttu-id="37c5d-108">Das Get-AzDeviceSecurityGroup-Cmdlet gibt eine in der iot-Sicherheitslösung definierte Gerätesicherheitsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="37c5d-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="37c5d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37c5d-109">EXAMPLES</span></span>

### <span data-ttu-id="37c5d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37c5d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="37c5d-111">Abrufen der Gerätesicherheitsgruppe "MySecurityGroup" in IoT Hub mit reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="37c5d-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="37c5d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37c5d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="37c5d-113">Abrufen einer Liste der Gerätesicherheitsgruppe in IoT Hub mit der Neuressourcen-ID "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="37c5d-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="37c5d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37c5d-114">PARAMETERS</span></span>

### <span data-ttu-id="37c5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c5d-115">-DefaultProfile</span></span>
<span data-ttu-id="37c5d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37c5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c5d-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="37c5d-117">-HubResourceId</span></span>
<span data-ttu-id="37c5d-118">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="37c5d-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="37c5d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="37c5d-119">-Name</span></span>
<span data-ttu-id="37c5d-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="37c5d-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c5d-121">CommonParameters</span></span>
<span data-ttu-id="37c5d-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c5d-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37c5d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c5d-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37c5d-124">INPUTS</span></span>

### <span data-ttu-id="37c5d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="37c5d-125">None</span></span>

## <span data-ttu-id="37c5d-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37c5d-126">OUTPUTS</span></span>

### <span data-ttu-id="37c5d-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="37c5d-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="37c5d-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37c5d-128">NOTES</span></span>

## <span data-ttu-id="37c5d-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37c5d-129">RELATED LINKS</span></span>
