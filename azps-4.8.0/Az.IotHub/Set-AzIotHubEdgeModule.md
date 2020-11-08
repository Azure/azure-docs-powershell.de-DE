---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009807"
---
# <span data-ttu-id="4a614-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="4a614-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="4a614-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a614-102">SYNOPSIS</span></span>
<span data-ttu-id="4a614-103">Setzen Sie Edge-Module auf einem einzelnen Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4a614-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="4a614-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a614-104">SYNTAX</span></span>

### <span data-ttu-id="4a614-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a614-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a614-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a614-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a614-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a614-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a614-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a614-108">DESCRIPTION</span></span>
<span data-ttu-id="4a614-109">Wendet den bereitgestellten Konfigurationsinhalt der Module auf das angegebene Edge-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="4a614-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="4a614-110">Hinweis: beim Ausführen des Befehls wird die Sammlung der auf das Gerät angewendeten Module ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a614-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="4a614-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a614-111">EXAMPLES</span></span>

### <span data-ttu-id="4a614-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a614-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="4a614-113">Testen Sie die Edge-Module während der Entwicklung, indem Sie Module auf einem Zielgerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="4a614-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="4a614-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a614-114">PARAMETERS</span></span>

### <span data-ttu-id="4a614-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a614-115">-DefaultProfile</span></span>
<span data-ttu-id="4a614-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a614-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a614-117">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="4a614-117">-DeviceId</span></span>
<span data-ttu-id="4a614-118">Ziel-Edge-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="4a614-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="4a614-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a614-119">-InputObject</span></span>
<span data-ttu-id="4a614-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4a614-120">IotHub object</span></span>

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

### <span data-ttu-id="4a614-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4a614-121">-IotHubName</span></span>
<span data-ttu-id="4a614-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="4a614-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a614-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="4a614-123">-ModulesContent</span></span>
<span data-ttu-id="4a614-124">Konfigurationsinhalt von Modulen für viel Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="4a614-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a614-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a614-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a614-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4a614-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a614-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4a614-127">-ResourceId</span></span>
<span data-ttu-id="4a614-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4a614-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4a614-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a614-129">-Confirm</span></span>
<span data-ttu-id="4a614-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a614-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a614-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a614-131">-WhatIf</span></span>
<span data-ttu-id="4a614-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a614-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a614-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a614-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a614-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a614-134">CommonParameters</span></span>
<span data-ttu-id="4a614-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a614-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a614-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a614-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a614-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a614-137">INPUTS</span></span>

### <span data-ttu-id="4a614-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4a614-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a614-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4a614-139">System.String</span></span>

## <span data-ttu-id="4a614-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a614-140">OUTPUTS</span></span>

### <span data-ttu-id="4a614-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="4a614-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="4a614-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a614-142">NOTES</span></span>

## <span data-ttu-id="4a614-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a614-143">RELATED LINKS</span></span>
