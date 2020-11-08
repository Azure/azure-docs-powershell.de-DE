---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165596"
---
# <span data-ttu-id="d23e5-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d23e5-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="d23e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d23e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d23e5-103">Erstellen oder Aktualisieren der Geräte Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="d23e5-103">Create or update device security group</span></span>

## <span data-ttu-id="d23e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d23e5-104">SYNTAX</span></span>

### <span data-ttu-id="d23e5-105">ResourceIdLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d23e5-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23e5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d23e5-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23e5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d23e5-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d23e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d23e5-108">DESCRIPTION</span></span>
<span data-ttu-id="d23e5-109">Das Set-AzDeviceSecurityGroup-Cmdlet erstellt oder aktualisiert eine Geräte Sicherheitsgruppe, die in der viel Sicherheitslösung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d23e5-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="d23e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d23e5-110">EXAMPLES</span></span>

### <span data-ttu-id="d23e5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d23e5-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
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

<span data-ttu-id="d23e5-112">Aktualisieren der vorhandenen Geräte Sicherheitsgruppe aus "/Subscriptions/xxxxxxxx-xxxx-xxxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/Providers/Microsoft.Devices/IotHubs/MyHub" mit dem Regeltyp "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="d23e5-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="d23e5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d23e5-113">PARAMETERS</span></span>

### <span data-ttu-id="d23e5-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="d23e5-114">-AllowlistRule</span></span>
<span data-ttu-id="d23e5-115">Listenregeln zulassen.</span><span class="sxs-lookup"><span data-stu-id="d23e5-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23e5-116">-DefaultProfile</span></span>
<span data-ttu-id="d23e5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d23e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d23e5-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="d23e5-118">-DenylistRule</span></span>
<span data-ttu-id="d23e5-119">Regeln zum Verweigern von Listen.</span><span class="sxs-lookup"><span data-stu-id="d23e5-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="d23e5-120">-HubResourceId</span></span>
<span data-ttu-id="d23e5-121">Viel Hub-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d23e5-121">IoT Hub resource Id.</span></span>

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

### <span data-ttu-id="d23e5-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d23e5-122">-InputObject</span></span>
<span data-ttu-id="d23e5-123">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="d23e5-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d23e5-124">-Name</span></span>
<span data-ttu-id="d23e5-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="d23e5-125">Resource name.</span></span>

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

### <span data-ttu-id="d23e5-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d23e5-126">-ResourceId</span></span>
<span data-ttu-id="d23e5-127">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d23e5-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="d23e5-128">-ThresholdRule</span></span>
<span data-ttu-id="d23e5-129">Schwellenwertregeln.</span><span class="sxs-lookup"><span data-stu-id="d23e5-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="d23e5-130">-TimeWindowRule</span></span>
<span data-ttu-id="d23e5-131">Regeln für das Zeitfenster.</span><span class="sxs-lookup"><span data-stu-id="d23e5-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23e5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d23e5-132">-Confirm</span></span>
<span data-ttu-id="d23e5-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d23e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23e5-134">-WhatIf</span></span>
<span data-ttu-id="d23e5-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d23e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23e5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d23e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23e5-137">CommonParameters</span></span>
<span data-ttu-id="d23e5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23e5-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d23e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23e5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d23e5-140">INPUTS</span></span>

### <span data-ttu-id="d23e5-141">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="d23e5-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="d23e5-142">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="d23e5-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="d23e5-143">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="d23e5-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="d23e5-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="d23e5-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="d23e5-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d23e5-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="d23e5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d23e5-146">System.String</span></span>

## <span data-ttu-id="d23e5-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d23e5-147">OUTPUTS</span></span>

### <span data-ttu-id="d23e5-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d23e5-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="d23e5-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="d23e5-149">NOTES</span></span>

## <span data-ttu-id="d23e5-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d23e5-150">RELATED LINKS</span></span>
