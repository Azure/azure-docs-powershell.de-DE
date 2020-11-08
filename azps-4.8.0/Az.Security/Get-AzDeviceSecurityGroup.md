---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173534"
---
# <span data-ttu-id="1b660-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b660-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="1b660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b660-102">SYNOPSIS</span></span>
<span data-ttu-id="1b660-103">Get Device Security Group (viel Hub-Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="1b660-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="1b660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b660-104">SYNTAX</span></span>

### <span data-ttu-id="1b660-105">ResourceIdScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b660-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b660-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="1b660-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b660-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b660-107">DESCRIPTION</span></span>
<span data-ttu-id="1b660-108">Das Get-AzDeviceSecurityGroup-Cmdlet gibt eine in der viel Sicherheitslösung definierte Geräte Sicherheitsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="1b660-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="1b660-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b660-109">EXAMPLES</span></span>

### <span data-ttu-id="1b660-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b660-110">Example 1</span></span>
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

<span data-ttu-id="1b660-111">Abrufen der Geräte Sicherheitsgruppe "mysecuritygroup" im viel Hub mit dasselbe Benuteroberflächenmodell-ID "/Subscriptions/xxxxxxxx-xxxx-xxxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/Providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="1b660-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="1b660-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1b660-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="1b660-113">Holen Sie sich die Liste der Device Security-Gruppe in viel Hub mit dasselbe Benuteroberflächenmodell-ID "/Subscriptions/xxxxxxxx-xxxx-xxxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/Providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="1b660-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="1b660-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b660-114">PARAMETERS</span></span>

### <span data-ttu-id="1b660-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b660-115">-DefaultProfile</span></span>
<span data-ttu-id="1b660-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b660-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b660-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="1b660-117">-HubResourceId</span></span>
<span data-ttu-id="1b660-118">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="1b660-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1b660-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b660-119">-Name</span></span>
<span data-ttu-id="1b660-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="1b660-120">Resource name.</span></span>

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

### <span data-ttu-id="1b660-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b660-121">CommonParameters</span></span>
<span data-ttu-id="1b660-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b660-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b660-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b660-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b660-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b660-124">INPUTS</span></span>

### <span data-ttu-id="1b660-125">Keine</span><span class="sxs-lookup"><span data-stu-id="1b660-125">None</span></span>

## <span data-ttu-id="1b660-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b660-126">OUTPUTS</span></span>

### <span data-ttu-id="1b660-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1b660-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="1b660-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b660-128">NOTES</span></span>

## <span data-ttu-id="1b660-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b660-129">RELATED LINKS</span></span>
