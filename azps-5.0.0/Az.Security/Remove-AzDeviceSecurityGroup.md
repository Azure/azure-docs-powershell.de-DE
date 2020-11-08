---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176938"
---
# <span data-ttu-id="237b3-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="237b3-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="237b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="237b3-102">SYNOPSIS</span></span>
<span data-ttu-id="237b3-103">Gruppe "Gerätesicherheit löschen"</span><span class="sxs-lookup"><span data-stu-id="237b3-103">Delete device security group</span></span>

## <span data-ttu-id="237b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="237b3-104">SYNTAX</span></span>

### <span data-ttu-id="237b3-105">ResourceIdLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="237b3-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237b3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="237b3-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237b3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="237b3-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237b3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="237b3-108">DESCRIPTION</span></span>
<span data-ttu-id="237b3-109">Das Remove-AzDeviceSecurityGroup-Cmdlet löscht eine in der viel Sicherheitslösung definierte Geräte Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="237b3-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="237b3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="237b3-110">EXAMPLES</span></span>

### <span data-ttu-id="237b3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="237b3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="237b3-112">Löschen Sie die Geräte Sicherheitsgruppe "mysecuritygroup" des viel-Hubs mit der Ressourcen-ID "/Subscriptions/xxxxxxxx-xxxx-xxxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/Providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="237b3-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="237b3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="237b3-113">PARAMETERS</span></span>

### <span data-ttu-id="237b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237b3-114">-DefaultProfile</span></span>
<span data-ttu-id="237b3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="237b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="237b3-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="237b3-116">-HubResourceId</span></span>
<span data-ttu-id="237b3-117">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="237b3-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="237b3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="237b3-118">-InputObject</span></span>
<span data-ttu-id="237b3-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="237b3-119">Input Object.</span></span>

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

### <span data-ttu-id="237b3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="237b3-120">-Name</span></span>
<span data-ttu-id="237b3-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="237b3-121">Resource name.</span></span>

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

### <span data-ttu-id="237b3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="237b3-122">-PassThru</span></span>
<span data-ttu-id="237b3-123">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="237b3-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="237b3-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="237b3-124">-ResourceId</span></span>
<span data-ttu-id="237b3-125">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="237b3-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="237b3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="237b3-126">-Confirm</span></span>
<span data-ttu-id="237b3-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="237b3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237b3-128">-WhatIf</span></span>
<span data-ttu-id="237b3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="237b3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237b3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="237b3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237b3-131">CommonParameters</span></span>
<span data-ttu-id="237b3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="237b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237b3-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="237b3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237b3-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="237b3-134">INPUTS</span></span>

### <span data-ttu-id="237b3-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="237b3-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="237b3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="237b3-136">System.String</span></span>

## <span data-ttu-id="237b3-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="237b3-137">OUTPUTS</span></span>

### <span data-ttu-id="237b3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="237b3-138">System.Boolean</span></span>

## <span data-ttu-id="237b3-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="237b3-139">NOTES</span></span>

## <span data-ttu-id="237b3-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="237b3-140">RELATED LINKS</span></span>
