---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174185"
---
# <span data-ttu-id="c90ee-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c90ee-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="c90ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c90ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c90ee-103">Gruppe "Gerätesicherheit löschen"</span><span class="sxs-lookup"><span data-stu-id="c90ee-103">Delete device security group</span></span>

## <span data-ttu-id="c90ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c90ee-104">SYNTAX</span></span>

### <span data-ttu-id="c90ee-105">ResourceIdLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c90ee-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c90ee-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c90ee-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c90ee-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c90ee-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c90ee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c90ee-108">DESCRIPTION</span></span>
<span data-ttu-id="c90ee-109">Das Remove-AzDeviceSecurityGroup-Cmdlet löscht eine in der viel Sicherheitslösung definierte Geräte Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c90ee-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="c90ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c90ee-110">EXAMPLES</span></span>

### <span data-ttu-id="c90ee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c90ee-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="c90ee-112">Löschen Sie die Geräte Sicherheitsgruppe "mysecuritygroup" des viel-Hubs mit der Ressourcen-ID "/Subscriptions/xxxxxxxx-xxxx-xxxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/Providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="c90ee-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="c90ee-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c90ee-113">PARAMETERS</span></span>

### <span data-ttu-id="c90ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90ee-114">-DefaultProfile</span></span>
<span data-ttu-id="c90ee-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c90ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c90ee-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="c90ee-116">-HubResourceId</span></span>
<span data-ttu-id="c90ee-117">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c90ee-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c90ee-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c90ee-118">-InputObject</span></span>
<span data-ttu-id="c90ee-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c90ee-119">Input Object.</span></span>

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

### <span data-ttu-id="c90ee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c90ee-120">-Name</span></span>
<span data-ttu-id="c90ee-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c90ee-121">Resource name.</span></span>

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

### <span data-ttu-id="c90ee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c90ee-122">-PassThru</span></span>
<span data-ttu-id="c90ee-123">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c90ee-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="c90ee-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c90ee-124">-ResourceId</span></span>
<span data-ttu-id="c90ee-125">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c90ee-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c90ee-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c90ee-126">-Confirm</span></span>
<span data-ttu-id="c90ee-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c90ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c90ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90ee-128">-WhatIf</span></span>
<span data-ttu-id="c90ee-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c90ee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c90ee-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c90ee-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c90ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90ee-131">CommonParameters</span></span>
<span data-ttu-id="c90ee-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90ee-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c90ee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90ee-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c90ee-134">INPUTS</span></span>

### <span data-ttu-id="c90ee-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c90ee-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="c90ee-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c90ee-136">System.String</span></span>

## <span data-ttu-id="c90ee-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c90ee-137">OUTPUTS</span></span>

### <span data-ttu-id="c90ee-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c90ee-138">System.Boolean</span></span>

## <span data-ttu-id="c90ee-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c90ee-139">NOTES</span></span>

## <span data-ttu-id="c90ee-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c90ee-140">RELATED LINKS</span></span>
