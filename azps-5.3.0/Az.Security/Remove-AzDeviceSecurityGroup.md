---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472013"
---
# <span data-ttu-id="0776f-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0776f-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="0776f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0776f-102">SYNOPSIS</span></span>
<span data-ttu-id="0776f-103">Sicherheitsgruppe "Gerät löschen"</span><span class="sxs-lookup"><span data-stu-id="0776f-103">Delete device security group</span></span>

## <span data-ttu-id="0776f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0776f-104">SYNTAX</span></span>

### <span data-ttu-id="0776f-105">ResourceIdLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0776f-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0776f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0776f-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0776f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0776f-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0776f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0776f-108">DESCRIPTION</span></span>
<span data-ttu-id="0776f-109">Mit Remove-AzDeviceSecurityGroup A0 wird eine gerätesicherheitsgruppe gelöscht, die in der Sicherheitslösung "iot" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0776f-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="0776f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0776f-110">EXAMPLES</span></span>

### <span data-ttu-id="0776f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0776f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="0776f-112">Löschen Sie die Gerätesicherheitsgruppe "MySecurityGroup" des iot-Hubs mit der Ressourcen-ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub".</span><span class="sxs-lookup"><span data-stu-id="0776f-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="0776f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0776f-113">PARAMETERS</span></span>

### <span data-ttu-id="0776f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0776f-114">-DefaultProfile</span></span>
<span data-ttu-id="0776f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0776f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0776f-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="0776f-116">-HubResourceId</span></span>
<span data-ttu-id="0776f-117">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="0776f-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0776f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0776f-118">-InputObject</span></span>
<span data-ttu-id="0776f-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="0776f-119">Input Object.</span></span>

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

### <span data-ttu-id="0776f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0776f-120">-Name</span></span>
<span data-ttu-id="0776f-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0776f-121">Resource name.</span></span>

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

### <span data-ttu-id="0776f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0776f-122">-PassThru</span></span>
<span data-ttu-id="0776f-123">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0776f-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0776f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0776f-124">-ResourceId</span></span>
<span data-ttu-id="0776f-125">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="0776f-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0776f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0776f-126">-Confirm</span></span>
<span data-ttu-id="0776f-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0776f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0776f-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0776f-128">-WhatIf</span></span>
<span data-ttu-id="0776f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0776f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0776f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0776f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0776f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0776f-131">CommonParameters</span></span>
<span data-ttu-id="0776f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0776f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0776f-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0776f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0776f-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0776f-134">INPUTS</span></span>

### <span data-ttu-id="0776f-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0776f-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="0776f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0776f-136">System.String</span></span>

## <span data-ttu-id="0776f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0776f-137">OUTPUTS</span></span>

### <span data-ttu-id="0776f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0776f-138">System.Boolean</span></span>

## <span data-ttu-id="0776f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0776f-139">NOTES</span></span>

## <span data-ttu-id="0776f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0776f-140">RELATED LINKS</span></span>
